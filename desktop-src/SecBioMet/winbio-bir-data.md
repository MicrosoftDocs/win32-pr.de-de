---
title: WINBIO_BIR_DATA-Struktur (Winbio \_ types.h)
description: Gibt die Größe in Bytes und den Offset eines Blocks biometrischer Informationen an.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- WINBIO_BIR_DATA Struktur Windows Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01978cf55d90e217aa50fb8fad696f6af90b33ab9e59975a901daa99db633181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911044"
---
# <a name="winbio_bir_data-structure"></a>WINBIO \_ BIR \_ DATA-Struktur

Die **WINBIO \_ BIR \_ DATA-Struktur** gibt die Größe in Bytes und den Offset eines Blocks biometrischer Informationen an. Diese Struktur wird von der [**WINBIO \_ BIR-Struktur**](winbio-bir.md) verwendet, um anzugeben, wo sich die verschiedenen Teile eines biometrischen Informationsdatensatzes befinden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Größe der biometrischen Informationen in Bytes.

</dd> <dt>

**Offset**
</dt> <dd>

Offset der biometrischen Informationen in Bytes vom Anfang der [**WINBIO \_ BIR-Struktur.**](winbio-bir.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Verwendung von Offsets anstelle von Zeigern ermöglicht eine einfache Serialisierung der BIR und eine weniger komplizierte Übersetzung zwischen 32- und 64-Bit-Umgebungen oder zwischen Benutzer- und Kernelmodus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ BIR**](winbio-bir.md)
</dt> <dt>

[**WINBIO \_ \_ BIR-HEADER**](winbio-bir-header.md)
</dt> </dl>

 

 





