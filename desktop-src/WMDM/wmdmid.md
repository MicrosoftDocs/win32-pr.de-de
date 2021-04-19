---
title: Wmdmid-Struktur
description: Die wmdmid-Struktur beschreibt Seriennummern und Gruppen-IDs.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Wmdmid-Struktur Windows Media Device Manager
- Pwmdmid-Struktur Zeiger Windows Media-Device Manager
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359792"
---
# <a name="wmdmid-structure"></a>Wmdmid-Struktur

Die **wmdmid** -Struktur beschreibt Seriennummern und Gruppen-IDs.

## <a name="syntax"></a>Syntax


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Größe der **wmdmid** -Struktur in Bytes.

</dd> <dt>

**dwvendorid**
</dt> <dd>

**DWORD** , das die registrierte ID-Nummer des Anbieters enthält. Enthält 0 (null), wenn Sie nicht verwendet wird.

</dd> <dt>

**Länge der PID- \[ wmdmid \_\]**
</dt> <dd>

Ein Zeiger auf ein Bytearray, das die Seriennummer enthält. Die Seriennummer ist eine Zeichenfolge von Byte Werten, die kein Standardformat aufweisen. Beachten Sie, dass es sich hierbei nicht um einen breit Zeichen Wert handelt. **Wmdmid \_ LENGTH** ist ein konstanter Wert, der in "mswap. h" definiert ist.

</dd> <dt>

**Serialzahldauer**
</dt> <dd>

Tatsächliche Länge der zurückgegebenen Seriennummer in Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imdspdevice:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**Imdspstorageglobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**Iwmdmdevice:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**Iwmdmstorageglobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





