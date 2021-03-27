---
description: Die Klasse "fleio \_ v0 \_ Name" ist eine ältere Version der Ereignistyp Klasse für Datei-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: FileIo_V0_Name-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758425"
---
# <a name="fileio_v0_name-class"></a><span data-ttu-id="50e75-104">Klasse "fleio \_ v0 \_ Name"</span><span class="sxs-lookup"><span data-stu-id="50e75-104">FileIo\_V0\_Name class</span></span>

<span data-ttu-id="50e75-105">Die Klasse " **fleio \_ v0 \_ Name** " ist eine ältere Version der Ereignistyp Klasse für Datei-e/a-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="50e75-105">The **FileIo\_V0\_Name** class is an older version of the event type class for file I/O events.</span></span>

<span data-ttu-id="50e75-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="50e75-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e75-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50e75-107">Syntax</span></span>

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="50e75-108">Member</span><span class="sxs-lookup"><span data-stu-id="50e75-108">Members</span></span>

<span data-ttu-id="50e75-109">Die Klasse " **fleio \_ v0 \_ Name** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="50e75-109">The **FileIo\_V0\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="50e75-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50e75-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50e75-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="50e75-111">Properties</span></span>

<span data-ttu-id="50e75-112">Die Klasse " **fleio \_ v0 \_ Name** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="50e75-112">The **FileIo\_V0\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50e75-113">FileName</span><span class="sxs-lookup"><span data-stu-id="50e75-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e75-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="50e75-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50e75-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50e75-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e75-116">Qualifizierer: wmidataid (2), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="50e75-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="50e75-117">Vollständiger Pfad zur Datei, ohne den Laufwerk Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="50e75-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="50e75-118">File Object</span><span class="sxs-lookup"><span data-stu-id="50e75-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50e75-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="50e75-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="50e75-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="50e75-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="50e75-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="50e75-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="50e75-122">Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**diskio \_ TypeGroup1**](diskio-typegroup1.md) -Ereignis, um den Typ des e/a-Vorgangs zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="50e75-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50e75-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50e75-123">Remarks</span></span>

<span data-ttu-id="50e75-124">**Windows Server 2003:** Zum Abrufen des Laufwerk Buchstabens für den Dateinamen Pfad verwenden Sie den **FileObject** -Eigenschafts Wert, um dem entsprechenden [**diskio \_ TypeGroup1**](diskio-typegroup1.md) -Ereignis zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="50e75-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="50e75-125">Verwenden Sie aus dem **diskio \_ TypeGroup1** -Ereignis die **disknumber** -und **Byteoffset** -Eigenschaftswerte, um das entsprechende [**SystemConfig \_ logdisk**](systemconfig-logdisk.md) -Ereignis zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="50e75-125">From the **DiskIo\_TypeGroup1** event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) event.</span></span> <span data-ttu-id="50e75-126">Die " **driveletterstring** "-Eigenschaft enthält den Laufwerk Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="50e75-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e75-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="50e75-127">Requirements</span></span>



| <span data-ttu-id="50e75-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50e75-128">Requirement</span></span> | <span data-ttu-id="50e75-129">Wert</span><span class="sxs-lookup"><span data-stu-id="50e75-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="50e75-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50e75-130">Minimum supported client</span></span><br/> | <span data-ttu-id="50e75-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50e75-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="50e75-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50e75-132">Minimum supported server</span></span><br/> | <span data-ttu-id="50e75-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50e75-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="50e75-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50e75-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e75-135">**"Fleio \_ v0"**</span><span class="sxs-lookup"><span data-stu-id="50e75-135">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> </dl>

 

 




