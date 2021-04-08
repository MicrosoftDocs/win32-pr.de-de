---
description: Fordert an, dass für das angegebene Ereignis angegebene Informationen aus der Objekttabelle erhalten.
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iobjecttablerequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746728"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>Iobjecttablerequest:: requestasync-Methode

Fordert an, dass für das angegebene Ereignis angegebene Informationen aus der Objekttabelle erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>Parameter

*EventID*   
Das angegebene Ereignis.

*NumColumns*   
Die Anzahl der Spalten (Felder) der aufzurufenden Informationen.

*count1- \_ Spalten*   
Die angegebenen Spalten (Felder).

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

[**Iobjecttablerequest**](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
