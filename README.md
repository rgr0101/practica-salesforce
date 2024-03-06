<div>
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Salesforce.com_logo.svg/2560px-Salesforce.com_logo.svg.png" alt="Salesforce Logo" style="width: 250px; height: 200px;">
  <img src="https://www.muylinux.com/wp-content/uploads/2017/06/github.png" alt="Texto alternativo" style="width: 250px; height: 200px;">
</div>

## Pasos para cargar un custom field y un flow a un repositorio en git. 
### Crear repoositorio en github

### Clonar repositorio en nuestra PC
```bash
git clone https://github.com/rgr0101/practica-salesforce.git
cd practica-salesforce
```
### Crear proyecto de Salesforce 
### (Tambien es posible crearlo con las extensiones de VS Code)
```bash
sfdx force:project:create -n practica
```

### Realizar commit de la creación del proyecto
```bash
git add .
git commit -m “Crear proyecto Salesforce”
```

### Acceder a proyecto creado ¨practica¨
```bash
cd practica
```

### Verificar org autorizadas en el entorno local
#### (Para este caso VSCodePlayground)
```bash
sfdx force:org:list
```

## Cargar Custom Field TextoPrueba del objeto Account
```bash
sfdx force:source:retrieve -m CustomField:Account.TextoPrueba__c -o VSCodePlayground
```

### Realizar commit del Custom Field\
```bash
git add .
git commit -m "Carga custom field TextoPrueba de object Account"
```

## Cargar Flow "PRACTICA"
```bash
sfdx force:source:retrieve -m Flow:PRACTICA -o VSCodePlayground
```

### Realizar commit del Custom Field
```bash
git add .
git commit -m “Carga flow PRACTICA”
```

### Subir cambios al repositorio remoto (github) en la rama principal
```bash
git push origin main
```


