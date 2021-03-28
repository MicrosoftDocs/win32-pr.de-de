---
description: Diese Klasse ist die Ereignistyp Klasse für einfache Datei Vorgangs Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: FileIo_SimpleOp-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980361"
---
# <a name="fileio_simpleop-class"></a><span data-ttu-id="c8395-104">Klasse "fleio \_ simpleop"</span><span class="sxs-lookup"><span data-stu-id="c8395-104">FileIo\_SimpleOp class</span></span>

<span data-ttu-id="c8395-105">Diese Klasse ist die Ereignistyp Klasse für einfache Datei Vorgangs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="c8395-105">This class is the event type class for simple file operation events.</span></span>

<span data-ttu-id="c8395-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c8395-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8395-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8395-107">Syntax</span></span>

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a><span data-ttu-id="c8395-108">Member</span><span class="sxs-lookup"><span data-stu-id="c8395-108">Members</span></span>

<span data-ttu-id="c8395-109">Die Klasse " **fleio \_ simpleop** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c8395-109">The **FileIo\_SimpleOp** class has these types of members:</span></span>

-   [<span data-ttu-id="c8395-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8395-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8395-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c8395-111">Properties</span></span>

<span data-ttu-id="c8395-112">Die Klasse " **fleio \_ simpleop** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c8395-112">The **FileIo\_SimpleOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8395-113">**Filekey**</span><span class="sxs-lookup"><span data-stu-id="c8395-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8395-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8395-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8395-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8395-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8395-116">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="c8395-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c8395-117">Um den Dateinamen zu ermitteln, vergleichen Sie den Wert dieser Eigenschaft mit der **FileObject** -Eigenschaft eines [**FileIO- \_ namens**](fileio-name.md) Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="c8395-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="c8395-118">**File Object**</span><span class="sxs-lookup"><span data-stu-id="c8395-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8395-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8395-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8395-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8395-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8395-121">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="c8395-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c8395-122">Ein Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Datei Objektinstanz zwischen Ereignissen zum Erstellen und Schließen von Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c8395-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="c8395-123">**Unpptr**</span><span class="sxs-lookup"><span data-stu-id="c8395-123">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8395-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8395-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8395-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8395-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8395-126">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="c8395-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c8395-127">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="c8395-127">IO request packet.</span></span> <span data-ttu-id="c8395-128">Diese Eigenschaft identifiziert die e/a-Aktivität.</span><span class="sxs-lookup"><span data-stu-id="c8395-128">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="c8395-129">**TTiD**</span><span class="sxs-lookup"><span data-stu-id="c8395-129">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8395-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c8395-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c8395-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c8395-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8395-132">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="c8395-132">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c8395-133">Thread Bezeichner des Threads, der den Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="c8395-133">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8395-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8395-134">Remarks</span></span>

<span data-ttu-id="c8395-135">Das Bereinigungs Ereignis wird protokolliert, wenn das letzte Handle der Datei geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c8395-135">The Cleanup event is logged when the last handle to the file is closed.</span></span> <span data-ttu-id="c8395-136">Das Close-Ereignis gibt an, dass ein Datei Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c8395-136">The Close event specifies that a file object is being freed.</span></span> <span data-ttu-id="c8395-137">Das Flush-Ereignis gibt an, wann die Datei Puffer vollständig auf den Datenträger geleert werden.</span><span class="sxs-lookup"><span data-stu-id="c8395-137">The Flush event specifies when the file buffers are fully flushed to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8395-138">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c8395-138">Requirements</span></span>



| <span data-ttu-id="c8395-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8395-139">Requirement</span></span> | <span data-ttu-id="c8395-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c8395-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c8395-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8395-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c8395-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8395-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c8395-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8395-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c8395-144">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8395-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8395-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8395-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8395-146">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="c8395-146">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




