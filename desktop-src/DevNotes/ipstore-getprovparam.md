---
description: Dient zum Festlegen der angegebenen Parameterinformationen.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'Ipstore:: getprovparam-Methode (pstore. h)'
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
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359225"
---
# <a name="ipstoregetprovparam-method"></a>Ipstore:: getprovparam-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

\[Diese Methode ist nicht implementiert.\]

Dient zum Festlegen der angegebenen Parameterinformationen. Beachten Sie jedoch, dass Sie nicht implementiert wird und immer fehlschlägt.

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

*dwparam* \[ in\]
</dt> <dd>

Reserviert.

</dd> <dt>

*pcbData* \[ vorgenommen\]
</dt> <dd>

Reserviert.

</dd> <dt>

*ppbdata* \[ vorgenommen\]
</dt> <dd>

Reserviert.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Aufrufen dieser Methode tritt immer ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipstore**](ipstore.md)
</dt> </dl>

 

 
