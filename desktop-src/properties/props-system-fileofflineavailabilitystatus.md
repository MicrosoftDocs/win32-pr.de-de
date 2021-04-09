---
description: NULL gibt den Normalfall an (die Datei ist offline verfügbar). Der partielle Fall gilt nur für Ordner, in denen einige Inhalte möglicherweise offline verfügbar sind, andere jedoch nicht.
ms.assetid: 46b03632-702e-46df-8204-33ada85adbee
title: System. fileofflineavailabilitystatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ca5c3f004c89cfb7b8625f9eb939a42f7fe842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865559"
---
# <a name="systemfileofflineavailabilitystatus"></a><span data-ttu-id="188e5-104">System. fileofflineavailabilitystatus</span><span class="sxs-lookup"><span data-stu-id="188e5-104">System.FileOfflineAvailabilityStatus</span></span>

<span data-ttu-id="188e5-105">NULL gibt den Normalfall an (die Datei ist offline verfügbar).</span><span class="sxs-lookup"><span data-stu-id="188e5-105">Null indicates the normal case (file is available offline).</span></span> <span data-ttu-id="188e5-106">Der partielle Fall gilt nur für Ordner, in denen einige Inhalte möglicherweise offline verfügbar sind, andere jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="188e5-106">The partial case is only for folders where some content may be available offline and some may not.</span></span>

## <a name="windows-10-version-1703"></a><span data-ttu-id="188e5-107">Windows 10, Version 1703</span><span class="sxs-lookup"><span data-stu-id="188e5-107">Windows 10, version 1703</span></span>

```
propertyDescription
   name = System.FileOfflineAvailabilityStatus
   shellPKey = PKEY_FileOfflineAvailabilityStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailableOffline
            value = 0
            text = NotAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_NOTAVAILABLEOFFLINE
         enum
            name = PartiallyAvailableOffline
            value = 1
            text = PartiallyAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PARTIAL
         enum
            name = Complete
            value = 2
            text = Complete
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_COMPLETE
         enum
            name = CompletePinned
            value = 3
            text = CompletePinned
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_COMPLETE_PINNED
         enum
            name = Excluded
            value = 4
            text = Excluded
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_EXCLUDED
         enum
            name = Empty
            value = 5
            text = Empty
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_FOLDER_EMPTY
```

## <a name="windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="188e5-108">Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="188e5-108">Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.FileOfflineAvailabilityStatus
   shellPKey = PKEY_FileOfflineAvailabilityStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailableOffline
            value = 0
            text = NotAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PROP_NOTAVAILABLEOFFLINE
         enum
            name = PartiallyAvailableOffline
            value = 1
            text = PartiallyAvailableOffline
            defineToken = FILEOFFLINEAVAILABILITYSTATUS_PROP_PARTIALLYAVAILABLEOFFLINE
```

## <a name="remarks"></a><span data-ttu-id="188e5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="188e5-109">Remarks</span></span>

<span data-ttu-id="188e5-110">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="188e5-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="188e5-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="188e5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="188e5-112">propertydescription</span><span class="sxs-lookup"><span data-stu-id="188e5-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="188e5-113">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="188e5-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="188e5-114">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="188e5-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="188e5-115">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="188e5-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="188e5-116">Display Info</span><span class="sxs-lookup"><span data-stu-id="188e5-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="188e5-117">StringFormat</span><span class="sxs-lookup"><span data-stu-id="188e5-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="188e5-118">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="188e5-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="188e5-119">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="188e5-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="188e5-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="188e5-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="188e5-121">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="188e5-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="188e5-122">DrawControl</span><span class="sxs-lookup"><span data-stu-id="188e5-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="188e5-123">editcontrol</span><span class="sxs-lookup"><span data-stu-id="188e5-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="188e5-124">FilterControl</span><span class="sxs-lookup"><span data-stu-id="188e5-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="188e5-125">querycontrol</span><span class="sxs-lookup"><span data-stu-id="188e5-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
