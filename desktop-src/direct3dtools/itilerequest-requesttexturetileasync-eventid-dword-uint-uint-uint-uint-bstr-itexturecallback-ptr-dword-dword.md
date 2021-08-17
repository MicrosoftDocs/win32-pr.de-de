---
description: Fordert an, den Inhalt einer kachelierten Textur als zu erhalten. DDS-Datei (DirectDraw Surface).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ITileRequest::RequestTextureTileAsync-Methode
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
ms.openlocfilehash: 20e67b9cd6d05e32488246306edb80d35fc8c6379fe4054f2cb1d7858f8e7402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119464"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest::RequestTextureTileAsync-Methode

Fordert an, den Inhalt einer kachelierten Textur als zu erhalten. DDS-Datei (DirectDraw Surface).

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

*Eventid*   
Das angegebene Ereignis, mit dem der Inhalt des Puffers übereinstimmen soll (z. B. kann sich ein Renderziel im Laufe der Zeit ändern).

*textureFileptr*   
Die Adresse des angegebenen Texturobjekts.

*tileSubresource*   
Die angegebene Unterressource der Kachel.

*tileX*   
Die angegebene Kachel X-Position.

*tileY*   
Die angegebene Y-Position der Kachel.

*tileZ*   
Die angegebene Kachel Z-Position.

*ddsFilename*   
Eine COM-Zeichenfolge, die den Pfadnamen der DDS-Datei enthält, in die Ergebnisse geschrieben werden.

*pRequestCallback*   
Die Adresse des Rückrufs, der verwendet wird, um den Host über Ergebnisse zu benachrichtigen.

*requestCookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert und verwendet werden kann, um zu signalisieren, dass sie abgebrochen wird.

*progressIntervalMsecs*   
Wird nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**ITileRequest**](/windows/desktop/direct3dtools/itilerequest)

 

 
