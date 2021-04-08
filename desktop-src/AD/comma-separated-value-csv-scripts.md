---
title: CSV-Skripts (Comma-Separated Value)
description: Windows 2000 umfasst das Befehlszeilen-Hilfsprogramm CSVDE zum Importieren von Verzeichnis Objekten mithilfe von CSV-Dateien und Exportieren von Verzeichnis Objekten als CSV-Dateien.
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- Durch Trennzeichen getrennte Skripts AD
- Skripts, durch Kommas getrennte Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec737f971bd7e462b8f6f0ef6e9e3df786a207cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707200"
---
# <a name="comma-separated-value-csv-scripts"></a>CSV-Skripts (Comma-Separated Value)

Windows 2000 umfasst das Befehlszeilen-Hilfsprogramm CSVDE zum Importieren von Verzeichnis Objekten mithilfe von CSV-Dateien und Exportieren von Verzeichnis Objekten als CSV-Dateien. CSV-Skripts werden zur leichteren Verwendung erstellt. Die erste Zeile im Skript identifiziert die Attribute in den folgenden Zeilen. Spalten werden durch Kommas getrennt. Das Dateiformat ist mit dem Microsoft Excel. CSV-Format kompatibel, sodass Dateien problemlos erstellt werden können. Verwenden Sie Excel oder ein anderes Tool, mit dem CSV-Dateien gelesen und geschrieben werden können. CSVDE unterstützt Unicode.

## <a name="example-csv-file"></a>Beispiel-CSV-Datei

Das folgende Codebeispiel ist eine CSV-Datei, die eine Hilfsklasse hinzufügt.

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




