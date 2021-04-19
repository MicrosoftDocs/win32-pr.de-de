---
title: ConnectionOptions-Objekt (WSManDisp. h)
description: Das ConnectionOptions-Objekt wird an die Methode "kreatesession" übergeben, um den Benutzernamen und das Kennwort anzugeben, die dem lokalen Konto auf dem Remote Computer zugeordnet sind.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- ConnectionOptions-Objekt Windows-Remoteverwaltung
- ConnectionOptions-Objekt Windows-Remoteverwaltung, beschrieben
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343454"
---
# <a name="connectionoptions-object"></a><span data-ttu-id="04b42-105">ConnectionOptions-Objekt</span><span class="sxs-lookup"><span data-stu-id="04b42-105">ConnectionOptions object</span></span>

<span data-ttu-id="04b42-106">Das **ConnectionOptions** -Objekt wird an die Methode " [**kreatesession**](wsman-createsession.md) " übergeben, um den Benutzernamen und das Kennwort anzugeben, die dem lokalen Konto auf dem Remote Computer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="04b42-106">The **ConnectionOptions** object is passed to the [**CreateSession**](wsman-createsession.md) method to provide the user name and password associated with the local account on the remote computer.</span></span> <span data-ttu-id="04b42-107">Wenn keine Parameter angegeben werden, werden die Anmelde Informationen des Kontos, auf dem das Skript ausgeführt wird, auf die Standardwerte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04b42-107">If no parameters are supplied, then the credentials of the account running the script are set to the default values.</span></span>

## <a name="members"></a><span data-ttu-id="04b42-108">Member</span><span class="sxs-lookup"><span data-stu-id="04b42-108">Members</span></span>

<span data-ttu-id="04b42-109">Das **ConnectionOptions** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="04b42-109">The **ConnectionOptions** object has these types of members:</span></span>

