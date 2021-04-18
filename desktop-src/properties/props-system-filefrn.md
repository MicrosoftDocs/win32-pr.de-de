---
description: Die eindeutige Datei-ID (auch als Datei Verweis Nummer bezeichnet).
ms.assetid: 65189671-1b55-4933-9dee-a120b38caa98
title: System. filefrn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aa536e0cdda3f42fd9e03315156716ef499c5f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358979"
---
# <a name="systemfilefrn"></a><span data-ttu-id="2a676-103">System. filefrn</span><span class="sxs-lookup"><span data-stu-id="2a676-103">System.FileFRN</span></span>

<span data-ttu-id="2a676-104">Die eindeutige Datei-ID (auch als Datei Verweis Nummer bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="2a676-104">The unique file ID, also known as the File Reference Number.</span></span> <span data-ttu-id="2a676-105">Für eine angegebene Datei ist dies der gleiche Wert wie der **fileid** -Member der [**Datei- \_ ID \_ both \_ - \_ Info**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) -Struktur, die durch einen Aufruf von [**getfileinformationbylenker Ex**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2a676-105">For a given file, this is the same value as the **FileId** member of the [**FILE\_ID\_BOTH\_DIR\_INFO**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) structure, which is obtained by a call to [**GetFileInformationByHandleEx**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="2a676-106">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a676-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileFRN
   shellPKey = PKEY_FileFRN
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 21
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="2a676-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a676-107">Remarks</span></span>

<span data-ttu-id="2a676-108">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="2a676-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a676-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a676-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a676-110">propertydescription</span><span class="sxs-lookup"><span data-stu-id="2a676-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2a676-111">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="2a676-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2a676-112">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="2a676-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2a676-113">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="2a676-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2a676-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="2a676-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2a676-115">StringFormat</span><span class="sxs-lookup"><span data-stu-id="2a676-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2a676-116">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="2a676-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2a676-117">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="2a676-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2a676-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2a676-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2a676-119">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="2a676-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2a676-120">DrawControl</span><span class="sxs-lookup"><span data-stu-id="2a676-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2a676-121">editcontrol</span><span class="sxs-lookup"><span data-stu-id="2a676-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2a676-122">FilterControl</span><span class="sxs-lookup"><span data-stu-id="2a676-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2a676-123">querycontrol</span><span class="sxs-lookup"><span data-stu-id="2a676-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
