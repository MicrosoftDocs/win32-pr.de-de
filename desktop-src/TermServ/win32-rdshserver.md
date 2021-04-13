---
title: Win32_RDSHServer-Klasse
description: Verwaltet einen Remotedesktop-Sitzungshost Server (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer-Klasse Remotedesktopdienste
- Win32_RDSHServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340718"
---
# <a name="win32_rdshserver-class"></a><span data-ttu-id="66fad-105">Win32 \_ rdshserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="66fad-105">Win32\_RDSHServer class</span></span>

<span data-ttu-id="66fad-106">Verwaltet einen Remotedesktop-Sitzungshost Server (RDSH).</span><span class="sxs-lookup"><span data-stu-id="66fad-106">Manages a Remote Desktop Session Host (RDSH) server.</span></span>

<span data-ttu-id="66fad-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="66fad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66fad-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="66fad-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a><span data-ttu-id="66fad-109">Member</span><span class="sxs-lookup"><span data-stu-id="66fad-109">Members</span></span>

<span data-ttu-id="66fad-110">Die **Win32 \_ rdshserver** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="66fad-110">The **Win32\_RDSHServer** class has these types of members:</span></span>

-   [<span data-ttu-id="66fad-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="66fad-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="66fad-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66fad-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="66fad-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="66fad-113">Methods</span></span>

<span data-ttu-id="66fad-114">Die **Win32 \_ rdshserver** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="66fad-114">The **Win32\_RDSHServer** class has these methods.</span></span>



| <span data-ttu-id="66fad-115">Methode</span><span class="sxs-lookup"><span data-stu-id="66fad-115">Method</span></span>                                                                          | <span data-ttu-id="66fad-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66fad-116">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66fad-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="66fad-117">**GetInt32Property**</span></span>](getint32property-win32-rdshserver.md)                   | <span data-ttu-id="66fad-118">Ruft einen ganzzahligen Eigenschafts Wert eines **Win32- \_ rdshserver** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="66fad-118">Retrieves an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="66fad-119">**Getpdingstartserverlist**</span><span class="sxs-lookup"><span data-stu-id="66fad-119">**GetPendingStartServerList**</span></span>](win32-rdshserver-getpendingstartserverlist.md) | <span data-ttu-id="66fad-120">Ruft eine Liste der Server ab, die auf den Start warten.</span><span class="sxs-lookup"><span data-stu-id="66fad-120">Retrieves a list of server waiting to start.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="66fad-121">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="66fad-121">**GetStringProperty**</span></span>](getstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="66fad-122">Ruft den Wert der Zeichen folgen Eigenschaft eines **Win32- \_ rdshserver** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="66fad-122">Retrieves a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="66fad-123">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="66fad-123">**SetInt32Property**</span></span>](setint32property-win32-rdshserver.md)                   | <span data-ttu-id="66fad-124">Aktualisiert einen ganzzahligen Eigenschafts Wert eines **Win32- \_ rdshserver** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="66fad-124">Updates an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="66fad-125">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="66fad-125">**SetStringProperty**</span></span>](setstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="66fad-126">Aktualisiert den Wert der Zeichen folgen Eigenschaft eines **Win32- \_ rdshserver** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="66fad-126">Updates a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="66fad-127">**Testandsetstate**</span><span class="sxs-lookup"><span data-stu-id="66fad-127">**TestAndSetState**</span></span>](win32-rdshserver-testandsetstate.md)                     | <span data-ttu-id="66fad-128">Vergleicht den aktuellen Zustand mit dem angegebenen comparand. Wenn die beiden Stimmen, wird der Zustand auf einen neuen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="66fad-128">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="66fad-129">Unabhängig von der Übereinstimmung wird der aktuelle Zustand ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="66fad-129">Regardless of the match, the current state is also returned.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="66fad-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="66fad-130">Properties</span></span>

