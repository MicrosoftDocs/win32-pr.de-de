---
title: MSAD_ReplCursor-Klasse
description: Stellt eingehende Replikations Zustandsinformationen zu allen Replikaten eines angegebenen Namens Kontexts (NC) bereit.
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor-Klasse Active Directory
- MSAD_ReplCursor Klasse Active Directory, beschrieben
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476845"
---
# <a name="msad_replcursor-class"></a><span data-ttu-id="58e80-105">MSAD \_ replcursor-Klasse</span><span class="sxs-lookup"><span data-stu-id="58e80-105">MSAD\_ReplCursor class</span></span>

<span data-ttu-id="58e80-106">Stellt eingehende Replikations Zustandsinformationen zu allen Replikaten eines angegebenen Namens Kontexts (NC) bereit.</span><span class="sxs-lookup"><span data-stu-id="58e80-106">Provides inbound replication state information about all replicas of a given naming context (NC).</span></span>

## <a name="syntax"></a><span data-ttu-id="58e80-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="58e80-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a><span data-ttu-id="58e80-108">Member</span><span class="sxs-lookup"><span data-stu-id="58e80-108">Members</span></span>

<span data-ttu-id="58e80-109">Die **MSAD \_ replcursor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="58e80-109">The **MSAD\_ReplCursor** class has these types of members:</span></span>

-   [<span data-ttu-id="58e80-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58e80-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58e80-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58e80-111">Properties</span></span>

<span data-ttu-id="58e80-112">Die **MSAD \_ replcursor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58e80-112">The **MSAD\_ReplCursor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58e80-113">**Namingcontextdn**</span><span class="sxs-lookup"><span data-stu-id="58e80-113">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58e80-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58e80-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="58e80-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58e80-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58e80-116">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58e80-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="58e80-117">Ruft den X. 500-Pfad für den namens Kontext (NC) ab, der diesen Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="58e80-117">Gets the X.500 path for the naming context (NC) that holds this cursor.</span></span>

</dd> <dt>

<span data-ttu-id="58e80-118">**Sourcedsadn**</span><span class="sxs-lookup"><span data-stu-id="58e80-118">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58e80-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58e80-119">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="58e80-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58e80-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58e80-121">Ruft den X. 500-Pfad für den Verzeichnis System-Agent (DSA) ab, der den Quell Domänen Controller (DC) darstellt.</span><span class="sxs-lookup"><span data-stu-id="58e80-121">Gets the X.500 path for the directory system agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="58e80-122">**Sourcedsainvocationid**</span><span class="sxs-lookup"><span data-stu-id="58e80-122">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58e80-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="58e80-123">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="58e80-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58e80-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58e80-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58e80-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="58e80-126">Ruft den Aufruf Bezeichner des Ursprungs Servers ab, **dem der Wert** von "".</span><span class="sxs-lookup"><span data-stu-id="58e80-126">Gets the invocation identifier of the originating server to which the **USNAttributeFilter** corresponds.</span></span>

</dd> <dt>

<span data-ttu-id="58e80-127">**Timeoflastsuccess fulsync**</span><span class="sxs-lookup"><span data-stu-id="58e80-127">**TimeOfLastSuccessfulSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58e80-128">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="58e80-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58e80-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58e80-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58e80-130">Ruft den Zeitstempel der letzten erfolgreichen Replikations Synchronisierung mit der Quell-DSA ab.</span><span class="sxs-lookup"><span data-stu-id="58e80-130">Gets the timestamp of the last successful replication sync with the source DSA.</span></span> <span data-ttu-id="58e80-131">Gibt den Zeitpunkt an, zu dem dieser Domänen Controller zuletzt Änderungen am Quell-DSA für diesen NC feststellte.</span><span class="sxs-lookup"><span data-stu-id="58e80-131">Indicates the time when this DC last saw changes made on the source DSA for this NC.</span></span>

</dd> <dt>

<span data-ttu-id="58e80-132">**"", "".**</span><span class="sxs-lookup"><span data-stu-id="58e80-132">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58e80-133">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58e80-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58e80-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="58e80-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58e80-135">Ruft die maximale Update Sequenznummer ab, auf die der Zielserver angeben kann, dass alle Änderungen, die vom angegebenen Server stammen, in den Update Sequenznummern, die kleiner oder gleich dieser Update Sequenznummer sind, aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="58e80-135">Gets the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number.</span></span> <span data-ttu-id="58e80-136">Diese Eigenschaft wird zum Filtern von Änderungen verwendet, die der Zielserver bereits auf Replikations Quell Servern angewendet hat.</span><span class="sxs-lookup"><span data-stu-id="58e80-136">This property is used to filter changes that the destination server has already applied at replication source servers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58e80-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58e80-137">Requirements</span></span>



| <span data-ttu-id="58e80-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58e80-138">Requirement</span></span> | <span data-ttu-id="58e80-139">Wert</span><span class="sxs-lookup"><span data-stu-id="58e80-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58e80-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58e80-140">Minimum supported client</span></span><br/> | <span data-ttu-id="58e80-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="58e80-141">None supported</span></span><br/>                                                               |
| <span data-ttu-id="58e80-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58e80-142">Minimum supported server</span></span><br/> | <span data-ttu-id="58e80-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58e80-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58e80-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="58e80-144">Namespace</span></span><br/>                | <span data-ttu-id="58e80-145">\\Microsoftactivedirectory-Stammverzeichnis</span><span class="sxs-lookup"><span data-stu-id="58e80-145">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="58e80-146">MOF</span><span class="sxs-lookup"><span data-stu-id="58e80-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58e80-147"><dt>ReplProv. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="58e80-147"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="58e80-148">DLL</span><span class="sxs-lookup"><span data-stu-id="58e80-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e80-149"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e80-149"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e80-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58e80-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e80-151">**DS- \_ repl- \_ Cursor**</span><span class="sxs-lookup"><span data-stu-id="58e80-151">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

