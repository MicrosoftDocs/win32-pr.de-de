---
description: Ruft die PROPVARIANT-und Eingabe Zeichenfolge ab, die einen Datenblock darstellt. Das Aufrufen dieser Methode entspricht dem Aufrufen von GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'Irichchunk:: remotegetdata-Methode'
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
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128505"
---
# <a name="irichchunkremotegetdata-method"></a>Irichchunk:: remotegetdata-Methode

Ruft die [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -und Eingabe Zeichenfolge ab, die einen Datenblock darstellt. Das Aufrufen dieser Methode entspricht dem Aufrufen von [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).

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

*Pfirsich Torys* \[ vorgenommen\]
</dt> <dd>

Empfängt die null basierte Anfangsposition des Bereichs. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*pLength* \[ vorgenommen\]
</dt> <dd>

Empfängt die Länge des Bereichs. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*ppsz* \[ vorgenommen\]
</dt> <dd>

Empfängt den zugeordneten Unicode-Zeichen folgen Wert oder **null** , wenn er nicht verfügbar ist.

</dd> <dt>

*pValue* \[ vorgenommen\]
</dt> <dd>

Empfängt den zugeordneten [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Wert oder **VT \_ empty** , wenn nicht verfügbar. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Irichchunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