<span data-ttu-id="66fad-131">Die **Win32 \_ rdshserver** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="66fad-131">The **Win32\_RDSHServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66fad-132">**Collectionalias**</span><span class="sxs-lookup"><span data-stu-id="66fad-132">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66fad-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="66fad-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66fad-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="66fad-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="66fad-135">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66fad-135">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66fad-136">Ruft den Alias für die RDSH-Auflistung ab, der der RDSH-Server zugewiesen ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="66fad-136">Gets and sets the alias to the RDSH collection to which the RDSH server is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="66fad-137">**Connectionbroker**</span><span class="sxs-lookup"><span data-stu-id="66fad-137">**ConnectionBroker**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66fad-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="66fad-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66fad-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="66fad-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="66fad-140">Ruft den Namen des Remotedesktopverbindung Brokers (RDCB) ab, der den Benutzer Zugriff auf den RDSH-Server verwaltet, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="66fad-140">Gets and sets the name of the Remote Desktop Connection Broker (RDCB) that manages user access to the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="66fad-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="66fad-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66fad-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="66fad-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66fad-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="66fad-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="66fad-144">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="66fad-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="66fad-145">Ruft den Namen des RDSH-Servers ab, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="66fad-145">Gets and sets the name of the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="66fad-146">**ServerState**</span><span class="sxs-lookup"><span data-stu-id="66fad-146">**ServerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66fad-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66fad-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66fad-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="66fad-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66fad-149">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66fad-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66fad-150">Beschreibt den Status des Servers.</span><span class="sxs-lookup"><span data-stu-id="66fad-150">Describes the state of the server.</span></span> <span data-ttu-id="66fad-151">Alle anderen Werte als das Ziel, das ausgeführt wird (3), sind reserviert und sollten einen ungültigen Status **\_ aufweisen** .</span><span class="sxs-lookup"><span data-stu-id="66fad-151">Any value other than **TARGET\_RUNNING** (3) is reserved and should be consider an invalid state.</span></span>

<span data-ttu-id="66fad-152">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="66fad-152">The possible values are.</span></span>

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

<span data-ttu-id="66fad-153">**Ziel \_ Unbekannt** (1)</span><span class="sxs-lookup"><span data-stu-id="66fad-153">**TARGET\_UNKNOWN** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

<span data-ttu-id="66fad-154">**Ziel \_ Wird ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="66fad-154">**TARGET\_RUNNING** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

<span data-ttu-id="66fad-155">**Ziel \_ Ungültig** (8)</span><span class="sxs-lookup"><span data-stu-id="66fad-155">**TARGET\_INVALID** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

<span data-ttu-id="66fad-156">**Ziel \_ Wird gestartet** (9)</span><span class="sxs-lookup"><span data-stu-id="66fad-156">**TARGET\_STARTING** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

<span data-ttu-id="66fad-157">**Ziel \_ Wird beendet (10** )</span><span class="sxs-lookup"><span data-stu-id="66fad-157">**TARGET\_STOPPING** (10)</span></span>


<span data-ttu-id="66fad-158"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="66fad-158"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="66fad-159">**Windows Server 2012 R2 und Windows Server 2012:** Diese Eigenschaft ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66fad-159">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66fad-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66fad-160">Requirements</span></span>



| <span data-ttu-id="66fad-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66fad-161">Requirement</span></span> | <span data-ttu-id="66fad-162">Wert</span><span class="sxs-lookup"><span data-stu-id="66fad-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fad-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66fad-163">Minimum supported client</span></span><br/> | <span data-ttu-id="66fad-164">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="66fad-164">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="66fad-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66fad-165">Minimum supported server</span></span><br/> | <span data-ttu-id="66fad-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66fad-166">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="66fad-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="66fad-167">Namespace</span></span><br/>                | <span data-ttu-id="66fad-168">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="66fad-168">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="66fad-169">MOF</span><span class="sxs-lookup"><span data-stu-id="66fad-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66fad-170"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="66fad-170"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="66fad-171">DLL</span><span class="sxs-lookup"><span data-stu-id="66fad-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66fad-172"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66fad-172"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="66fad-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66fad-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fad-174">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="66fad-174">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

