---
title: IDWriteTextLayout3 getLineMetrics-Methode
description: Ruft die Eigenschaften der einzelnen Zeilen ab.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- GetLineMetrics-Methode direkt schreiben
- GetLineMetrics-Methode Direct Write, IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3 Interface Direct Write, getLineMetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477517"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a>IDWriteTextLayout3:: getLineMetrics-Methode

Ruft die Eigenschaften der einzelnen Zeilen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*linemetriken* \[ vorgenommen\]
</dt> <dd>

Das Array, das mit Zeilen Informationen aufgefüllt werden soll.

</dd> <dt>

*MaxLineCount* 
</dt> <dd>

Die maximale Größe des LineMetrics-Arrays.

</dd> <dt>

*actuallinecount* \[ vorgenommen\]
</dt> <dd>

Die tatsächliche Größe des benötigten LineMetrics-Arrays.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn MaxLineCount nicht groß genug \_ \_ und kein ausreichender \_ Puffer ist, der HRESULT \_ aus \_ Win32 (Fehler \_ unzureichender \_ Puffer) entspricht, wird zurückgegeben, und actuallinecount wird auf die Anzahl der benötigten Zeilen festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





