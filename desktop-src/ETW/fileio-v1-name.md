---
description: Diese Klasse ist die Ereignistyp Klasse für Datei-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: FileIo_V1_Name-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 617e0abeed095099996079211107d0720017514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042553"
---
# <a name="fileio_v1_name-class"></a><span data-ttu-id="aa43c-104">Namensklasse von "fleio \_ v1" \_</span><span class="sxs-lookup"><span data-stu-id="aa43c-104">FileIo\_V1\_Name class</span></span>

<span data-ttu-id="aa43c-105">Diese Klasse ist die Ereignistyp Klasse für Datei-e/a-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="aa43c-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="aa43c-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="aa43c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa43c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa43c-107">Syntax</span></span>

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="aa43c-108">Member</span><span class="sxs-lookup"><span data-stu-id="aa43c-108">Members</span></span>

<span data-ttu-id="aa43c-109">Die Name-Klasse von " **fleio \_ v1 \_** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aa43c-109">The **FileIo\_V1\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="aa43c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa43c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa43c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa43c-111">Properties</span></span>

<span data-ttu-id="aa43c-112">Die Name-Klasse von " **fleio \_ v1 \_** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa43c-112">The **FileIo\_V1\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa43c-113">FileName</span><span class="sxs-lookup"><span data-stu-id="aa43c-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa43c-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa43c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa43c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa43c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa43c-116">Qualifizierer: wmidataid (2), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="aa43c-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="aa43c-117">Vollständiger Pfad zur Datei, ohne den Laufwerk Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="aa43c-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="aa43c-118">File Object</span><span class="sxs-lookup"><span data-stu-id="aa43c-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa43c-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa43c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa43c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa43c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa43c-121">Qualifizierer: wmidataid (1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="aa43c-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aa43c-122">Vergleichen Sie den Wert dieses Zeigers mit dem **FileObject** -Zeiger Wert in einem [**diskio \_ TypeGroup1**](diskio-typegroup1.md) -Ereignis, um den Typ des e/a-Vorgangs zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="aa43c-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa43c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa43c-123">Remarks</span></span>

<span data-ttu-id="aa43c-124">**Windows Server 2003:** Zum Abrufen des Laufwerk Buchstabens für den Dateinamen Pfad verwenden Sie den **FileObject** -Eigenschafts Wert, um dem entsprechenden [diskio \_ TypeGroup1](diskio-typegroup1.md) -Ereignis zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="aa43c-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="aa43c-125">Verwenden Sie aus dem diskio \_ TypeGroup1-Ereignis **die disknumber** -und **Byteoffset** -Eigenschaftswerte, um das entsprechende [SystemConfig \_ logdisk](systemconfig-logdisk.md) -Ereignis zuzuordnen (**Byteoffset** wird **Startoffset** zugeordnet).</span><span class="sxs-lookup"><span data-stu-id="aa43c-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="aa43c-126">Die " **driveletterstring** "-Eigenschaft enthält den Laufwerk Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="aa43c-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa43c-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aa43c-127">Requirements</span></span>



| <span data-ttu-id="aa43c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa43c-128">Requirement</span></span> | <span data-ttu-id="aa43c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="aa43c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa43c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa43c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aa43c-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa43c-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="aa43c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa43c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aa43c-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa43c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa43c-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa43c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa43c-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="aa43c-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




