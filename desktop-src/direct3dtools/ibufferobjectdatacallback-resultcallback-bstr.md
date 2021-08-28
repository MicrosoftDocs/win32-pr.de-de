---
description: Ein Rückruf, der den Host von Pufferinformationen benachrichtigt, die von der assocaited-Anforderung in eine Datei geschrieben wurden.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IBufferObjectDataCallback::ResultCallback-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: eaf084402c1cc34bff83d3b50002fbdcf3d97fb1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623096"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback::ResultCallback-Methode

Ein Rückruf, der den Host von Pufferinformationen benachrichtigt, die von der assocaited-Anforderung in eine Datei geschrieben wurden.

## <a name="syntax"></a>Syntax

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a>Parameter

*Datei* Eine COM-Zeichenfolge, die den Pfadnamen der Datei enthält, in die Ergebnisse geschrieben werden.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IBufferObjectDataCallback**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
