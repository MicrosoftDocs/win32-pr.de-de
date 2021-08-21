---
title: CSV-Skripts (Comma-separated Value)
description: Windows 2000 enthält das Befehlszeilenprogramm CSVDE zum Importieren von Verzeichnisobjekten mithilfe .csv Dateien und exportieren Verzeichnisobjekte als .csv Dateien.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Durch Trennzeichen getrennte Wertskripts AD
- Skripts, durch Trennzeichen getrenntes Wert-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3764593303f7f2a81c524df16665c74afd1c83909e8286511090ee6c84323bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022446"
---
# <a name="comma-separated-value-csv-scripts"></a>CSV-Skripts (Comma-separated Value)

Windows 2000 enthält das Befehlszeilenprogramm CSVDE zum Importieren von Verzeichnisobjekten mithilfe .csv Dateien und exportieren Verzeichnisobjekte als .csv Dateien. CSV-Skripts werden zur Benutzerfreundlichkeit erstellt. Die erste Zeile im Skript identifiziert die Attribute in den folgenden Zeilen. Spalten werden durch Kommas getrennt. Das Dateiformat ist mit dem Microsoft Excel .csv-Format kompatibel, sodass Dateien problemlos erstellt werden können. Verwenden Sie Excel oder ein anderes Tool, das .csv Dateien lesen und schreiben kann. CSVDE unterstützt Unicode.

## <a name="example-csv-file"></a>CSV-Beispieldatei

Das folgende Codebeispiel ist eine CSV-Datei, die eine Hilfsklasse hinzufügt.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




