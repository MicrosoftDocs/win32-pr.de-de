---
description: Der \_ WPD STORAGE \_ TYPE \_ VALUES-Enumerationstyp beschreibt die verschiedenen Speichertypen Windows Portable Device.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: WPD_STORAGE_TYPE_VALUES-Enumeration (PortableDevice.h)
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
ms.openlocfilehash: 1aad78833f9e5baa0d3c7da3ab37d39f4159672b85d5c01c54ae8b034c5b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842076"
---
# <a name="wpd_storage_type_values-enumeration"></a>WPD \_ STORAGE \_ TYPE \_ VALUES-Enumeration

Der **WPD \_ STORAGE TYPE \_ VALUES-Enumerationstyp \_** beschreibt die verschiedenen Speichertypen Windows Portable Device.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**\_WPD-SPEICHERTYP \_ \_ UNDEFINED**
</dt> <dd>

Der Speicher hat einen nicht definierten Typ.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**\_FESTES ROM DES WPD-SPEICHERTYPS \_ \_ \_**
</dt> <dd>

Der Speicher ist nicht wechselbar und schreibgeschützt.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_WECHSELDATENTRÄGER DES WPD-SPEICHERTYPS \_ \_ \_**
</dt> <dd>

Der Speicher ist wechselbar und schreibgeschützt.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ WPD-SPEICHERTYP \_ FESTER \_ RAM**
</dt> <dd>

Der Speicher ist nicht wechselbar und lese-/schreibfähig.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_WPD-SPEICHERTYP \_ \_ \_ WECHSELDATENTRÄGER**
</dt> <dd>

Der Speicher ist wechselbar und lese-/schreibfähig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




