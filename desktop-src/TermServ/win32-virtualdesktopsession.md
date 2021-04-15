---
title: Win32_VirtualDesktopSession-Klasse
description: Verwaltet eine virtuelle Desktop Sitzung.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession-Klasse Remotedesktopdienste
- Win32_VirtualDesktopSession Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475450"
---
# <a name="win32_virtualdesktopsession-class"></a><span data-ttu-id="1fa93-105">Win32 \_ virtualdesktopsession-Klasse</span><span class="sxs-lookup"><span data-stu-id="1fa93-105">Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="1fa93-106">Verwaltet eine virtuelle Desktop Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1fa93-106">Manages a virtual desktop session.</span></span>

<span data-ttu-id="1fa93-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1fa93-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa93-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fa93-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a><span data-ttu-id="1fa93-109">Member</span><span class="sxs-lookup"><span data-stu-id="1fa93-109">Members</span></span>

<span data-ttu-id="1fa93-110">Die Win32-Klasse " **\_ virtualdesktopsession** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1fa93-110">The **Win32\_VirtualDesktopSession** class has these types of members:</span></span>

-   [<span data-ttu-id="1fa93-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1fa93-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1fa93-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fa93-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1fa93-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="1fa93-113">Methods</span></span>

<span data-ttu-id="1fa93-114">Die Win32-Klasse " **\_ virtualdesktopsession** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1fa93-114">The **Win32\_VirtualDesktopSession** class has these methods.</span></span>



| <span data-ttu-id="1fa93-115">Methode</span><span class="sxs-lookup"><span data-stu-id="1fa93-115">Method</span></span>                                                         | <span data-ttu-id="1fa93-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fa93-116">Description</span></span>                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="1fa93-117">**Trennen**</span><span class="sxs-lookup"><span data-stu-id="1fa93-117">**Disconnect**</span></span>](disconnect-win32-virtualdesktopsession.md)   | <span data-ttu-id="1fa93-118">Trennt die virtuelle Desktop Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1fa93-118">Disconnects the virtual desktop session.</span></span><br/>                        |
| [<span data-ttu-id="1fa93-119">**Abmeldung**</span><span class="sxs-lookup"><span data-stu-id="1fa93-119">**Logoff**</span></span>](logoff-win32-virtualdesktopsession.md)           | <span data-ttu-id="1fa93-120">Meldet den Benutzer von der virtuellen Desktop Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="1fa93-120">Logs off the user from the virtual desktop session.</span></span><br/>             |
| [<span data-ttu-id="1fa93-121">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="1fa93-121">**SendMessage**</span></span>](sendmessage-win32-virtualdesktopsession.md) | <span data-ttu-id="1fa93-122">Senden Sie eine Nachricht über die virtuelle Desktop Sitzung an den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1fa93-122">Send a message to the user through the virtual desktop session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1fa93-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fa93-123">Properties</span></span>

<span data-ttu-id="1fa93-124">Die Win32-Klasse " **\_ virtualdesktopsession** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1fa93-124">The **Win32\_VirtualDesktopSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fa93-125">**ClientMachineName**</span><span class="sxs-lookup"><span data-stu-id="1fa93-125">**ClientMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa93-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fa93-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fa93-128">Ruft den Namen des Client Computers ab, der mit der Sitzung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1fa93-128">Gets the name of the client machine that is connected to the session.</span></span>

</dd> <dt>

<span data-ttu-id="1fa93-129">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="1fa93-129">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa93-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fa93-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fa93-132">Ruft den Namen der virtuellen Desktop Sammlung ab, die die virtuelle Maschine hostet.</span><span class="sxs-lookup"><span data-stu-id="1fa93-132">Gets the name of the virtual desktop collection that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1fa93-133">**Connectstate**</span><span class="sxs-lookup"><span data-stu-id="1fa93-133">**ConnectState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa93-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fa93-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fa93-136">Ruft den Status der Verbindung mit der Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="1fa93-136">Gets the state of the connection to the session.</span></span>

</dd> <dt>

<span data-ttu-id="1fa93-137">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="1fa93-137">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa93-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fa93-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fa93-140">Ruft den Domänen Namen des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="1fa93-140">Gets the domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="1fa93-141">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="1fa93-141">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa93-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fa93-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-144">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1fa93-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1fa93-145">Ruft die ID der virtuellen Desktop Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="1fa93-145">Gets the ID of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="1fa93-146">**UserName**</span><span class="sxs-lookup"><span data-stu-id="1fa93-146">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa93-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fa93-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fa93-149">Ruft den Namen des Benutzerkontos ab, das der Sitzung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1fa93-149">Gets the name of the user account that is assigned to the session.</span></span>

</dd> <dt>

<span data-ttu-id="1fa93-150">**VMHostName**</span><span class="sxs-lookup"><span data-stu-id="1fa93-150">**VMHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa93-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fa93-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-153">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1fa93-153">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1fa93-154">Ruft den Namen des Remotedesktop Virtualisierungshostservers ab, der die virtuelle Maschine hostet.</span><span class="sxs-lookup"><span data-stu-id="1fa93-154">Gets the name of the Remote Desktop virtualization host server that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1fa93-155">**VMName**</span><span class="sxs-lookup"><span data-stu-id="1fa93-155">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fa93-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fa93-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fa93-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fa93-158">Ruft den Namen des virtuellen Computers ab, der der Sitzung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1fa93-158">Gets the name of the virtual machine that is assigned to the session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fa93-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fa93-159">Requirements</span></span>



| <span data-ttu-id="1fa93-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fa93-160">Requirement</span></span> | <span data-ttu-id="1fa93-161">Wert</span><span class="sxs-lookup"><span data-stu-id="1fa93-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa93-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fa93-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa93-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1fa93-163">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1fa93-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fa93-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa93-165">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fa93-165">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1fa93-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="1fa93-166">Namespace</span></span><br/>                | <span data-ttu-id="1fa93-167">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="1fa93-167">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1fa93-168">MOF</span><span class="sxs-lookup"><span data-stu-id="1fa93-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fa93-169"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1fa93-169"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fa93-170">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa93-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fa93-171"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa93-171"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1fa93-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fa93-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa93-173">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="1fa93-173">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

