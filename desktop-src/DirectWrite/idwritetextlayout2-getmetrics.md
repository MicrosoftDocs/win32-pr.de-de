---
title: IDWriteTextLayout2 GetMetrics-Methode
description: Ruft allgemeine Metriken für die formatierte Zeichenfolge ab.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- GetMetrics-Methode " Direct Write"
- GetMetrics-Methode Direct Write , IDWriteTextLayout2-Schnittstelle
- IDWriteTextLayout2-Schnittstelle Direct Write , GetMetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f08a0b1e47003bb818f0b80ebc3b13f639f8ded8334137d8b8812e7f0154a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070740"
---
# <a name="idwritetextlayout2getmetrics-method"></a>IDWriteTextLayout2::GetMetrics-Methode

Ruft allgemeine Metriken für die formatierte Zeichenfolge ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 *textMetrics* \[ out\]
</dt> <dd>

Typ: **[ **DWRITE \_ TEXT \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\***

Enthält nach der Rückgabe dieser Methode die gemessenen Entfernungen von Text und zugeordnetem Inhalt nach dem Formatieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





