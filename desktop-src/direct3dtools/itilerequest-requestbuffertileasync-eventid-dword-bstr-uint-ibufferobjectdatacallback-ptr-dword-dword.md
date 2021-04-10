---
description: Fordert an, den Rohinhalt einer Kachel zu erhalten.
MS-HAID: vspixengine.ITileRequest_RequestBufferTileAsync_EventID_DWORD_BSTR_UINT_IBufferObjectDataCallback_ptr_DWORD_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Itilerequest:: requestbuffertileasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2D68766F-1BED-439E-AC51-790471DA4F70
api_name:
- ITileRequest.RequestBufferTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 83f013b4bc3235ece2850c75324333e4b59d298f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213995"
---
# <a name="span-idvspixengineitilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dwordspanitilerequestrequestbuffertileasync-method"></a><span id="vspixengine.itilerequest_requestbuffertileasync_eventid_dword_bstr_uint_ibufferobjectdatacallback_ptr_dword_dword"></span>Itilerequest:: requestbuffertileasync-Methode

Fordert an, den Rohinhalt einer Kachel zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestBufferTileAsync(
   EventID                     eventID,
   DWORD                       RequestedDataUID,
   BSTR                        File,
   UINT                        tileIndex,
   IBufferObjectDataCallback * requestCallback,
   DWORD                       requestCookie,
   DWORD                       progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*EventID*   
Das angegebene Ereignis, mit dem der Inhalt der Kachel abgeglichen werden soll (z. b. ein Renderziel kann sich im Laufe der Zeit ändern).

*Requesteddatauid*   
Die Adresse der angegebenen Kachel.

*Datei*   
Eine com-Zeichenfolge, die den Pfadnamen der Datei enthält, in die Ergebnisse geschrieben werden.

*tileingedex*   
Der Index der angegebenen Kachel.

*requestCallback*   
Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.

*requestcookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.

*progressintervalmsekunden*   
Nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Itilerequest**](/windows/desktop/direct3dtools/itilerequest)

 

 
