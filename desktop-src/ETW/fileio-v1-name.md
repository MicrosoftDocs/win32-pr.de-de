---
description: 'FileIo_V1_Name Klasse: Diese Klasse ist die Ereignistypklasse für Datei-E/A-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: 62069f8a462499dfbfd9cfa368b9f5985d4775e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106548"
---
# <a name="fileio_v1_name-class"></a><span data-ttu-id="ce0e3-104">FileIo \_ V1 \_ Name-Klasse</span><span class="sxs-lookup"><span data-stu-id="ce0e3-104">FileIo\_V1\_Name class</span></span>

<span data-ttu-id="ce0e3-105">Diese Klasse ist die Ereignistypklasse für Datei-E/A-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="ce0e3-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="ce0e3-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ce0e3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0e3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce0e3-107">Syntax</span></span>

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="ce0e3-108">Member</span><span class="sxs-lookup"><span data-stu-id="ce0e3-108">Members</span></span>

<span data-ttu-id="ce0e3-109">Die **FileIo \_ V1 \_ Name-Klasse** verfügt über die folgenden Membertypen:</span><span class="sxs-lookup"><span data-stu-id="ce0e3-109">The **FileIo\_V1\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="ce0e3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce0e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce0e3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce0e3-111">Properties</span></span>

<span data-ttu-id="ce0e3-112">Die **FileIo \_ V1 \_ Name-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ce0e3-112">The **FileIo\_V1\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce0e3-113">FileName</span><span class="sxs-lookup"><span data-stu-id="ce0e3-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce0e3-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce0e3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce0e3-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce0e3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce0e3-116">Qualifizierer: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="ce0e3-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="ce0e3-117">Vollständiger Pfad zur Datei, ohne den Laufwerkbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="ce0e3-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="ce0e3-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="ce0e3-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce0e3-119">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ce0e3-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce0e3-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce0e3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce0e3-121">Qualifizierer: WmiDataId(1), Zeiger</span><span class="sxs-lookup"><span data-stu-id="ce0e3-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ce0e3-122">Übereinstimmung mit dem Wert dieses Zeigers auf den **FileObject-Zeigerwert** in einem [**DiskIo \_ TypeGroup1-Ereignis,**](diskio-typegroup1.md) um den Typ des E/A-Vorgangs zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="ce0e3-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce0e3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce0e3-123">Remarks</span></span>

<span data-ttu-id="ce0e3-124">**Windows Server 2003:** Um den Laufwerkbuchstaben für den Dateinamenpfad abzurufen, verwenden Sie den **FileObject-Eigenschaftswert,** um dem entsprechenden [DiskIo \_ TypeGroup1-Ereignis zu](diskio-typegroup1.md) zuordnen.</span><span class="sxs-lookup"><span data-stu-id="ce0e3-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="ce0e3-125">Verwenden Sie aus dem DiskIo \_ TypeGroup1-Ereignis die **Eigenschaftswerte DiskNumber** und **ByteOffset,** um dem entsprechenden [SystemConfig \_ LogDisk-Ereignis](systemconfig-logdisk.md) **(ByteOffset** wird **StartOffset** zu zuordnen).</span><span class="sxs-lookup"><span data-stu-id="ce0e3-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="ce0e3-126">Die **DriveLetterString-Eigenschaft** enthält den Laufwerkbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="ce0e3-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce0e3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce0e3-127">Requirements</span></span>



| <span data-ttu-id="ce0e3-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce0e3-128">Requirement</span></span> | <span data-ttu-id="ce0e3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ce0e3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce0e3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce0e3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ce0e3-131">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce0e3-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ce0e3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce0e3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ce0e3-133">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce0e3-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce0e3-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ce0e3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0e3-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="ce0e3-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




