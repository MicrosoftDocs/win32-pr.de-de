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
# <a name="wpd_storage_type_values-enumeration"></a>WPD \_ - \_ Speichertyp \_ Values-Enumeration

Der Enumerationstyp " **WPD- \_ \_ Speichertyp \_ Werte** " beschreibt die verschiedenen Speichertypen für tragbare Windows-Geräte.

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

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**WPD \_ - \_ Speichertyp nicht \_ definiert**
</dt> <dd>

Der Speicher weist einen nicht definierten Typ auf.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**Festes Rom für WPD- \_ \_ Speichertyp \_ \_**
</dt> <dd>

Der Speicher kann nicht entfernt werden und ist schreibgeschützt.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**Wechsel-Rom für WPD- \_ \_ Speichertyp \_ \_**
</dt> <dd>

Der Speicher ist austauschbar und schreibgeschützt.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**Arbeitsspeicher für den WPD- \_ \_ Speichertyp \_ \_**
</dt> <dd>

Der Speicher kann nicht entfernt werden und ist Lese-/schreibfähig.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**WPD \_ - \_ Speichertyp Wechsel- \_ \_ RAM**
</dt> <dd>

Der Speicher ist austauschbar und ist Lese-/schreibfähig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




