---
description: Fordert an, generische Objektdaten zurückzugeben, die ein Objekt in der VSGLOG-Datei für das angegebene Ereignis und im angegebenen Format beschreiben.
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IGenericBufferDataRequest::RequestAsync-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1859c5527480f018223933603a2dedb0af54cfe009194a170d537f10e124d35a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722067"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>IGenericBufferDataRequest::RequestAsync-Methode

Fordert an, generische Objektdaten zurückzugeben, die ein Objekt in der VSGLOG-Datei für das angegebene Ereignis und im angegebenen Format beschreiben.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*dumperType*   
Das angegebene Format der Textdarstellung des Objekts (HTML, XML usw.)

*Eventid*   
Das angegebene Ereignis, mit dem der Inhalt des Puffers übereinstimmt (z. B. kann sich ein Renderziel im Laufe der Zeit ändern).

*RequestedDataUID*   
Die Adresse des angegebenen Objekts.

*requestCallback*   
Die Adresse des Rückrufs, der verwendet wird, um den Host über Ergebnisse zu benachrichtigen.

*requestCookie*   
Ein Cookie, das die Anforderung eindeutig identifiziert und verwendet werden kann, um zu signalisieren, dass sie abgebrochen wird.

*progressIntervalMsecs*   
Wird nicht verwendet.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IGenericBufferDataRequest**](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
