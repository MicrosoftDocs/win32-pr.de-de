---
description: 'IDelaydC::QueryStatus-Methode: Die QueryStatus-Methode ruft den Status des NPP ab.'
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: IDelaydC::QueryStatus-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 13d1e34b57302d263b81ed64df0b136dc01177b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118458"
---
# <a name="idelaydcquerystatus-method"></a>IDelaydC::QueryStatus-Methode

Die **QueryStatus-Methode** ruft den Status des NPP ab.

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

Zeiger auf eine zurückgegebene [NETWORKSTATUS-Struktur,](networkstatus.md) die den aktuellen Zustand des NPP angibt (Erfassen, Anhalten, Beendeten und so weiter). Es liegt in Ihrer Verantwortung, den der **NETWORKSTATUS-Struktur** zugeordneten Arbeitsspeicher zu reservieren und frei zu geben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ INVALID \_ PARAMETER**</dt> </dl> | Der *pNetworkStatus-Parameter* zeigt nicht auf eine gültige [NETWORKSTATUS-Struktur.](networkstatus.md) Ordnen Sie Arbeitsspeicher für diese Struktur zu, und rufen Sie **erneut die IDelaydC::QueryStatus-Methode** auf.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jederzeit aufgerufen werden, nachdem [CreateNPPInterface](createnppinterface.md) aufgerufen wurde. Sie kann aufgerufen werden, um zu überprüfen, ob die NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu finden und um zu überprüfen, ob Trigger ausstehen.

Bevor Sie diese Methode aufrufen, müssen Sie den für die [NETWORKSTATUS-Struktur](networkstatus.md) erforderlichen Arbeitsspeicher zuordnen und den Arbeitsspeicher frei geben, wenn die Struktur nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[Networkstatus](networkstatus.md)
</dt> </dl>

 

 




