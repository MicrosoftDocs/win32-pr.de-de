---
description: Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Gelesener texel-Wert abgeschlossen wurde.
MS-HAID: vspixengine.IPixEngine5Callbacks\_ReadTexelValueComplete\_UINT\_BSTR\_arr\_double\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks::ReadTexelValueComplete-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAC08D8-0E4F-40B5-B91C-5C9159665C96
api_name:
- IPixEngine5Callbacks.ReadTexelValueComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b79abda0c76e20933465c3611431761e07a5a963
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624906"
---
# <a name="span-idvspixengineipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arrspanipixengine5callbacksreadtexelvaluecomplete-method"></a><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>IPixEngine5Callbacks::ReadTexelValueComplete-Methode

Eine Rückruffunktion, die verwendet wird, um den Host zu benachrichtigen, wenn ein Gelesener texel-Wert abgeschlossen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadTexelValueComplete(
   UINT      numChannels,
   BSTR []   count0_channelNames,
   double [] count0_channelValues
);
```

## <a name="parameters"></a>Parameter

*numChannels*   
Die Anzahl der Kanäle, über die das Texel verfügt.

*count0 \_ channelNames*   
COM-Zeichenfolgen, die die Namen der Kanäle enthalten.

*count0 \_ channelValues*   
Die Werte der Kanäle.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
