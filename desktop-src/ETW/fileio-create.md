---
description: Diese Klasse ist die Ereignistyp Klasse für das file Create-Ereignis. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: FileIo_Create-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977664"
---
# <a name="fileio_create-class"></a><span data-ttu-id="5eb2d-104">\_Klasse "Klasse erstellen"</span><span class="sxs-lookup"><span data-stu-id="5eb2d-104">FileIo\_Create class</span></span>

<span data-ttu-id="5eb2d-105">Diese Klasse ist die Ereignistyp Klasse für das file Create-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-105">This class is the event type class for the file create event.</span></span>

<span data-ttu-id="5eb2d-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5eb2d-107">Syntax</span></span>

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a><span data-ttu-id="5eb2d-108">Member</span><span class="sxs-lookup"><span data-stu-id="5eb2d-108">Members</span></span>

<span data-ttu-id="5eb2d-109">Die Klasse "Klasse **\_ Erstellen** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5eb2d-109">The **FileIo\_Create** class has these types of members:</span></span>

-   [<span data-ttu-id="5eb2d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5eb2d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5eb2d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5eb2d-111">Properties</span></span>

<span data-ttu-id="5eb2d-112">Die Klasse "Klasse **\_ Erstellen** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-112">The **FileIo\_Create** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5eb2d-113">**"Kreateoptions"**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-113">**CreateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb2d-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5eb2d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-116">Qualifizierer: wmidataid (4)</span><span class="sxs-lookup"><span data-stu-id="5eb2d-116">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="5eb2d-117">Werte, die in den Parametern "up *options* " und " *deedispositionen* " an die Funktion " [**ntkreatefile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-117">Values passed in the *CreateOptions* and *CreateDispositions* parameters to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2d-118">**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-118">**FileAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb2d-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5eb2d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-121">Qualifizierer: wmidataid (5)</span><span class="sxs-lookup"><span data-stu-id="5eb2d-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="5eb2d-122">Der Wert, der im *FileAttribute* -Parameter an die [**ntkreatefile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-122">Value passed in the *FileAttributes* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2d-123">**File Object**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb2d-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5eb2d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-126">Qualifizierer: wmidataid (3), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5eb2d-126">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5eb2d-127">Ein Bezeichner, der zum Korrelieren von Vorgängen mit derselben geöffneten Datei Objektinstanz zwischen Ereignissen zum Erstellen und Schließen von Dateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-127">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2d-128">**Unpptr**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-128">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb2d-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5eb2d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-131">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5eb2d-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5eb2d-132">E/a-Anforderungspaket.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-132">IO request packet.</span></span> <span data-ttu-id="5eb2d-133">Diese Eigenschaft identifiziert die e/a-Aktivität.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-133">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2d-134">**OpenPath**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-134">**OpenPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb2d-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5eb2d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-137">Qualifizierer: wmidataid (7), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="5eb2d-137">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5eb2d-138">Pfad zur Datei.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-138">Path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2d-139">**ShareAccess**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-139">**ShareAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb2d-140">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5eb2d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-142">Qualifizierer: wmidataid (6)</span><span class="sxs-lookup"><span data-stu-id="5eb2d-142">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="5eb2d-143">Der Wert, der im *share Access* -Parameter an die [**ntkreatefile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-143">Value passed in the *ShareAccess* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="5eb2d-144">**TTiD**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5eb2d-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5eb2d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5eb2d-147">Qualifizierer: wmidataid (2), Zeiger</span><span class="sxs-lookup"><span data-stu-id="5eb2d-147">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5eb2d-148">Thread Bezeichner des Threads, der die Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="5eb2d-148">Thread identifier of the thread that is creating the file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5eb2d-149">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5eb2d-149">Requirements</span></span>



| <span data-ttu-id="5eb2d-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5eb2d-150">Requirement</span></span> | <span data-ttu-id="5eb2d-151">Wert</span><span class="sxs-lookup"><span data-stu-id="5eb2d-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5eb2d-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5eb2d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="5eb2d-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eb2d-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5eb2d-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5eb2d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="5eb2d-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5eb2d-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5eb2d-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5eb2d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb2d-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="5eb2d-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 
