---
description: Eine asynchrone Anforderung zum erhalten der im Grafik Protokoll erfassten Listen Frames.
MS-HAID: vspixengine.IFrameListRequest\_RequestAsync\_IFrameListCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframelistrequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 309C28F2-CE01-49E7-9A21-5053E3ED7721
api_name:
- IFrameListRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3627fc5ef3a425ae7607009b4ad382080ea99192
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041161"
---
# <a name="span-idvspixengineiframelistrequest_requestasync_iframelistcallback_ptr_dword_dwordspaniframelistrequestrequestasync-method"></a><span id="vspixengine.iframelistrequest_requestasync_iframelistcallback_ptr_dword_dword"></span>Iframelistrequest:: requestasync-Methode

Eine asynchrone Anforderung zum erhalten der im Grafik Protokoll erfassten Listen Frames.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestAsync(
   IFrameListCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*requestCallback*   
Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.

*requestcookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.

*progressintervalmsekunden*   
Nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iframelistrequest**](/windows/desktop/direct3dtools/iframelistrequest)

 

 
