---
description: Ein Rückruf, der den Host über Puffer Informationen benachrichtigt, die von der assocaas-Anforderung in eine Datei geschrieben wurden.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ibufferobjectdatacallback:: resultCallback-Methode'
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
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392874"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Ibufferobjectdatacallback:: resultCallback-Methode

Ein Rückruf, der den Host über Puffer Informationen benachrichtigt, die von der assocaas-Anforderung in eine Datei geschrieben wurden.

## <a name="syntax"></a>Syntax

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a>Parameter

*Datei* Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die Ergebnisse geschrieben werden.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ibufferobjectdatacallback**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
