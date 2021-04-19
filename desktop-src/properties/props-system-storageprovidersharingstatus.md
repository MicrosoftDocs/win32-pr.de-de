---
description: Diese Eigenschaft stellt einen Status mit den meisten Berechtigungen für die Datei bzw. den Ordner dar, der vom Speicher Anbieter angegeben wird. Der Freigabe Status von den meisten bis zu den geringsten Berechtigungen liegt im Besitz > > öffentlichen > Shared > private. storageprovidersharingstatus ist eine schreibgeschützte Eigenschaft.
ms.assetid: c3b93159-4279-4b27-b006-ab73e0beee9c
title: System. storageprovidersharingstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b5b6b23b3a541037511eee3ae7201252e4ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350345"
---
# <a name="systemstorageprovidersharingstatus"></a><span data-ttu-id="89d71-103">System. storageprovidersharingstatus</span><span class="sxs-lookup"><span data-stu-id="89d71-103">System.StorageProviderSharingStatus</span></span>

<span data-ttu-id="89d71-104">Diese Eigenschaft stellt einen Status mit den meisten Berechtigungen für die Datei bzw. den Ordner dar, der vom Speicher Anbieter angegeben wird. Der Freigabe Status von den meisten bis zu den geringsten Berechtigungen liegt im Besitz > > öffentlichen > Shared > private. storageprovidersharingstatus ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="89d71-104">This property represents a the most permissive share status for the file/folder specified by the storage provider.The share statuses from most to least permissive are Owned > Co-owned > Public > Shared > Private.StorageProviderSharingStatus is a readonly property.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="89d71-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="89d71-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.StorageProviderSharingStatus
   shellPKey = PKEY_StorageProviderSharingStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 117
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotShared
            value = 0
            text
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_NOTSHARED
         enum
            name = Shared
            value = 1
            text = Shared
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED
         enum
            name = Private
            value = 2
            text
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PRIVATE
         enum
            name = Public
            value = 3
            text = Public
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC
         enum
            name = SharedOwned
            value = 4
            text = Shared (co-owned, owner)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED_OWNED
         enum
            name = SharedCoOwned
            value = 5
            text = Shared (co-owned)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED_COOWNED
         enum
            name = PublicOwned
            value = 6
            text = Public (co-owned, owner)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC_OWNED
         enum
            name = PublicCoOwned
            value = 7
            text = Public (co-owned)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC_COOWNED
```

## <a name="remarks"></a><span data-ttu-id="89d71-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89d71-106">Remarks</span></span>

<span data-ttu-id="89d71-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="89d71-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89d71-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89d71-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d71-109">propertydescription</span><span class="sxs-lookup"><span data-stu-id="89d71-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="89d71-110">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="89d71-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="89d71-111">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="89d71-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="89d71-112">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="89d71-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="89d71-113">Display Info</span><span class="sxs-lookup"><span data-stu-id="89d71-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="89d71-114">StringFormat</span><span class="sxs-lookup"><span data-stu-id="89d71-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="89d71-115">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="89d71-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="89d71-116">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="89d71-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="89d71-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="89d71-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="89d71-118">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="89d71-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="89d71-119">DrawControl</span><span class="sxs-lookup"><span data-stu-id="89d71-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="89d71-120">editcontrol</span><span class="sxs-lookup"><span data-stu-id="89d71-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="89d71-121">FilterControl</span><span class="sxs-lookup"><span data-stu-id="89d71-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="89d71-122">querycontrol</span><span class="sxs-lookup"><span data-stu-id="89d71-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
