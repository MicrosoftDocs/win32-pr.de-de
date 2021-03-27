---
description: Diese Klasse ist die Ereignistyp Klasse für das Datei Informations Ereignis. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: FileIo_Info-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980369"
---
# <a name="fileio_info-class"></a><span data-ttu-id="5fa51-104">Klasse "fleio \_ Info"</span><span class="sxs-lookup"><span data-stu-id="5fa51-104">FileIo\_Info class</span></span>

<span data-ttu-id="5fa51-105">Diese Klasse ist die Ereignistyp Klasse für das Datei Informations Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5fa51-105">This class is the event type class for file information event.</span></span>

<span data-ttu-id="5fa51-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="5fa51-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa51-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fa51-107">Syntax</span></span>

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a><span data-ttu-id="5fa51-108">Member</span><span class="sxs-lookup"><span data-stu-id="5fa51-108">Members</span></span>

<span data-ttu-id="5fa51-109">Die Klasse " **fleio \_ Info** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5fa51-109">The **FileIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="5fa51-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fa51-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fa51-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fa51-111">Properties</span></span>

<span data-ttu-id="5fa51-112">Die Klasse " **fleio \_ Info** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5fa51-112">The **FileIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fa51-113">**ExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="5fa51-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fa51-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fa51-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fa51-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-116">Qualifizierer: wmidataid (5), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5fa51-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5fa51-117">Bei filedispositioninformation-Anforderungen enthält dieses Feld die angeforderte Disposition.</span><span class="sxs-lookup"><span data-stu-id="5fa51-117">For FileDispositionInformation requests, this field contains the requested disposition.</span></span> <span data-ttu-id="5fa51-118">Bei fileendoffileinformation-und filezugecationinformation-Anforderungen enthält dieses Feld die angegebene Dateigröße.</span><span class="sxs-lookup"><span data-stu-id="5fa51-118">For FileEndOfFileInformation and FileAllocationInformation requests, this field contains the specified file size.</span></span>

</dd> <dt>

<span data-ttu-id="5fa51-119">**Filekey**</span><span class="sxs-lookup"><span data-stu-id="5fa51-119">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fa51-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fa51-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fa51-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-122">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5fa51-122">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5fa51-123">Um den Dateinamen zu ermitteln, vergleichen Sie den Wert dieser Eigenschaft mit der **FileObject** -Eigenschaft eines [**FileIO- \_ namens**](fileio-name.md) Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="5fa51-123">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="5fa51-124">**File Object**</span><span class="sxs-lookup"><span data-stu-id="5fa51-124">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fa51-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fa51-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fa51-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-127">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5fa51-127">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5fa51-128">Ein Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Datei Objektinstanz zwischen Ereignissen zum Erstellen und Schließen von Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5fa51-128">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="5fa51-129">**Infoclass**</span><span class="sxs-lookup"><span data-stu-id="5fa51-129">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fa51-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fa51-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fa51-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-132">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="5fa51-132">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="5fa51-133">Die angeforderte Datei Informations Klasse.</span><span class="sxs-lookup"><span data-stu-id="5fa51-133">Requested file information class.</span></span>

</dd> <dt>

<span data-ttu-id="5fa51-134">**Unpptr**</span><span class="sxs-lookup"><span data-stu-id="5fa51-134">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fa51-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fa51-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fa51-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-137">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5fa51-137">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5fa51-138">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="5fa51-138">IO request packet.</span></span> <span data-ttu-id="5fa51-139">Diese Eigenschaft identifiziert die e/a-Aktivität.</span><span class="sxs-lookup"><span data-stu-id="5fa51-139">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="5fa51-140">**TTiD**</span><span class="sxs-lookup"><span data-stu-id="5fa51-140">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fa51-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fa51-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fa51-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa51-143">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5fa51-143">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5fa51-144">Thread Bezeichner des Threads, der den Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="5fa51-144">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5fa51-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fa51-145">Remarks</span></span>

<span data-ttu-id="5fa51-146">Festlegen von Informationen und Abfrage Informations Ereignissen geben an, dass die Dateiattribute festgelegt oder abgefragt wurden.</span><span class="sxs-lookup"><span data-stu-id="5fa51-146">Set information and query information events indicate that the file attributes were set or queried.</span></span> <span data-ttu-id="5fa51-147">Wenn ein FSCTL-Befehl ausgegeben wird, wird ein Ereignis für die Dateisystem Steuerung (fscontrol) aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5fa51-147">A file system control (FSControl) event is recorded when a FSCTL command is issued.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa51-148">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5fa51-148">Requirements</span></span>



| <span data-ttu-id="5fa51-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fa51-149">Requirement</span></span> | <span data-ttu-id="5fa51-150">Wert</span><span class="sxs-lookup"><span data-stu-id="5fa51-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5fa51-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5fa51-151">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa51-152">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5fa51-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5fa51-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5fa51-153">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa51-154">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5fa51-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5fa51-155">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5fa51-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa51-156">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="5fa51-156">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




