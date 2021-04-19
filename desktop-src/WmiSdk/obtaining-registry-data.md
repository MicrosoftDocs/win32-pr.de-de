---
description: Sie können Registrierungsdaten abrufen oder ändern, indem Sie die WMI-Klasse "StdRegProv" und deren Methoden verwenden.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Abrufen von Registrierungsdaten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346673"
---
# <a name="obtaining-registry-data"></a><span data-ttu-id="e1c4a-103">Abrufen von Registrierungsdaten</span><span class="sxs-lookup"><span data-stu-id="e1c4a-103">Obtaining Registry Data</span></span>

<span data-ttu-id="e1c4a-104">Sie können Registrierungsdaten abrufen oder ändern, indem Sie die WMI-Klasse " [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) " und deren Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-104">You can obtain or modify registry data by using the WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class and its methods.</span></span> <span data-ttu-id="e1c4a-105">Wenn Sie das Hilfsprogramm regedit verwenden, um Registrierungs Werte auf dem lokalen Computer anzuzeigen und zu ändern, können Sie mit **StdRegProv** ein Skript oder eine Anwendung verwenden, um solche Aktivitäten auf dem lokalen Computer und auf Remote Computern zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-105">While use the Regedit utility to view and change registry values on the local computer, **StdRegProv** allows you to use a script or application to automate such activities on the local computer and remote computers.</span></span>

<span data-ttu-id="e1c4a-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) enthält Methoden für folgende Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="e1c4a-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contains methods to do the following:</span></span>

-   <span data-ttu-id="e1c4a-107">Überprüfen der Zugriffsberechtigungen für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="e1c4a-107">Verify the access permissions for a user</span></span>
-   <span data-ttu-id="e1c4a-108">Erstellen, auflisten und Löschen von Registrierungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="e1c4a-108">Create, enumerate, and delete registry keys</span></span>
-   <span data-ttu-id="e1c4a-109">Erstellen, aufzählen und Löschen von unter Schlüsseln oder benannten Werten</span><span class="sxs-lookup"><span data-stu-id="e1c4a-109">Create, enumerate, and delete subkeys or named values</span></span>
-   <span data-ttu-id="e1c4a-110">Lesen, schreiben und Löschen von Datenwerten</span><span class="sxs-lookup"><span data-stu-id="e1c4a-110">Read, write, and delete data values</span></span>

<span data-ttu-id="e1c4a-111">Registrierungsdaten werden nach Teil Strukturen, Schlüsseln und unter Schlüsseln organisiert, die unter einem Schlüssel der obersten Ebene gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-111">Registry data is organized by subtrees, keys, and subkeys nested under a top level key.</span></span> <span data-ttu-id="e1c4a-112">Die tatsächlichen Datenwerte werden als Einträge oder benannte Werte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-112">The actual data values are called entries or named values.</span></span>

<span data-ttu-id="e1c4a-113">Die Unterstrukturen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e1c4a-113">The subtrees include the following:</span></span>

-   <span data-ttu-id="e1c4a-114">**HKEY \_ Klassen \_** Stamm (abgekürzt als **HKCR**)</span><span class="sxs-lookup"><span data-stu-id="e1c4a-114">**HKEY\_CLASSES\_ROOT** (abbreviated as **HKCR**)</span></span>
-   <span data-ttu-id="e1c4a-115">**HKEY \_ aktueller \_ Benutzer** (**HKCU**)</span><span class="sxs-lookup"><span data-stu-id="e1c4a-115">**HKEY\_CURRENT\_USER** (**HKCU**)</span></span>
-   <span data-ttu-id="e1c4a-116">**HKEY \_ lokaler \_ Computer** (**HKLM**)</span><span class="sxs-lookup"><span data-stu-id="e1c4a-116">**HKEY\_LOCAL\_MACHINE** (**HKLM**)</span></span>
-   <span data-ttu-id="e1c4a-117">**HKEY- \_ Benutzer**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-117">**HKEY\_USERS**</span></span>
-   <span data-ttu-id="e1c4a-118">**aktuelle HKEY- \_ \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-118">**HKEY\_CURRENT\_CONFIG**</span></span>

