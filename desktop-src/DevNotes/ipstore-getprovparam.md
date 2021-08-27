---
description: Zum Festlegen der angegebenen Parameterinformationen vorgesehen.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: IPStore::GetProvParam-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: de18c4452456ed98f7e5214a33445a0780189f7864d96cfb05e08123a3b42cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955909"
---
# <a name="ipstoregetprovparam-method"></a>IPStore::GetProvParam-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

\[Diese Methode ist nicht implementiert.\]

Zum Festlegen der angegebenen Parameterinformationen vorgesehen. Beachten Sie jedoch, dass sie nicht implementiert ist und immer fehlschlägt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwParam* \[ In\]
</dt> <dd>

Reserviert.

</dd> <dt>

*datasetData* \[ out\]
</dt> <dd>

Reserviert.

</dd> <dt>

*ppbData* \[ out\]
</dt> <dd>

Reserviert.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Aufrufe dieser Methode führen immer zu Einem Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
