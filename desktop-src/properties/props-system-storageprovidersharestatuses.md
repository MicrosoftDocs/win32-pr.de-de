---
description: Diese Eigenschaft stellt eine Liste von Freigabe Status für die Datei bzw. den Ordner dar, die vom Speicher Anbieter angegeben werden. Jeder Freigabe Status muss einer der bekannten Werte sein, die von den Enumerationen angegeben werden, dass belowstorageprovidersharestatuses eine schreibgeschützte Eigenschaft ist. Sie sollte nur vom Speicher Anbieter aktualisiert werden.
ms.assetid: 131bf48a-0ab9-4b1f-9625-6fca5d15219f
title: System. storageprovidersharestatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92340e4afb1005146a32d2505292a5e60dec971
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362334"
---
# <a name="systemstorageprovidersharestatuses"></a><span data-ttu-id="28f35-103">System. storageprovidersharestatus</span><span class="sxs-lookup"><span data-stu-id="28f35-103">System.StorageProviderShareStatuses</span></span>

<span data-ttu-id="28f35-104">Diese Eigenschaft stellt eine Liste von Freigabe Status für die Datei bzw. den Ordner dar, die vom Speicher Anbieter angegeben werden. Jeder Freigabe Status muss einer der bekannten Werte sein, die von den Enumerationen angegeben werden, dass belowstorageprovidersharestatuses eine schreibgeschützte Eigenschaft ist. Sie sollte nur vom Speicher Anbieter aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="28f35-104">This property represents a list of share statuses for the file/folder specified by the storage provider.Each share status must be one of the known value specified by the enumerations belowStorageProviderShareStatuses is a readonly property, it should only be updated by the storage provider.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="28f35-105">Windows 10, Version 1703, Windows 10, Version 1607, Windows 10, Version 1511, Windows 10, Version 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="28f35-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.StorageProviderShareStatuses
   shellPKey = PKEY_StorageProviderShareStatuses
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 111
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Private
            value = Private
            text = Private
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_PRIVATE
            mnemonics = private
         enum
            name = Shared
            value = Shared
            text = Shared
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_SHARED
            mnemonics = shared
         enum
            name = Public
            value = Public
            text = Public
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_PUBLIC
            mnemonics = public
         enum
            name = Group
            value = Group
            text = Group
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_GROUP
            mnemonics = group
         enum
            name = Owner
            value = Owner
            text = Owner
            defineToken = STORAGE_PROVIDER_SHARE_STATUS_OWNER
            mnemonics = owner
```

## <a name="remarks"></a><span data-ttu-id="28f35-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28f35-106">Remarks</span></span>

<span data-ttu-id="28f35-107">Pkey-Werte werden in "propkey. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="28f35-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28f35-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28f35-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f35-109">propertydescription</span><span class="sxs-lookup"><span data-stu-id="28f35-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="28f35-110">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="28f35-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="28f35-111">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="28f35-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="28f35-112">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="28f35-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="28f35-113">Display Info</span><span class="sxs-lookup"><span data-stu-id="28f35-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="28f35-114">StringFormat</span><span class="sxs-lookup"><span data-stu-id="28f35-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="28f35-115">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="28f35-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="28f35-116">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="28f35-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="28f35-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="28f35-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="28f35-118">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="28f35-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="28f35-119">DrawControl</span><span class="sxs-lookup"><span data-stu-id="28f35-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="28f35-120">editcontrol</span><span class="sxs-lookup"><span data-stu-id="28f35-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="28f35-121">FilterControl</span><span class="sxs-lookup"><span data-stu-id="28f35-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="28f35-122">querycontrol</span><span class="sxs-lookup"><span data-stu-id="28f35-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
