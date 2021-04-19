---
description: Ruft die nächste angegebene Anzahl von Datenelement Namen in der enumerationssequenz ab.
ms.assetid: 6f30bf64-bd63-43d7-ab7e-f64e372c723b
title: 'Iumumpstoreitems:: Next-Methode (pstore. h)'
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
ms.openlocfilehash: 967f2f84553b87965d5b2c92d99e347cb259264b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372236"
---
# <a name="ienumpstoreitemsnext-method"></a>Iumumpstoreitems:: Next-Methode

\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar. Pstore verwendet eine ältere Implementierung des Schutzes von Daten. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]

Ruft die nächste angegebene Anzahl von Datenelement Namen in der enumerationssequenz ab.

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

*celt* \[ in\]
</dt> <dd>

Die Anzahl der angeforderten Datenelemente.

</dd> <dt>

*rgelt* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, in die der Datenelement Name zurückgegeben werden soll.

</dd> <dt>

*pceltfetch* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Datenelement Namen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT** -Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iumumpstoreitems**](ienumpstoreitems.md)
</dt> </dl>

 

 
