---
description: Im folgenden Thema wird beschrieben, wie die Online Programmierungs Dokumentation für ein dynamisch erstelltes Rohdaten-oder formatiertes Datenobjekt abgerufen wird.
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: Abrufen der Dokumentation für Rohdaten Objekte und formatierte Leistungsdaten Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ab9cf66aa4536da25102511fdcbcab6bdd5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349239"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>Abrufen der Dokumentation für Rohdaten Objekte und formatierte Leistungsdaten Objekte

Im folgenden Thema wird beschrieben, wie die Online Programmierungs Dokumentation für ein dynamisch erstelltes Rohdaten-oder formatiertes Datenobjekt abgerufen wird.

WMI enthält eine Reihe von Objekten, mit denen die Leistung nachverfolgt wird. Von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitete Klassen enthalten unformatierte Leistungsdaten und werden vom [Leistungs Anbieter](performance-counter-provider.md)unterstützt. Im Gegensatz dazu enthalten Klassen, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet sind, "gekochte" oder formatierte Daten und werden von der [formatierten Leistungs Datenanbieter](formatted-performance-data-provider.md)unterstützt.

Beide Anbieter unterstützen jedoch eine Reihe von dynamisch erstellten untergeordneten Klassen. Da die Eigenschaften zur Laufzeit hinzugefügt werden, enthalten diese Klassen möglicherweise nicht dokumentierte Eigenschaften. Sie können den folgenden Code verwenden, um zu ermitteln, welche Eigenschaften eine bestimmte dynamisch erstellte Klasse aufweist.

**So rufen Sie eine Beschreibung einer dynamisch erstellten Klasse ab**

1.  Erstellen Sie eine Instanz des Elements, und legen Sie den geänderten Qualifizierer auf true fest.

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  Rufen Sie die Eigenschaften der-Klasse ab.

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  Zeigen Sie die Eigenschaften an.

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

Der folgende Code Ruft die Eigenschafts Beschreibungen für das angegebene [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Objekt ab.


```PowerShell
$osClass = New-Object System.Management.ManagementClass Win32_PerfFormattedData_APPPOOLCountersProvider_APPPOOLWAS  
$osClass.Options.UseAmendedQualifiers = $true  
  
# Get the Properties in the class  
$properties = $osClass.Properties  
"This class has {0} properties as follows:" -f $properties.count  
  
  
# display the Property name, description, type, qualifiers and instance values  
  
foreach ($property in $properties) {  
"Property Name: {0}" -f $property.Name  
"Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
"Type:          {0}" -f $property.Type  
"-------"  
}
```



 

 
