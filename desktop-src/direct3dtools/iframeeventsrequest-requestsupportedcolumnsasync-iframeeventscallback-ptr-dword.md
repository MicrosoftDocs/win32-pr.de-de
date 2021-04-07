---
description: Eine asynchrone Anforderung, um Informationen darüber zu erhalten, welche Spalten (Felder) dieser Frame Ereignis Anforderungstyp unterstützt.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestSupportedColumnsAsync\_IFrameEventsCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iframeeventsrequest:: requestsupportedcolumnsasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8F8ED8F7-F764-4CC8-891B-F0582F6B1337
api_name:
- IFrameEventsRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 13d4c797e338f6b0901781760a39511a1f136174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746729"
---
# <a name="span-idvspixengineiframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dwordspaniframeeventsrequestrequestsupportedcolumnsasync-method"></a><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>Iframeeventsrequest:: requestsupportedcolumnsasync-Methode

Eine asynchrone Anforderung, um Informationen darüber zu erhalten, welche Spalten (Felder) dieser Frame Ereignis Anforderungstyp unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestSupportedColumnsAsync(
   IFrameEventsCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*requestCallback*   
Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.

*progressintervalmsekunden*   
Nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iframeeventsrequest**](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
