---
description: Ruft die PROPVARIANT-Zeichenfolge und die Eingabezeichenfolge ab, die einen Daten chunk darstellt. Das Aufrufen dieser Methode ist identisch mit dem Aufrufen von GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: IRichChunk::RemoteGetData-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: caaa4ab9688ab8169bd0955c8abb1e976e7eb318e94875be1486e61b32e13207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862795"
---
# <a name="irichchunkremotegetdata-method"></a>IRichChunk::RemoteGetData-Methode

Ruft die [PROPVARIANT-Zeichenfolge](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) und die Eingabezeichenfolge ab, die einen Daten chunk darstellt. Das Aufrufen dieser Methode ist identisch mit dem Aufrufen [**von GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFirstPos* \[ out\]
</dt> <dd>

Empfängt die nullbasierte Anfangsposition des Bereichs. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pLength* \[ out\]
</dt> <dd>

Empfängt die Länge des Bereichs. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*ppsz* \[ out\]
</dt> <dd>

Empfängt den zugeordneten Unicode-Zeichenfolgenwert oder **NULL,** wenn nicht verfügbar.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Empfängt den [zugeordneten PROPVARIANT-Wert](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) oder **VT \_ EMPTY,** falls nicht verfügbar. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
