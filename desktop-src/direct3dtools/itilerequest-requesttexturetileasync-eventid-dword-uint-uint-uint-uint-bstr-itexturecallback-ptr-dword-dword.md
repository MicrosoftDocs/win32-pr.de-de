---
description: Fordert an, den Inhalt einer gekachelten Textur als zu erhalten. DDS-Datei (DirectDraw Surface).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Itilerequest:: requesttexturetileasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e22c3b54c1e04242805d698c37a1d4dd2709fa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124711"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>Itilerequest:: requesttexturetileasync-Methode

Fordert an, den Inhalt einer gekachelten Textur als zu erhalten. DDS-Datei (DirectDraw Surface).

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*EventID*   
Das angegebene Ereignis, mit dem der Inhalt des Puffers verglichen werden soll (z. b. kann sich ein Renderziel im Laufe der Zeit ändern).

*texturemeleptr*   
Die Adresse des angegebenen Textur Objekts.

*tilesubresource*   
Die angegebene untergeordnete Quelle der Kachel.

*Tilex*   
Die angegebene X-Position der Kachel.

*tiley*   
Die angegebene Y-Position der Kachel.

*tilez*   
Die angegebene Z-Position der Kachel.

*ddsfilename*   
Eine com-Zeichenfolge, die den Pfadnamen der DDS-Datei enthält, in die die Ergebnisse geschrieben werden.

*prequestcallback*   
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

[**Itilerequest**](/windows/desktop/direct3dtools/itilerequest)

 

 