-   [<span data-ttu-id="04b42-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04b42-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04b42-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="04b42-111">Properties</span></span>

<span data-ttu-id="04b42-112">Das **ConnectionOptions** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="04b42-112">The **ConnectionOptions** object has these properties.</span></span>



| <span data-ttu-id="04b42-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="04b42-113">Property</span></span>                                                  | <span data-ttu-id="04b42-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="04b42-114">Access type</span></span>           | <span data-ttu-id="04b42-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04b42-115">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04b42-116">**Kennwort**</span><span class="sxs-lookup"><span data-stu-id="04b42-116">**Password**</span></span>](connectionoptions-password.md)<br/> | <span data-ttu-id="04b42-117">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="04b42-117">Write-only</span></span><br/> | <span data-ttu-id="04b42-118">Legt das Kennwort eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer fest.</span><span class="sxs-lookup"><span data-stu-id="04b42-118">Sets the password of a local or domain account on the remote computer.</span></span><br/>           |
| [<span data-ttu-id="04b42-119">**User**</span><span class="sxs-lookup"><span data-stu-id="04b42-119">**UserName**</span></span>](connectionoptions-username.md)<br/> | <span data-ttu-id="04b42-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="04b42-120">Read/write</span></span><br/> | <span data-ttu-id="04b42-121">Hiermit wird der Benutzername eines lokalen Kontos oder eines Domänen Kontos auf dem Remote Computer festgelegt und abgerufen.</span><span class="sxs-lookup"><span data-stu-id="04b42-121">Sets and gets the user name of a local or domain account on the remote computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04b42-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04b42-122">Remarks</span></span>

<span data-ttu-id="04b42-123">Das **ConnectionOptions** -Objekt entspricht der [**iwsmanconnectionoptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="04b42-123">The **ConnectionOptions** object corresponds to the [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) interface.</span></span>

<span data-ttu-id="04b42-124">Wenn eine Windows-Remoteverwaltung Client Anwendung unter dem Identitätswechsel ausgeführt wird, tritt ein Fehler auf, wenn Sie die Kenn [**Wort**](connectionoptions-password.md) Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="04b42-124">If a Windows Remote Management client application is running under impersonation, then a failure occurs if you set the [**Password**](connectionoptions-password.md) property.</span></span> <span data-ttu-id="04b42-125">Bei einer Client Anwendung handelt es sich um ein Skript oder ein anderes Programm, das eine Anforderung an WinRM auf dem lokalen Computer oder auf einem Remote Computer sendet.</span><span class="sxs-lookup"><span data-stu-id="04b42-125">A client application is a script or other program that sends a request to WinRM on the local or a remote computer.</span></span> <span data-ttu-id="04b42-126">Die Client Anwendung wird möglicherweise unter dem Identitätswechsel ausgeführt, da Sie eine [**Funktion wie "**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85))Identitätsnachweis Nachweis" genannt hat.</span><span class="sxs-lookup"><span data-stu-id="04b42-126">The client application may be running under impersonation because it called a function like [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)).</span></span> <span data-ttu-id="04b42-127">Eine Active Server Seite (ASP) oder ein Dienst kann keinen Benutzernamen und kein Kennwort anfordern, wenn der ASP-Prozess unter einem Konto ausgeführt wird, das die Identität eines Clients annimmt.</span><span class="sxs-lookup"><span data-stu-id="04b42-127">An Active Server Page (ASP) or service cannot request a user name and password if the ASP process runs under an account that impersonates a client.</span></span>

<span data-ttu-id="04b42-128">Das Flag " **wsmanflagkredusernamepassword** " sollte für den [**WSMAN. anatesession**](wsman-createsession.md) -Befehl festgelegt werden, wenn der [**Benutzername**](connectionoptions-username.md) und das [**Kennwort**](connectionoptions-password.md) für die Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04b42-128">The **WSManFlagCredUserNamePassword** flag should be set on the [**WSman.CreateSession**](wsman-createsession.md) call when using the [**UserName**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md) for authentication.</span></span>

## <a name="examples"></a><span data-ttu-id="04b42-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04b42-129">Examples</span></span>

<span data-ttu-id="04b42-130">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie ein **ConnectionOptions** -Objekt erstellt, die Eigenschaften für das Konto auf dem Remote Computer festgelegt und beim Erstellen eines [**Sitzungs**](session.md) Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04b42-130">The following VBScript code example shows how to create a **ConnectionOptions** object, set the properties for the account on the remote computer, and use it in creating a [**Session**](session.md) object.</span></span>


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a><span data-ttu-id="04b42-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04b42-131">Requirements</span></span>



| <span data-ttu-id="04b42-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04b42-132">Requirement</span></span> | <span data-ttu-id="04b42-133">Wert</span><span class="sxs-lookup"><span data-stu-id="04b42-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b42-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04b42-134">Minimum supported client</span></span><br/> | <span data-ttu-id="04b42-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04b42-135">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="04b42-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04b42-136">Minimum supported server</span></span><br/> | <span data-ttu-id="04b42-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04b42-137">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="04b42-138">Header</span><span class="sxs-lookup"><span data-stu-id="04b42-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="04b42-139"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b42-139"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="04b42-140">IDL</span><span class="sxs-lookup"><span data-stu-id="04b42-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04b42-141"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04b42-141"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="04b42-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04b42-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="04b42-143"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="04b42-143"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="04b42-144">DLL</span><span class="sxs-lookup"><span data-stu-id="04b42-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04b42-145"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04b42-145"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04b42-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04b42-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b42-147">Authentifizierung für Remote Verbindungen</span><span class="sxs-lookup"><span data-stu-id="04b42-147">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="04b42-148">WinRM-Skript-API</span><span class="sxs-lookup"><span data-stu-id="04b42-148">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="04b42-149">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="04b42-149">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="04b42-150">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="04b42-150">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="04b42-151">Skripterstellung in Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="04b42-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="04b42-152">Abrufen von Daten vom lokalen Computer</span><span class="sxs-lookup"><span data-stu-id="04b42-152">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="04b42-153">Abrufen von Daten von einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="04b42-153">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

