---
description: Diese Klasse ist die Ereignistyp Klasse für Lese-und Schreib Ereignisse von Dateien. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: FileIo_ReadWrite-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980368"
---
# <a name="fileio_readwrite-class"></a><span data-ttu-id="1543a-104">Klasse von "fleio" \_</span><span class="sxs-lookup"><span data-stu-id="1543a-104">FileIo\_ReadWrite class</span></span>

<span data-ttu-id="1543a-105">Diese Klasse ist die Ereignistyp Klasse für Lese-und Schreib Ereignisse von Dateien.</span><span class="sxs-lookup"><span data-stu-id="1543a-105">This class is the event type class for file read and write events.</span></span>

<span data-ttu-id="1543a-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1543a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1543a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1543a-107">Syntax</span></span>

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a><span data-ttu-id="1543a-108">Member</span><span class="sxs-lookup"><span data-stu-id="1543a-108">Members</span></span>

<span data-ttu-id="1543a-109">Die " **fleio \_** "-Klasse "Read Write" enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1543a-109">The **FileIo\_ReadWrite** class has these types of members:</span></span>

-   [<span data-ttu-id="1543a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1543a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1543a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1543a-111">Properties</span></span>

<span data-ttu-id="1543a-112">Die " **fleio"- \_ /schreibklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1543a-112">The **FileIo\_ReadWrite** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1543a-113">**Filekey**</span><span class="sxs-lookup"><span data-stu-id="1543a-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1543a-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1543a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1543a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1543a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1543a-116">Qualifizierer: wmidataid (5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="1543a-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1543a-117">Um den Dateinamen zu ermitteln, vergleichen Sie den Wert dieser Eigenschaft mit der **FileObject** -Eigenschaft eines [**FileIO- \_ namens**](fileio-name.md) Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="1543a-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="1543a-118">**File Object**</span><span class="sxs-lookup"><span data-stu-id="1543a-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1543a-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1543a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1543a-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1543a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1543a-121">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="1543a-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1543a-122">Ein Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Datei Objektinstanz zwischen Ereignissen zum Erstellen und Schließen von Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1543a-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="1543a-123">**Ioflags**</span><span class="sxs-lookup"><span data-stu-id="1543a-123">**IoFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1543a-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1543a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1543a-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1543a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1543a-126">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="1543a-126">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="1543a-127">Für diesen Vorgang angegebene e/a-Anforderungs Paketflags.</span><span class="sxs-lookup"><span data-stu-id="1543a-127">IO request packet flags specified for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="1543a-128">**Iosize**</span><span class="sxs-lookup"><span data-stu-id="1543a-128">**IoSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1543a-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1543a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1543a-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1543a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1543a-131">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="1543a-131">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="1543a-132">Anzahl der angeforderten Bytes.</span><span class="sxs-lookup"><span data-stu-id="1543a-132">Number of bytes requested.</span></span>

</dd> <dt>

<span data-ttu-id="1543a-133">**Unpptr**</span><span class="sxs-lookup"><span data-stu-id="1543a-133">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1543a-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1543a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1543a-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1543a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1543a-136">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="1543a-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1543a-137">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="1543a-137">IO request packet.</span></span> <span data-ttu-id="1543a-138">Diese Eigenschaft identifiziert die e/a-Aktivität.</span><span class="sxs-lookup"><span data-stu-id="1543a-138">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="1543a-139">**Offset**</span><span class="sxs-lookup"><span data-stu-id="1543a-139">**Offset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1543a-140">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1543a-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1543a-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1543a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1543a-142">Qualifizierer: wmidataid (1)</span><span class="sxs-lookup"><span data-stu-id="1543a-142">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="1543a-143">Der Dateioffset für den angeforderten Vorgang wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="1543a-143">Starting file offset for the requested operation.</span></span>

</dd> <dt>

<span data-ttu-id="1543a-144">**TTiD**</span><span class="sxs-lookup"><span data-stu-id="1543a-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1543a-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1543a-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1543a-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1543a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1543a-147">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="1543a-147">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1543a-148">Thread Bezeichner des Threads, der den Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="1543a-148">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1543a-149">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1543a-149">Requirements</span></span>



| <span data-ttu-id="1543a-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1543a-150">Requirement</span></span> | <span data-ttu-id="1543a-151">Wert</span><span class="sxs-lookup"><span data-stu-id="1543a-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1543a-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1543a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1543a-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1543a-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1543a-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1543a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1543a-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1543a-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1543a-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1543a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1543a-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="1543a-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




