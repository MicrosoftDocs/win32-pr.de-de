---
description: Ruft die nächste angegebene Anzahl von Datenelementnamen in der Enumerationssequenz ab.
ms.assetid: 6f30bf64-bd63-43d7-ab7e-f64e372c723b
title: IEnumPStoreItems::Next-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0a70ac415c937b3fb3d5bf95901d2ae30f9d4b8fd5b5677c55465ccbadada4b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432590"
---
# <a name="ienumpstoreitemsnext-method"></a>IEnumPStoreItems::Next-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Ruft die nächste angegebene Anzahl von Datenelementnamen in der Enumerationssequenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ In\]
</dt> <dd>

Die Anzahl der angeforderten Datenelemente.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, in der der Datenelementname zurückgegeben werden soll.

</dd> <dt>

*pceltFetched* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Anzahl der tatsächlich angegebenen Datenelementnamen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> </dl>

 

 
