---
description: Legen Sie diese Eigenschaft für eine Verknüpfung auf (1) fest, um zu verhindern, dass eine Anwendung bei der Installation automatisch an den Start Bildschirm angeheftet wird. oder (2) geben Sie an, dass ein Element Programm gesteuert über eine Benutzeraktion zum Start Programm hinzugefügt wird (was das automatische anheften an Start und DELETE bei unpin impliziert).
ms.assetid: 247ad0a6-ce65-45f1-a0d5-51ad135000aa
title: System. appusermodel. startpinoption
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cdef82a90488ce87bbf182323b00d62a5cdfea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863903"
---
# <a name="systemappusermodelstartpinoption"></a><span data-ttu-id="ab04e-103">System. appusermodel. startpinoption</span><span class="sxs-lookup"><span data-stu-id="ab04e-103">System.AppUserModel.StartPinOption</span></span>

<span data-ttu-id="ab04e-104">Legen Sie diese Eigenschaft für eine Verknüpfung auf (1) fest, um zu verhindern, dass eine Anwendung bei der Installation automatisch an den Start Bildschirm angeheftet wird. oder (2) geben Sie an, dass ein Element Programm gesteuert über eine Benutzeraktion zum Start Programm hinzugefügt wird (was das automatische anheften an Start und DELETE bei unpin impliziert).</span><span class="sxs-lookup"><span data-stu-id="ab04e-104">Set this property on a shortcut to (1) prevent an application from being automatically pinned to Start screen upon installation; or(2) indicate that an item is programmatically added to launcher via user action (which implies automatically pin to Start and delete on unpin).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="ab04e-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="ab04e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.AppUserModel.StartPinOption
   shellPKey = PKEY_AppUserModel_StartPinOption
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = false
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Default
            value = 0
            text = Default
            defineToken = APPUSERMODEL_STARTPINOPTION_DEFAULT
         enum
            name = NoPinOnInstall
            value = 1
            text = NoPinOnInstall
            defineToken = APPUSERMODEL_STARTPINOPTION_NOPINONINSTALL
         enum
            name = UserPinned
            value = 2
            text = UserPinned
            defineToken = APPUSERMODEL_STARTPINOPTION_USERPINNED
```

## <a name="remarks"></a><span data-ttu-id="ab04e-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab04e-106">Remarks</span></span>

<span data-ttu-id="ab04e-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="ab04e-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab04e-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ab04e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab04e-109">propertydescription</span><span class="sxs-lookup"><span data-stu-id="ab04e-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ab04e-110">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="ab04e-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ab04e-111">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="ab04e-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ab04e-112">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="ab04e-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ab04e-113">Display Info</span><span class="sxs-lookup"><span data-stu-id="ab04e-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ab04e-114">StringFormat</span><span class="sxs-lookup"><span data-stu-id="ab04e-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ab04e-115">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="ab04e-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ab04e-116">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="ab04e-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ab04e-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ab04e-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ab04e-118">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="ab04e-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ab04e-119">DrawControl</span><span class="sxs-lookup"><span data-stu-id="ab04e-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ab04e-120">editcontrol</span><span class="sxs-lookup"><span data-stu-id="ab04e-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ab04e-121">FilterControl</span><span class="sxs-lookup"><span data-stu-id="ab04e-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ab04e-122">querycontrol</span><span class="sxs-lookup"><span data-stu-id="ab04e-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
