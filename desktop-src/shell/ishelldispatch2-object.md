---
description: Erweitert das ishelldispatch-Objekt mit einer Reihe von neuen Funktionen.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: IShellDispatch2-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978032"
---
# <a name="ishelldispatch2-object"></a><span data-ttu-id="85edc-103">IShellDispatch2-Objekt</span><span class="sxs-lookup"><span data-stu-id="85edc-103">IShellDispatch2 object</span></span>

<span data-ttu-id="85edc-104">Erweitert das [**ishelldispatch**](ishelldispatch.md) -Objekt mit einer Reihe von neuen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="85edc-104">Extends the [**IShellDispatch**](ishelldispatch.md) object with a variety of new functionality.</span></span>

> [!Note]  
> <span data-ttu-id="85edc-105">**IShellDispatch2** wird implementiert, und der Zugriff erfolgt über das [**Shellobjekt**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="85edc-105">**IShellDispatch2** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="85edc-106">Member</span><span class="sxs-lookup"><span data-stu-id="85edc-106">Members</span></span>

<span data-ttu-id="85edc-107">Das **IShellDispatch2** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="85edc-107">The **IShellDispatch2** object has these types of members:</span></span>

-   [<span data-ttu-id="85edc-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="85edc-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="85edc-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="85edc-109">Methods</span></span>

<span data-ttu-id="85edc-110">Das **IShellDispatch2** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="85edc-110">The **IShellDispatch2** object has these methods.</span></span>



| <span data-ttu-id="85edc-111">Methode</span><span class="sxs-lookup"><span data-stu-id="85edc-111">Method</span></span>                                                               | <span data-ttu-id="85edc-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85edc-112">Description</span></span>                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="85edc-113">**Canstartstopservice**</span><span class="sxs-lookup"><span data-stu-id="85edc-113">**CanStartStopService**</span></span>](ishelldispatch2-canstartstopservice.md)   | <span data-ttu-id="85edc-114">Bestimmt, ob der aktuelle Benutzer den benannten Dienst starten und Abbrechen kann.</span><span class="sxs-lookup"><span data-stu-id="85edc-114">Determines if the current user can start and stop the named service.</span></span><br/>    |
| [<span data-ttu-id="85edc-115">**Findprinter**</span><span class="sxs-lookup"><span data-stu-id="85edc-115">**FindPrinter**</span></span>](ishelldispatch2-findprinter.md)                   | <span data-ttu-id="85edc-116">Zeigt das Dialogfeld **Drucker suchen** an.</span><span class="sxs-lookup"><span data-stu-id="85edc-116">Displays the **Find Printer** dialog box.</span></span><br/>                               |
| [<span data-ttu-id="85edc-117">**Getsysteminformation**</span><span class="sxs-lookup"><span data-stu-id="85edc-117">**GetSystemInformation**</span></span>](ishelldispatch2-getsysteminformation.md) | <span data-ttu-id="85edc-118">Ruft Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="85edc-118">Retrieves system information.</span></span><br/>                                           |
| [<span data-ttu-id="85edc-119">**IsRestricted**</span><span class="sxs-lookup"><span data-stu-id="85edc-119">**IsRestricted**</span></span>](ishelldispatch2-isrestricted.md)                 | <span data-ttu-id="85edc-120">Ruft die Einschränkungs Einstellung einer Gruppe aus der Registrierung ab.</span><span class="sxs-lookup"><span data-stu-id="85edc-120">Retrieves a group's restriction setting from the registry.</span></span><br/>              |
| [<span data-ttu-id="85edc-121">**Isservicerunning**</span><span class="sxs-lookup"><span data-stu-id="85edc-121">**IsServiceRunning**</span></span>](ishelldispatch2-isservicerunning.md)         | <span data-ttu-id="85edc-122">Gibt einen Wert zurück, der angibt, ob ein bestimmter Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85edc-122">Returns a value that indicates whether a particular service is running.</span></span><br/> |
| [<span data-ttu-id="85edc-123">**Servicestart**</span><span class="sxs-lookup"><span data-stu-id="85edc-123">**ServiceStart**</span></span>](ishelldispatch2-servicestart.md)                 | <span data-ttu-id="85edc-124">Startet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="85edc-124">Starts a named service.</span></span><br/>                                                 |
| [<span data-ttu-id="85edc-125">**Servicestop**</span><span class="sxs-lookup"><span data-stu-id="85edc-125">**ServiceStop**</span></span>](ishelldispatch2-servicestop.md)                   | <span data-ttu-id="85edc-126">Beendet einen benannten Dienst.</span><span class="sxs-lookup"><span data-stu-id="85edc-126">Stops a named service.</span></span><br/>                                                  |
| [<span data-ttu-id="85edc-127">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="85edc-127">**ShellExecute**</span></span>](ishelldispatch2-shellexecute.md)                 | <span data-ttu-id="85edc-128">Führt einen angegebenen Vorgang für eine angegebene Datei aus.</span><span class="sxs-lookup"><span data-stu-id="85edc-128">Performs a specified operation on a specified file.</span></span><br/>                     |
| [<span data-ttu-id="85edc-129">**Showbrowserbar**</span><span class="sxs-lookup"><span data-stu-id="85edc-129">**ShowBrowserBar**</span></span>](ishelldispatch2-showbrowserbar.md)             | <span data-ttu-id="85edc-130">Zeigt eine Browserleiste an.</span><span class="sxs-lookup"><span data-stu-id="85edc-130">Displays a browser bar.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="85edc-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85edc-131">Remarks</span></span>

<span data-ttu-id="85edc-132">Eine Erläuterung der Windows-Dienste finden Sie in der Dokumentation zu [Diensten](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="85edc-132">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="85edc-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="85edc-133">Requirements</span></span>



| <span data-ttu-id="85edc-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85edc-134">Requirement</span></span> | <span data-ttu-id="85edc-135">Wert</span><span class="sxs-lookup"><span data-stu-id="85edc-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85edc-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85edc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="85edc-137">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85edc-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85edc-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85edc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="85edc-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85edc-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="85edc-140">Header</span><span class="sxs-lookup"><span data-stu-id="85edc-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="85edc-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="85edc-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="85edc-142">IDL</span><span class="sxs-lookup"><span data-stu-id="85edc-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="85edc-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="85edc-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="85edc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="85edc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85edc-145"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="85edc-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85edc-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85edc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85edc-147">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="85edc-147">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="85edc-148">**Shellobjekt**</span><span class="sxs-lookup"><span data-stu-id="85edc-148">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="85edc-149">**Ishelldispatch**</span><span class="sxs-lookup"><span data-stu-id="85edc-149">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> </dl>

 

 
