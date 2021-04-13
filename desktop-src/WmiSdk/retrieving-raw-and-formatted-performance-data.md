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
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a><span data-ttu-id="fffe8-103">Abrufen der Dokumentation für Rohdaten Objekte und formatierte Leistungsdaten Objekte</span><span class="sxs-lookup"><span data-stu-id="fffe8-103">Retrieving Documentation for Raw and Formatted Performance Data Objects</span></span>

<span data-ttu-id="fffe8-104">Im folgenden Thema wird beschrieben, wie die Online Programmierungs Dokumentation für ein dynamisch erstelltes Rohdaten-oder formatiertes Datenobjekt abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="fffe8-104">The following topic describes how to retrieve the on-line programming documentation for a dynamically-created raw or formatted data object.</span></span>

<span data-ttu-id="fffe8-105">WMI enthält eine Reihe von Objekten, mit denen die Leistung nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="fffe8-105">WMI contains a number of objects that track performance.</span></span> <span data-ttu-id="fffe8-106">Von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleitete Klassen enthalten unformatierte Leistungsdaten und werden vom [Leistungs Anbieter](performance-counter-provider.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fffe8-106">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contain raw, or "uncooked" performance data, and are supported by the [Performance Counter provider](performance-counter-provider.md).</span></span> <span data-ttu-id="fffe8-107">Im Gegensatz dazu enthalten Klassen, die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet sind, "gekochte" oder formatierte Daten und werden von der [formatierten Leistungs Datenanbieter](formatted-performance-data-provider.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fffe8-107">In contrast, classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contain "cooked", or formatted data, and are supported by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="fffe8-108">Beide Anbieter unterstützen jedoch eine Reihe von dynamisch erstellten untergeordneten Klassen.</span><span class="sxs-lookup"><span data-stu-id="fffe8-108">However, both providers support a number of dynamically-created child classes.</span></span> <span data-ttu-id="fffe8-109">Da die Eigenschaften zur Laufzeit hinzugefügt werden, enthalten diese Klassen möglicherweise nicht dokumentierte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fffe8-109">Because the properties are added at run-time, these classes may contain undocumented properties.</span></span> <span data-ttu-id="fffe8-110">Sie können den folgenden Code verwenden, um zu ermitteln, welche Eigenschaften eine bestimmte dynamisch erstellte Klasse aufweist.</span><span class="sxs-lookup"><span data-stu-id="fffe8-110">You can use the following code to identify what properties a given dynamically-created class has.</span></span>

<span data-ttu-id="fffe8-111">**So rufen Sie eine Beschreibung einer dynamisch erstellten Klasse ab**</span><span class="sxs-lookup"><span data-stu-id="fffe8-111">**To retrieve a description of a dynamically-created class**</span></span>

1.  <span data-ttu-id="fffe8-112">Erstellen Sie eine Instanz des Elements, und legen Sie den geänderten Qualifizierer auf true fest.</span><span class="sxs-lookup"><span data-stu-id="fffe8-112">Create an instance of the item, and set the amended qualifier to true.</span></span>

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  <span data-ttu-id="fffe8-113">Rufen Sie die Eigenschaften der-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="fffe8-113">Retrieve the properties of the class.</span></span>

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  <span data-ttu-id="fffe8-114">Zeigen Sie die Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="fffe8-114">Display the properties.</span></span>

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

<span data-ttu-id="fffe8-115">Der folgende Code Ruft die Eigenschafts Beschreibungen für das angegebene [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="fffe8-115">The following code retrieves the property descriptions for the specified [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) object.</span></span>


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



 

 
