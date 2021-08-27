---
description: Ein Rückruf, der den Host über generische Pufferinformationen benachrichtigt, die von der assocaited-Anforderung zurückgegeben werden.
MS-HAID: vspixengine.IGenericBufferDataCallback\_ResultCallback\_DWORD\_BYTE\_arr\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IGenericBufferDataCallback::ResultCallback-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5627A93E-8BE8-4413-BFB4-724AF2DDFEB6
api_name:
- IGenericBufferDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0035b0546b863c87c54fbd09bbc62897ab581bfe
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622326"
---
# <a name="span-idvspixengineigenericbufferdatacallback_resultcallback_dword_byte_arr_bstrspanigenericbufferdatacallbackresultcallback-method"></a><span id="vspixengine.igenericbufferdatacallback_resultcallback_dword_byte_arr_bstr"></span>IGenericBufferDataCallback::ResultCallback-Methode

Ein Rückruf, der den Host über generische Pufferinformationen benachrichtigt, die von der assocaited-Anforderung zurückgegeben werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResultCallback(
   DWORD   size,
   BYTE [] count0_buffer,
   BSTR    type
);
```

## <a name="parameters"></a>Parameter

*Größe*   
Die Größe des Pufferinhalts in Bytes.

*\_count0-Puffer*   
Der Pufferinhalt. In den meisten Fällen handelt es sich dabei um XML-Daten.

*Typ*   
Eine COM-Zeichenfolge, die den Typ des im Puffer zurückgegebenen Inhalts angibt.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IGenericBufferDataCallback**](/windows/desktop/direct3dtools/igenericbufferdatacallback)

 

 
