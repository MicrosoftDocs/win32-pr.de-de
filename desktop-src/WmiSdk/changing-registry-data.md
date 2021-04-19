---
description: 'Die System Registrierungs Anbieter-Klasse StdRegProv für WMI verfügt über Methoden, die Folgendes ausführen:'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Ändern von Registrierungsdaten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106373413"
---
# <a name="changing-registry-data"></a><span data-ttu-id="5110d-103">Ändern von Registrierungsdaten</span><span class="sxs-lookup"><span data-stu-id="5110d-103">Changing Registry Data</span></span>

<span data-ttu-id="5110d-104">Die [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) -Klasse [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) für WMI verfügt über Methoden, die Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="5110d-104">The [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) class [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) for WMI has methods that do the following:</span></span>

-   <span data-ttu-id="5110d-105">Erstellen oder Löschen von Registrierungs Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="5110d-105">Create or delete registry keys.</span></span>

    <span data-ttu-id="5110d-106">Verwenden Sie " [**kreatekey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) " oder " [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov)".</span><span class="sxs-lookup"><span data-stu-id="5110d-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) or [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span></span>

-   <span data-ttu-id="5110d-107">Erstellen oder löschen Sie benannte Werte, die als Einträge bezeichnet werden, wenn Sie sich Unterschlüssel befinden.</span><span class="sxs-lookup"><span data-stu-id="5110d-107">Create or delete named values, which are called entries when they are under keys.</span></span>

    <span data-ttu-id="5110d-108">Verwenden Sie den Namen eines neuen Werts und [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)oder [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) , um einen benannten Wert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5110d-108">Use the name of a new value and [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov), or [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) to create a named value.</span></span> <span data-ttu-id="5110d-109">Verwenden Sie [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) , um einen benannten Wert zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5110d-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) to delete a named value.</span></span>

-   <span data-ttu-id="5110d-110">Ändern benannter Werte.</span><span class="sxs-lookup"><span data-stu-id="5110d-110">Change named values.</span></span>

    <span data-ttu-id="5110d-111">Verwenden Sie den Namen eines Werts und die Set-Methoden (im vorherigen aufzurufenen Element identifiziert), um vorhandene benannte Werte unter einem Schlüssel zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5110d-111">Use the name of a value and the Set methods (identified in the previous bulleted item) to change existing named values under a key.</span></span> <span data-ttu-id="5110d-112">Sie müssen den Namen eines Werts kennen, um ihn zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5110d-112">You must know the name of a value to change it.</span></span> <span data-ttu-id="5110d-113">Wenn Sie die Wertnamen unter einem Schlüssel nicht kennen, verwenden Sie die [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) -Methode, um die Namen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5110d-113">If you do not know the value names under a key, use the [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) method to obtain the names.</span></span>

<span data-ttu-id="5110d-114">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="5110d-114">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="5110d-115">Erstellen eines Registrierungsschlüssels mit VBScript</span><span class="sxs-lookup"><span data-stu-id="5110d-115">Creating a Registry Key Using VBScript</span></span>](#creating-a-registry-key-using-vbscript)
-   [<span data-ttu-id="5110d-116">Erstellen eines benannten Registrierungs Werts mithilfe von PowerShell und VBScript</span><span class="sxs-lookup"><span data-stu-id="5110d-116">Creating a Named Registry Value Using PowerShell and VBScript</span></span>](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a><span data-ttu-id="5110d-117">Erstellen eines Registrierungsschlüssels mit VBScript</span><span class="sxs-lookup"><span data-stu-id="5110d-117">Creating a Registry Key Using VBScript</span></span>

<span data-ttu-id="5110d-118">Da es sich bei der Registrierung um die zentrale Konfigurations Datenbank für das Betriebssystem, Anwendungen und Dienste handelt, sollten Sie Vorsicht walten lassen, wenn Sie Änderungen an Registrierungs Werten schreiben oder Schlüssel löschen.</span><span class="sxs-lookup"><span data-stu-id="5110d-118">Because the registry is the central configuration database for the operating system, applications, and services, use caution when you write changes to registry values or delete keys.</span></span>

> [!Note]  
> <span data-ttu-id="5110d-119">Der Stamm Unterschlüssel **HKEY \_ - \_ Klassen** des HKEY **\_ Current \_ User (HKCU)** kann nicht überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="5110d-119">You cannot monitor the **HKEY\_CLASSES\_ROOT** subkey of **HKEY\_CURRENT\_USER(HKCU)**.</span></span> <span data-ttu-id="5110d-120">Das Überwachen von **HKEY- \_ Benutzern** wird nicht empfohlen, da die untergeordneten Schlüssel beim Laden von Strukturen angezeigt und ausgeblendet werden.</span><span class="sxs-lookup"><span data-stu-id="5110d-120">Monitoring **HKEY\_USERS** is not recommended because the subkeys appear and disappear as hives are loaded.</span></span>

 

<span data-ttu-id="5110d-121">In den folgenden Codebeispielen wird gezeigt, wie ein neuer Registrierungsschlüssel und ein Unterschlüssel erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5110d-121">The following code examples show how to create a new registry key and a subkey.</span></span>


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a><span data-ttu-id="5110d-122">Erstellen eines benannten Registrierungs Werts mithilfe von PowerShell und VBScript</span><span class="sxs-lookup"><span data-stu-id="5110d-122">Creating a Named Registry Value Using PowerShell and VBScript</span></span>

<span data-ttu-id="5110d-123">Im folgenden Codebeispiel wird gezeigt, wie ein benannter Wert mit dem Namen " **multistringvalue** " unter der **HKEY \_ local \_ Machine** \\ **Software** \\ **myKey** \\ **MySubKey** -Schlüssel erstellt wird, den das vorherige Skript erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="5110d-123">The following code example shows how to create a named value called **MultiStringValue** under the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**MyKey**\\**MySubKey** key that the previous script creates.</span></span> <span data-ttu-id="5110d-124">Das Skript ruft [**StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) auf, um Zeichen folgen Werte in einen neuen benannten Wert zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="5110d-124">The script calls [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) to write string values to a new named value.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

<span data-ttu-id="5110d-125">Mit WMI können Sie die Zugriffssicherheit für einen Registrierungsschlüssel nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="5110d-125">Using WMI, you cannot set access security on a registry key.</span></span> <span data-ttu-id="5110d-126">Allerdings vergleicht die [**StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) -Methode die Sicherheitseinstellungen des aktuellen Benutzers mit der Sicherheits Beschreibung eines Registrierungsschlüssels, um zu bestimmen, ob der Benutzer über eine bestimmte Berechtigung verfügt, z. b. einen **Schlüssel \_ Satz \_ Wert**.</span><span class="sxs-lookup"><span data-stu-id="5110d-126">However, the [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) method compares the security settings of the current user to the security descriptor on a registry key to determine if the user has a specific permission, such as **KEY\_SET\_VALUE**.</span></span>
