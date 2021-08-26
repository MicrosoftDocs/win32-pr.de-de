---
description: Ruft den NPP-Status ab.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: IESP::QueryStatus-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 00b83cbbb167775a8de360c880f381b41f250abf0eab01c883bc7580be4d956f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037540"
---
# <a name="iespquerystatus-method"></a>IESP::QueryStatus-Methode

Die **QueryStatus-Methode** ruft den NPP-Status ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNetworkStatus* \[ out\]
</dt> <dd>

Ein Zeiger auf eine zurückgegebene [NETWORKSTATUS-Struktur,](networkstatus.md) der den aktuellen Zustand des NPP angibt (Erfassen, Anhalten, Beendeten und so weiter). Der Benutzer muss den Arbeitsspeicher für die NETWORKSTATUS-Struktur zuordnen und frei geben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ INVALID \_ PARAMETER**</dt> </dl> | Der *pNetworkStatus-Parameter* zeigt nicht auf eine gültige [NETWORKSTATUS-Struktur.](networkstatus.md) Ordnen Sie Arbeitsspeicher für diese Struktur zu, und rufen **Sie IESP::QueryStatus erneut** auf.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann jederzeit aufgerufen werden, nachdem [CreateNPPInterface](createnppinterface.md) aufgerufen wurde. Sie können diese Methode aufrufen, um zu überprüfen, ob die NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu finden und um zu überprüfen, ob Trigger ausstehen.

Weisen Sie vor dem Aufrufen dieser Methode den für die [NETWORKSTATUS-Struktur](networkstatus.md) erforderlichen Arbeitsspeicher zu, und geben Sie diesen Arbeitsspeicher frei, wenn die Struktur nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[Networkstatus](networkstatus.md)
</dt> </dl>

 

 




