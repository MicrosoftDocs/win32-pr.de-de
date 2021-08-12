---
title: WMDMID-Struktur
description: Die WMDMID-Struktur beschreibt Seriennummern und Gruppen-IDs.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- WMDMID-Strukturfenster Media Geräte-Manager
- PWMDMID-Strukturzeigerfenster Media Geräte-Manager
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
ms.openlocfilehash: 93079b2b32dae918e1c7f5c7756a1c24dd29c539c6b760dc698273006ae30f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583993"
---
# <a name="wmdmid-structure"></a>WMDMID-Struktur

Die **WMDMID-Struktur** beschreibt Seriennummern und Gruppen-IDs.

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

**cbSize**
</dt> <dd>

Größe der **WMDMID-Struktur** in Bytes.

</dd> <dt>

**dwVendorID**
</dt> <dd>

**DWORD** mit der registrierten ID-Nummer des Anbieters. Enthält 0 (null), wenn es nicht verwendet wird.

</dd> <dt>

**pID \[ WMDMID \_ LENGTH\]**
</dt> <dd>

Zeiger auf ein Bytearray, das die Seriennummer enthält. Die Seriennummer ist eine Zeichenfolge mit Bytewerten, die kein Standardformat haben. Beachten Sie, dass dies kein Breitzeichenwert ist. **WMDMID \_ LENGTH** ist ein konstanter Wert, der in mswmdm.h definiert ist.

</dd> <dt>

**SerialNumberLength**
</dt> <dd>

Die tatsächliche Länge der zurückgegebenen Seriennummer in Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMDSPDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**IWMDMDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





