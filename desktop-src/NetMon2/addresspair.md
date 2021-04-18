---
description: Die "adresssspair"-Struktur erstellt einen Erfassungs Filter.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Adresssspair-Struktur (Netmon. h)
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
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358564"
---
# <a name="addresspair-structure"></a>Adresssspair-Struktur

Die " **adresssspair** "-Struktur erstellt einen Erfassungs Filter.

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

**Addressflags**
</dt> <dd>

Flags, die die von einem Erfassungs Filter verwendeten Adressen beschreiben. Weitere Informationen finden Sie unter Hinweise.



| Wert                                                                                                                                                                                                         | Bedeutung                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**\_adressflags \_ entsprechen " \_ DST"**</dt> </dl>                 | Entspricht der Zieladresse.<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**\_adressflags \_ entsprechen \_ src**</dt> </dl>                 | Entspricht der Quelladresse.<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**\_ \_ ausgeschlossene adressflags**</dt> </dl>                     | Schließt den Frame aus, wenn diese Adresse gefunden wurde.<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**\_adressflags \_ DST \_ Group \_ addr**</dt> </dl> | Entspricht nur dem Gruppen Bit. Verwenden Sie dies für Broadcast-/typnachrichten.<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**\_adressflags \_ stimmen mit \_ beiden identisch.**</dt> </dl>              | Entspricht den Ziel-und Quelladressen.<br/>                     |



 

</dd> <dt>

**Nalreserved**
</dt> <dd>

Dies ist reserviert.

</dd> <dt>

**Dstaddress**
</dt> <dd>

Die Zieladresse des Adress paar Elements.

</dd> <dt>

**Srcaddress**
</dt> <dd>

Die Quelladresse des Adress paar Elements.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Flags des **addressflags** -Members können kombiniert werden. Die folgende Einstellung schließt z. b. den Frame aus, wenn die angegebene Quelladresse erkannt wird.

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungs Filter](capture-filters.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Capturefilter](capturefilter.md)
</dt> </dl>

 

 




