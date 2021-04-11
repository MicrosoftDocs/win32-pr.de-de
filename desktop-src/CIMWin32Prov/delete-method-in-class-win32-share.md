---
description: Löscht einen Freigabe Namen aus der Liste der freigegebenen Ressourcen eines Servers und trennt Verbindungen mit der freigegebenen Ressource.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Delete-Methode der Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126921"
---
# <a name="delete-method-of-the-win32_share-class"></a><span data-ttu-id="83928-103">Delete-Methode der Win32- \_ Freigabe Klasse</span><span class="sxs-lookup"><span data-stu-id="83928-103">Delete method of the Win32\_Share class</span></span>

<span data-ttu-id="83928-104">Die **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode löscht einen Freigabe Namen aus der Liste der freigegebenen Ressourcen eines Servers und trennt Verbindungen mit der freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="83928-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span>

<span data-ttu-id="83928-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="83928-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="83928-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="83928-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="83928-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="83928-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="83928-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="83928-108">Parameters</span></span>

<span data-ttu-id="83928-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="83928-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83928-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83928-110">Return value</span></span>

<span data-ttu-id="83928-111">Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="83928-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="83928-112">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="83928-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="83928-113">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="83928-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="83928-114">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="83928-114">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83928-115">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="83928-115">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="83928-116">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="83928-116">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="83928-117">**Ungültiger Name** (9)</span><span class="sxs-lookup"><span data-stu-id="83928-117">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="83928-118">**Ungültige Ebene** (10)</span><span class="sxs-lookup"><span data-stu-id="83928-118">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="83928-119">**Ungültiger Parameter** (21)</span><span class="sxs-lookup"><span data-stu-id="83928-119">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="83928-120">**Doppelte Freigabe** (22)</span><span class="sxs-lookup"><span data-stu-id="83928-120">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="83928-121">**Umgeleiteter Pfad** (23)</span><span class="sxs-lookup"><span data-stu-id="83928-121">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="83928-122">**Unbekanntes Gerät oder Verzeichnis** (24)</span><span class="sxs-lookup"><span data-stu-id="83928-122">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="83928-123">Der **Netzwerkname wurde nicht gefunden** (25).</span><span class="sxs-lookup"><span data-stu-id="83928-123">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="83928-124">**Sonstige** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="83928-124">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="83928-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83928-125">Remarks</span></span>

<span data-ttu-id="83928-126">Die **Delete** -Methode ist eine Objektmethode und wird für eine Instanz einer-Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="83928-126">The **Delete** method is an object method and is used on an instance of a class.</span></span>

<span data-ttu-id="83928-127">Nur Mitglieder der lokalen Gruppe "Administratoren" oder "Konto-Operatoren" oder die Gruppenmitgliedschaften "Kommunikation", "Drucken" oder "Server Operator" können die Methode erfolgreich ausführen.</span><span class="sxs-lookup"><span data-stu-id="83928-127">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute the method.</span></span> <span data-ttu-id="83928-128">Der Druck Operator kann nur Drucker Warteschlangen löschen.</span><span class="sxs-lookup"><span data-stu-id="83928-128">The Print operator can delete only printer queues.</span></span> <span data-ttu-id="83928-129">Der Kommunikations Operator kann nur Verbindungsgeräte Warteschlangen löschen.</span><span class="sxs-lookup"><span data-stu-id="83928-129">The Communication operator can delete only communication-device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="83928-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83928-130">Examples</span></span>

<span data-ttu-id="83928-131">Im folgenden VBScript-Codebeispiel wird die angegebene Freigabe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="83928-131">The following VBScript code sample deletes the specified share.</span></span>


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



<span data-ttu-id="83928-132">Im folgenden PowerShell-Codebeispiel werden leere Freigaben gelöscht.</span><span class="sxs-lookup"><span data-stu-id="83928-132">The following PowerShell code sample deletes blank shares.</span></span>


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



## <a name="requirements"></a><span data-ttu-id="83928-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83928-133">Requirements</span></span>



| <span data-ttu-id="83928-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83928-134">Requirement</span></span> | <span data-ttu-id="83928-135">Wert</span><span class="sxs-lookup"><span data-stu-id="83928-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83928-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="83928-136">Minimum supported client</span></span><br/> | <span data-ttu-id="83928-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83928-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="83928-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="83928-138">Minimum supported server</span></span><br/> | <span data-ttu-id="83928-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83928-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="83928-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="83928-140">Namespace</span></span><br/>                | <span data-ttu-id="83928-141">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="83928-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="83928-142">MOF</span><span class="sxs-lookup"><span data-stu-id="83928-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83928-143"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="83928-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="83928-144">DLL</span><span class="sxs-lookup"><span data-stu-id="83928-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83928-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83928-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83928-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83928-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="83928-147">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="83928-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="83928-148">**Win32- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="83928-148">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

