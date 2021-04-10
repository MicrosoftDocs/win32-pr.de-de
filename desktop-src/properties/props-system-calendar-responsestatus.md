---
description: Speichert den Status der Antworten eines Benutzers auf Besprechungen im Kalender.
ms.assetid: 5cbc0306-20c7-4f12-bb8b-3889b93dfd69
title: System. Calendar. Response Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af8f69d177dba751ead02a0ee71f5ea4a42ae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131096"
---
# <a name="systemcalendarresponsestatus"></a><span data-ttu-id="fbaad-103">System. Calendar. Response Status</span><span class="sxs-lookup"><span data-stu-id="fbaad-103">System.Calendar.ResponseStatus</span></span>

<span data-ttu-id="fbaad-104">Speichert den Status der Antworten eines Benutzers auf Besprechungen im Kalender.</span><span class="sxs-lookup"><span data-stu-id="fbaad-104">Stores the status of a user's responses to meetings in the calendar.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="fbaad-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbaad-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Calendar.ResponseStatus
   shellPKey = PKEY_Calendar_ResponseStatus
   formatID = 188C1F91-3C40-4132-9EC5-D8B03B72A8A2
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0
            text = None
            defineToken = CALENDAR_RESPONSESTATUS_NONE
         enum
            name = Organized
            value = 1
            text = Organized
            defineToken = CALENDAR_RESPONSESTATUS_ORGANIZED
         enum
            name = Tentative
            value = 2
            text = Tentative
            defineToken = CALENDAR_RESPONSESTATUS_TENTATIVE
         enum
            name = Accepted
            value = 3
            text = Accepted
            defineToken = CALENDAR_RESPONSESTATUS_ACCEPTED
         enum
            name = Declined
            value = 4
            text = Declined
            defineToken = CALENDAR_RESPONSESTATUS_DECLINED
         enum
            name = NotResponded
            value = 5
            text = Not Responded
            defineToken = CALENDAR_RESPONSESTATUS_NOTRESPONDED
```

## <a name="windows-vista"></a><span data-ttu-id="fbaad-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbaad-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Calendar.ResponseStatus
   shellPKey = PKEY_Calendar_ResponseStatus
   formatID = 188C1F91-3C40-4132-9EC5-D8B03B72A8A2
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = None
            defineName = CALENDAR_RESPONSESTATUS_NONE
         enum
            value = 1
            text = Organized
            defineName = CALENDAR_RESPONSESTATUS_ORGANIZED
         enum
            value = 2
            text = Tentative
            defineName = CALENDAR_RESPONSESTATUS_TENTATIVE
         enum
            value = 3
            text = Accepted
            defineName = CALENDAR_RESPONSESTATUS_ACCEPTED
         enum
            value = 4
            text = Declined
            defineName = CALENDAR_RESPONSESTATUS_DECLINED
         enum
            value = 5
            text = Not Responded
            defineName = CALENDAR_RESPONSESTATUS_NOTRESPONDED
```

## <a name="remarks"></a><span data-ttu-id="fbaad-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbaad-107">Remarks</span></span>

<span data-ttu-id="fbaad-108">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="fbaad-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbaad-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fbaad-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbaad-110">propertydescription</span><span class="sxs-lookup"><span data-stu-id="fbaad-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fbaad-111">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="fbaad-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fbaad-112">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="fbaad-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fbaad-113">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="fbaad-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fbaad-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="fbaad-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fbaad-115">StringFormat</span><span class="sxs-lookup"><span data-stu-id="fbaad-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fbaad-116">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="fbaad-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fbaad-117">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="fbaad-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fbaad-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fbaad-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fbaad-119">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="fbaad-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fbaad-120">DrawControl</span><span class="sxs-lookup"><span data-stu-id="fbaad-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fbaad-121">editcontrol</span><span class="sxs-lookup"><span data-stu-id="fbaad-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fbaad-122">FilterControl</span><span class="sxs-lookup"><span data-stu-id="fbaad-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fbaad-123">querycontrol</span><span class="sxs-lookup"><span data-stu-id="fbaad-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
