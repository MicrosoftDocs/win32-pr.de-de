---
description: Die ADDRESSPAIR-Struktur erstellt einen Erfassungsfilter.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: ADDRESSPAIR-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bbfc455951e76548694415434e0ee4b53893d594b8f0f31419e516bc466ed2c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744855"
---
# <a name="addresspair-structure"></a>ADDRESSPAIR-Struktur

Die **ADDRESSPAIR-Struktur** erstellt einen Erfassungsfilter.

## <a name="syntax"></a>Syntax


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a>Member

<dl> <dt>

**AddressFlags**
</dt> <dd>

Flags, die die von einem Erfassungsfilter verwendeten Adressen beschreiben. Weitere Informationen finden Sie unter Hinweise.



| Wert                                                                                                                                                                                                         | Bedeutung                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**\_ADRESSFLAGS \_ STIMMEN MIT \_ DST ÜBEREIN**</dt> </dl>                 | Entspricht der Zieladresse.<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**ADDRESS \_ FLAGS \_ MATCH \_ SRC**</dt> </dl>                 | Entspricht der Quelladresse.<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**\_AUSGESCHLOSSENE ADRESSFLAGS \_**</dt> </dl>                     | Schließt den Frame aus, wenn diese Adresse gefunden wird.<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**\_ADRESSFLAGS \_ DST GROUP \_ \_ ADDR**</dt> </dl> | Entspricht nur Gruppenbits. Verwenden Sie dies für Nachrichten vom Typ Broadcast.<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**\_ADRESSFLAGS STIMMEN MIT \_ BEIDEN ÜBEREIN. \_**</dt> </dl>              | Entspricht Ziel- und Quelladressen.<br/>                     |



 

</dd> <dt>

**NalReserved**
</dt> <dd>

Dies ist reserviert.

</dd> <dt>

**DstAddress**
</dt> <dd>

Zieladresse des Adresspaarelements.

</dd> <dt>

**SrcAddress**
</dt> <dd>

Quelladresse des Adresspaarelements.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Flags des **AddressFlags-Members** können kombiniert werden. Die folgende Einstellung schließt z. B. den Frame aus, wenn die angegebene Quelladresse erkannt wird.

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungsfilter.](capture-filters.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




