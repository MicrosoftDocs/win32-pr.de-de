---
description: Zeigt den aktuellen Status des Tasks an.
ms.assetid: 76bb9bb7-3383-4e5a-ae75-a11c40f318e2
title: System. Communication. Taskstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd74f25400093d9719607a718b4d1fc727ff36de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358805"
---
# <a name="systemcommunicationtaskstatus"></a><span data-ttu-id="02757-103">System. Communication. Taskstatus</span><span class="sxs-lookup"><span data-stu-id="02757-103">System.Communication.TaskStatus</span></span>

<span data-ttu-id="02757-104">Zeigt den aktuellen Status des Tasks an.</span><span class="sxs-lookup"><span data-stu-id="02757-104">Indicates the current status of the task.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="02757-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="02757-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Communication.TaskStatus
   shellPKey = PKEY_Communication_TaskStatus
   formatID = BE1A72C6-9A1D-46B7-AFE7-AFAF8CEF4999
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotStarted
            value = 0
            text = Not Started
            defineToken = TASKSTATUS_NOTSTARTED
         enum
            name = InProgress
            value = 1
            text = In Progress
            defineToken = TASKSTATUS_INPROGRESS
         enum
            name = Complete
            value = 2
            text = Complete
            defineToken = TASKSTATUS_COMPLETE
         enum
            name = Waiting
            value = 3
            text = Waiting
            defineToken = TASKSTATUS_WAITING
         enum
            name = Deferred
            value = 4
            text = Deferred
            defineToken = TASKSTATUS_DEFERRED
```

## <a name="windows-vista"></a><span data-ttu-id="02757-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02757-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Communication.TaskStatus
   shellPKey = PKEY_Communication_TaskStatus
   formatID = BE1A72C6-9A1D-46B7-AFE7-AFAF8CEF4999
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
            text = Not Started
            defineName = TASKSTATUS_NOTSTARTED
         enum
            value = 1
            text = In Progress
            defineName = TASKSTATUS_INPROGRESS
         enum
            value = 2
            text = Complete
            defineName = TASKSTATUS_COMPLETE
         enum
            value = 3
            text = Waiting
            defineName = TASKSTATUS_WAITING
         enum
            value = 4
            text = Deferred
            defineName = TASKSTATUS_DEFERRED
```

## <a name="remarks"></a><span data-ttu-id="02757-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02757-107">Remarks</span></span>

<span data-ttu-id="02757-108">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="02757-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02757-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02757-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02757-110">propertydescription</span><span class="sxs-lookup"><span data-stu-id="02757-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="02757-111">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="02757-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="02757-112">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="02757-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="02757-113">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="02757-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="02757-114">Display Info</span><span class="sxs-lookup"><span data-stu-id="02757-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="02757-115">StringFormat</span><span class="sxs-lookup"><span data-stu-id="02757-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="02757-116">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="02757-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="02757-117">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="02757-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="02757-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="02757-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="02757-119">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="02757-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="02757-120">DrawControl</span><span class="sxs-lookup"><span data-stu-id="02757-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="02757-121">editcontrol</span><span class="sxs-lookup"><span data-stu-id="02757-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="02757-122">FilterControl</span><span class="sxs-lookup"><span data-stu-id="02757-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="02757-123">querycontrol</span><span class="sxs-lookup"><span data-stu-id="02757-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
