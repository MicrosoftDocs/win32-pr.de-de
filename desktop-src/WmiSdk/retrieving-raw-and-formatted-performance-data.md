---
description: Im folgenden Thema wird beschrieben, wie Die Onlineprogrammierungsdokumentation für ein dynamisch erstelltes unformatiertes oder formatiertes Datenobjekt abgerufen wird.
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: Abrufen der Dokumentation für Unformatierte und formatierte Leistungsdatenobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f155d89ffe8e01c3a21809c102780bcedbf461e4b3040ab876ed2836c37e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923076"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>Abrufen der Dokumentation für Unformatierte und formatierte Leistungsdatenobjekte

Im folgenden Thema wird beschrieben, wie Die Onlineprogrammierungsdokumentation für ein dynamisch erstelltes unformatiertes oder formatiertes Datenobjekt abgerufen wird.

WMI enthält eine Reihe von -Objekten, die die Leistung nachverfolgen. Von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitete Klassen enthalten unformatierte oder "nichtcookierte" Leistungsdaten und werden vom [Leistungsindikatoranbieter](performance-counter-provider.md)unterstützt. Im Gegensatz dazu enthalten von [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitete Klassen "cooked" oder formatierte Daten und werden von der [formatierten Leistung Datenanbieter](formatted-performance-data-provider.md)unterstützt.

Beide Anbieter unterstützen jedoch eine Reihe dynamisch erstellter untergeordneter Klassen. Da die Eigenschaften zur Laufzeit hinzugefügt werden, können diese Klassen nicht dokumentierte Eigenschaften enthalten. Sie können den folgenden Code verwenden, um zu ermitteln, welche Eigenschaften eine bestimmte dynamisch erstellte Klasse aufweist.

**So rufen Sie eine Beschreibung einer dynamisch erstellten Klasse ab**

1.  Erstellen Sie eine Instanz des Elements, und legen Sie den geänderten Qualifizierer auf TRUE fest.

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  Rufen Sie die Eigenschaften der -Klasse ab.

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

    

Der folgende Code ruft die Eigenschaftenbeschreibungen für das angegebene [**Win32 \_ PerfFormattedData-Objekt**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) ab.


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



 

 
