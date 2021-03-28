---
description: Diese Klasse ist die Ereignistyp Klasse für das Auflisten von Verzeichnis-und Verzeichnis Benachrichtigungs Ereignissen. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: FileIo_DirEnum-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977657"
---
# <a name="fileio_direnum-class"></a><span data-ttu-id="8b20c-104">Klasse "fleio \_ direnum"</span><span class="sxs-lookup"><span data-stu-id="8b20c-104">FileIo\_DirEnum class</span></span>

<span data-ttu-id="8b20c-105">Diese Klasse ist die Ereignistyp Klasse für das Auflisten von Verzeichnis-und Verzeichnis Benachrichtigungs Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="8b20c-105">This class is the event type class for the enumerate directory and directory notification events.</span></span>

<span data-ttu-id="8b20c-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="8b20c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b20c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b20c-107">Syntax</span></span>

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="8b20c-108">Member</span><span class="sxs-lookup"><span data-stu-id="8b20c-108">Members</span></span>

<span data-ttu-id="8b20c-109">Die Klasse " **fleio \_ direnum** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8b20c-109">The **FileIo\_DirEnum** class has these types of members:</span></span>

-   [<span data-ttu-id="8b20c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b20c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b20c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b20c-111">Properties</span></span>

<span data-ttu-id="8b20c-112">Die Klasse " **fleio \_ direnum** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8b20c-112">The **FileIo\_DirEnum** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b20c-113">**Fileingedex**</span><span class="sxs-lookup"><span data-stu-id="8b20c-113">**FileIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b20c-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b20c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b20c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-116">Qualifizierer: wmidataid (7)</span><span class="sxs-lookup"><span data-stu-id="8b20c-116">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="8b20c-117">Der Datei Index, von dem die Verzeichnis Enumeration fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b20c-117">File index from which to continue directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="8b20c-118">**Filekey**</span><span class="sxs-lookup"><span data-stu-id="8b20c-118">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b20c-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b20c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b20c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-121">Qualifizierer: wmidataid (4), Zeiger</span><span class="sxs-lookup"><span data-stu-id="8b20c-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8b20c-122">Um den Verzeichnisnamen zu ermitteln, vergleichen Sie den Wert dieser Eigenschaft mit der **FileObject** -Eigenschaft eines [**FileIO- \_ namens**](fileio-name.md) Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="8b20c-122">To determine the directory name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="8b20c-123">**FileName**</span><span class="sxs-lookup"><span data-stu-id="8b20c-123">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b20c-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8b20c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b20c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-126">Qualifizierer: wmidataid (8), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="8b20c-126">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="8b20c-127">Für die verzeichnisenumeration festgelegtes Muster.</span><span class="sxs-lookup"><span data-stu-id="8b20c-127">Pattern specified for directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="8b20c-128">**File Object**</span><span class="sxs-lookup"><span data-stu-id="8b20c-128">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b20c-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b20c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b20c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-131">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="8b20c-131">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8b20c-132">Ein Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Datei Objektinstanz zwischen Ereignissen zum Erstellen und Schließen von Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8b20c-132">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="8b20c-133">**Infoclass**</span><span class="sxs-lookup"><span data-stu-id="8b20c-133">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b20c-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b20c-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b20c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-136">Qualifizierer: wmidataid (6), Zeiger</span><span class="sxs-lookup"><span data-stu-id="8b20c-136">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8b20c-137">Die Informations Klasse der angeforderten verzeichnisenumeration.</span><span class="sxs-lookup"><span data-stu-id="8b20c-137">Requested directory enumeration information class.</span></span>

</dd> <dt>

<span data-ttu-id="8b20c-138">**Unpptr**</span><span class="sxs-lookup"><span data-stu-id="8b20c-138">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b20c-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b20c-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b20c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-141">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="8b20c-141">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8b20c-142">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="8b20c-142">IO request packet.</span></span> <span data-ttu-id="8b20c-143">Diese Eigenschaft identifiziert die e/a-Aktivität.</span><span class="sxs-lookup"><span data-stu-id="8b20c-143">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="8b20c-144">**Länge**</span><span class="sxs-lookup"><span data-stu-id="8b20c-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b20c-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b20c-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b20c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-147">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="8b20c-147">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="8b20c-148">Größe des Abfrage Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8b20c-148">Size of the query buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8b20c-149">**TTiD**</span><span class="sxs-lookup"><span data-stu-id="8b20c-149">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b20c-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b20c-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8b20c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b20c-152">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="8b20c-152">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8b20c-153">Thread Bezeichner des Threads, der den Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="8b20c-153">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b20c-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b20c-154">Remarks</span></span>

<span data-ttu-id="8b20c-155">Verzeichnisenumerationsereignisse und Verzeichnis Benachrichtigungs Ereignisse werden aufgezeichnet, wenn ein Verzeichnis aufgezählt oder eine Verzeichnis Änderungs Benachrichtigung an registrierte Listener gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b20c-155">Directory enumeration and directory notification events are recorded when a directory is enumerated or a directory change notification is sent to registered listeners, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b20c-156">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8b20c-156">Requirements</span></span>



| <span data-ttu-id="8b20c-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b20c-157">Requirement</span></span> | <span data-ttu-id="8b20c-158">Wert</span><span class="sxs-lookup"><span data-stu-id="8b20c-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8b20c-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b20c-159">Minimum supported client</span></span><br/> | <span data-ttu-id="8b20c-160">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b20c-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8b20c-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b20c-161">Minimum supported server</span></span><br/> | <span data-ttu-id="8b20c-162">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b20c-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b20c-163">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8b20c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b20c-164">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="8b20c-164">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