<span data-ttu-id="e1c4a-119">Im Registrierungs Eintrag **HKEY** \\ **Software** \\ **Microsoft** \\ **DirectX** \\ **installedversion** lautet die HKEY-Unterstruktur beispielsweise **Software**. die Unterschlüssel sind **Microsoft** und **DirectX**, und der benannte Wert Eintrag ist **installedversion**.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-119">For example, in the registry entry **HKEY**\\**SOFTWARE**\\**Microsoft**\\**DirectX**\\**InstalledVersion**, the HKEY subtree is **SOFTWARE**; the subkeys are **Microsoft** and **DirectX**; and the named value entry is **InstalledVersion**.</span></span>

<span data-ttu-id="e1c4a-120">Ein [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) tritt auf, wenn eine Änderung an einem bestimmten Schlüssel auftritt, aber der Eintrag nicht identifiziert, wie sich die Werte ändern, und dass dieses Ereignis nicht durch Änderungen unter dem angegebenen Schlüssel ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-120">A [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) occurs when a change to a specific key occurs, but the entry does not identify how the values change nor will this event be triggered by changes below the specified key.</span></span> <span data-ttu-id="e1c4a-121">Um Änderungen an beliebiger Stelle in einer hierarchischen Schlüsselstruktur zu identifizieren, verwenden Sie das [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), das keine bestimmten Werte oder Schlüssel Änderungen zurückgibt, die auftreten.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-121">To identify changes anywhere in a hierarchical key structure, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), which does not return specific values or key changes that occur.</span></span> <span data-ttu-id="e1c4a-122">Um einen bestimmten Wert für den Einstiegs Wert zu erhalten, verwenden Sie das [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), und lesen Sie dann den Eintrag, um einen Baselinewert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-122">To obtain a specific entry value change, use the [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), and then read the entry to obtain a baseline value.</span></span>

<span data-ttu-id="e1c4a-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) verfügt nur über Methoden, die von C++ oder Skript aufgerufen werden können. Dies unterscheidet sich von der Win32-Klassenstruktur.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) only has methods that can be called from C++ or script, which is different from the Win32 class structure.</span></span>

<span data-ttu-id="e1c4a-124">Im folgenden Codebeispiel wird gezeigt, wie die [**StdRegProv. EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) -Methode verwendet wird, um alle Microsoft-Software Unterschlüssel unter dem Registrierungsschlüssel aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-124">The following code example shows how to use the [**StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) method to list all of the Microsoft software subkeys under the registry key.</span></span>

<span data-ttu-id="e1c4a-125">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





<span data-ttu-id="e1c4a-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) verfügt über verschiedene Methoden zum Lesen der verschiedenen Datentypen von Registrierungs Eintrags Werten.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) has different methods for reading the various registry entry value data types.</span></span> <span data-ttu-id="e1c4a-127">Wenn der Eintrag unbekannte Werte enthält, können Sie [**StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) zum Auflisten der Werte abrufen.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-127">If the entry has unknown values, then you can call [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) to list them.</span></span> <span data-ttu-id="e1c4a-128">In der folgenden Tabelle werden die Entsprechungen zwischen **StdRegProv** -Methoden und den-Datentypen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-128">The following table lists the correspondence between **StdRegProv** methods and the data types.</span></span>



| <span data-ttu-id="e1c4a-129">Methode</span><span class="sxs-lookup"><span data-stu-id="e1c4a-129">Method</span></span>                                                                                  | <span data-ttu-id="e1c4a-130">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e1c4a-130">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="e1c4a-131">**GetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-131">**GetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="e1c4a-132">**REG- \_ Binärdatei**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-132">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="e1c4a-133">**GetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-133">**GetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="e1c4a-134">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-134">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="e1c4a-135">**GetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-135">**GetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="e1c4a-136">**REG \_ Expand \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-136">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="e1c4a-137">**GetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-137">**GetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="e1c4a-138">**REG \_ \_ MultiSZ**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-138">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="e1c4a-139">**GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-139">**GetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="e1c4a-140">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-140">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="e1c4a-141">In der folgenden Tabelle werden die entsprechenden Methoden zum Erstellen neuer Schlüssel oder Werte oder zum Ändern vorhandener-Werte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-141">The following table lists the corresponding methods for creating new keys or values, or changing existing ones.</span></span>



