---
description: Der \_ \_ Enumerationstyp "WPD-Speichertyp \_ Werte" beschreibt die verschiedenen Speichertypen für tragbare Windows-Geräte.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: WPD_STORAGE_TYPE_VALUES-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361534"
---
# <a name="wpd_storage_type_values-enumeration"></a><span data-ttu-id="a93c4-103">WPD \_ - \_ Speichertyp \_ Values-Enumeration</span><span class="sxs-lookup"><span data-stu-id="a93c4-103">WPD\_STORAGE\_TYPE\_VALUES enumeration</span></span>

<span data-ttu-id="a93c4-104">Der Enumerationstyp " **WPD- \_ \_ Speichertyp \_ Werte** " beschreibt die verschiedenen Speichertypen für tragbare Windows-Geräte.</span><span class="sxs-lookup"><span data-stu-id="a93c4-104">The **WPD\_STORAGE\_TYPE\_VALUES** enumeration type describes the different Windows Portable Device storage types.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93c4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a93c4-105">Syntax</span></span>


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a><span data-ttu-id="a93c4-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a93c4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a93c4-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD \_ - \_ Speichertyp nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="a93c4-107"><span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD\_STORAGE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="a93c4-108">Der Speicher weist einen nicht definierten Typ auf.</span><span class="sxs-lookup"><span data-stu-id="a93c4-108">The storage is of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="a93c4-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**Festes Rom für WPD- \_ \_ Speichertyp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a93c4-109"><span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**WPD\_STORAGE\_TYPE\_FIXED\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="a93c4-110">Der Speicher kann nicht entfernt werden und ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a93c4-110">The storage is non-removable and read-only.</span></span>

</dd> <dt>

<span data-ttu-id="a93c4-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**Wechsel-Rom für WPD- \_ \_ Speichertyp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a93c4-111"><span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="a93c4-112">Der Speicher ist austauschbar und schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a93c4-112">The storage is removable and is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="a93c4-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**Arbeitsspeicher für den WPD- \_ \_ Speichertyp \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a93c4-113"><span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**WPD\_STORAGE\_TYPE\_FIXED\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="a93c4-114">Der Speicher kann nicht entfernt werden und ist Lese-/schreibfähig.</span><span class="sxs-lookup"><span data-stu-id="a93c4-114">The storage is non-removable and is read/write capable.</span></span>

</dd> <dt>

<span data-ttu-id="a93c4-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD \_ - \_ Speichertyp Wechsel- \_ \_ RAM**</span><span class="sxs-lookup"><span data-stu-id="a93c4-115"><span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD\_STORAGE\_TYPE\_REMOVABLE\_RAM**</span></span>
</dt> <dd>

<span data-ttu-id="a93c4-116">Der Speicher ist austauschbar und ist Lese-/schreibfähig.</span><span class="sxs-lookup"><span data-stu-id="a93c4-116">The storage is removable and is read/write capable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a93c4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a93c4-117">Remarks</span></span>

<span data-ttu-id="a93c4-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="a93c4-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a93c4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a93c4-119">Requirements</span></span>



| <span data-ttu-id="a93c4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a93c4-120">Requirement</span></span> | <span data-ttu-id="a93c4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a93c4-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a93c4-122">Header</span><span class="sxs-lookup"><span data-stu-id="a93c4-122">Header</span></span><br/> | <dl> <span data-ttu-id="a93c4-123"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a93c4-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a93c4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a93c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93c4-125">**Strukturen und Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="a93c4-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




