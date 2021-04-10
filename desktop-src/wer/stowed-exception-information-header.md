---
title: STOWED_EXCEPTION_INFORMATION_HEADER Struktur
description: Enthält Informationen, die die übergeordnete Struktur identifizieren.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER Struktur Windows-Fehlerberichterstattung
- PSTOWED_EXCEPTION_INFORMATION_HEADER Struktur Zeiger Windows-Fehlerberichterstattung
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040916"
---
# <a name="stowed_exception_information_header-structure"></a>Header Struktur der verstauten \_ Ausnahme \_ Informationen \_

Enthält Informationen, die die übergeordnete Struktur identifizieren.

## <a name="syntax"></a>Syntax


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Größe der übergeordneten Struktur in Bytes.

</dd> <dt>

**Signature**
</dt> <dd>

Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ein 32-Bit-Wert, der die Signatur der übergeordneten Struktur angibt.



| Wert                                                                                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <dt>**Verstauaut \_ Ausnahme \_ Informationen \_ v1- \_ Signatur**</dt> <dt>"SE01"</dt> </dl> | Dieser Wert gibt an, dass das übergeordnete Element eine **verstaute \_ Ausnahme \_ Information \_ v1** -Struktur ist.<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <dt>**Verstauaut \_ Ausnahme \_ Informationen \_ v2- \_ Signatur**</dt> <dt>"SE02"</dt> </dl> | Dieser Wert gibt an, dass das übergeordnete Element eine [**verstaute \_ Ausnahme \_ Information \_ v2**](stowed-exception-information-v2.md) -Struktur ist.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

[**Verstauaut \_ Ausnahme \_ Informationen \_ v2**](stowed-exception-information-v2.md) -und **gestaut- \_ Ausnahme \_ Informations \_ Header** sind zurzeit nicht in einem Header definiert, der öffentlich verfügbar ist, sodass Sie Sie im Quellcode definieren müssen, bevor Sie Sie verwenden.

Die Struktur der **verstauten \_ Ausnahme \_ Informationen \_ v1** ist mit dieser Struktur identisch, außer Sie enthält nicht die Member " **netstedexceptiontype** " und " **netstedexception** ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>None</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Informationen zu verstauten \_ Ausnahmen \_ \_ v2**](stowed-exception-information-v2.md)
</dt> </dl>

 