| <span data-ttu-id="e1c4a-142">Methode</span><span class="sxs-lookup"><span data-stu-id="e1c4a-142">Method</span></span>                                                                                  | <span data-ttu-id="e1c4a-143">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e1c4a-143">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="e1c4a-144">**SetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-144">**SetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="e1c4a-145">**REG- \_ Binärdatei**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-145">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="e1c4a-146">**SetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-146">**SetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="e1c4a-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-147">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="e1c4a-148">**"Abtexpandedstringvalue"**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-148">**SetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="e1c4a-149">**REG \_ Expand \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-149">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="e1c4a-150">**SetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-150">**SetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="e1c4a-151">**REG \_ \_ MultiSZ**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-151">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="e1c4a-152">**SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-152">**SetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="e1c4a-153">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="e1c4a-153">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="e1c4a-154">Im folgenden Beispiel wird gezeigt, wie die Liste der Quellen für das System Ereignisprotokoll aus dem Registrierungsschlüssel gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-154">The following example shows how to read the list of sources for the system event log from the registry key.</span></span>

<span data-ttu-id="e1c4a-155">**HKEY \_ \_** \\ **System** \\ **Aktuelles System Steuerungs Satz** \\ **Dienste**- \\ **Ereignisprotokoll** \\ **System** des lokalen Computers</span><span class="sxs-lookup"><span data-stu-id="e1c4a-155">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Services**\\**Eventlog**\\**System**</span></span>

<span data-ttu-id="e1c4a-156">Beachten Sie, dass die Elemente im mehrteiligen Zeichen folgen Wert als Sammlung oder Array behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-156">Note that the items in the multistring value are treated as a collection or array.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



<span data-ttu-id="e1c4a-157">Der Registrierungs Anbieter wird in LocalService gehostet – nicht in LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-157">The registry provider is hosted in LocalService—not the LocalSystem.</span></span> <span data-ttu-id="e1c4a-158">Aus diesem Grund ist das Abrufen von Informationen aus der Unterstruktur **HKEY \_ aktueller \_ Benutzer** nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-158">Therefore, obtaining information remotely from the subtree **HKEY\_CURRENT\_USER** is not possible.</span></span> <span data-ttu-id="e1c4a-159">Skripts, die auf dem lokalen Computer ausgeführt werden, können jedoch weiterhin auf den **aktuellen HKEY- \_ \_ Benutzer** zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-159">However, scripts run on the local computer can still access **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="e1c4a-160">Sie können das Hostingmodell auf einem Remote Computer auf "LocalSystem" festlegen, dies ist jedoch ein Sicherheitsrisiko, da die Registrierung auf dem Remote Computer anfällig für feindlichen Zugriff ist.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-160">You can set the hosting model to LocalSystem on a remote machine, but that is a security risk because the registry on the remote machine is vulnerable to hostile access.</span></span> <span data-ttu-id="e1c4a-161">Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="e1c4a-161">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e1c4a-162">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1c4a-162">Examples</span></span>

<span data-ttu-id="e1c4a-163">Der Code zum [Lesen eines binären Registrierungs Werts](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript in der TechNet Gallery verwendet WMI, um einen binären Registrierungs Wert zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e1c4a-163">The [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript code example on TechNet Gallery uses WMI to read a binary registry value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1c4a-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1c4a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c4a-165">WMI-Tasks: Registrierung</span><span class="sxs-lookup"><span data-stu-id="e1c4a-165">WMI Tasks: Registry</span></span>](wmi-tasks--registry.md)
</dt> </dl>

 

 
