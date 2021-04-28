---
description: 'IRTC::QueryStatus-Methode: Die QueryStatus-Methode ruft den Status des NPP ab.'
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: IRTC::QueryStatus-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 6dd8c18d19df7d577ad219742520630f00122a41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110608"
---
# <a name="irtcquerystatus-method"></a>IRTC::QueryStatus-Methode

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

Zeiger auf eine zurückgegebene [NETWORKSTATUS-Struktur,](networkstatus.md) die den aktuellen Zustand (Erfassen, Anhalten, Beendet usw.) des NPP angibt. Es liegt in der Verantwortung der Anwendung, den Arbeitsspeicher für die **NETWORKSTATUS-Struktur** zuzuordnen und freizugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ – UNGÜLTIGER \_ PARAMETER**</dt> </dl> | Der *pNetworkStatus-Parameter* verweist nicht auf eine gültige [NETWORKSTATUS-Struktur.](networkstatus.md) Belegen Sie Arbeitsspeicher für diese Struktur, und rufen Sie **IRTC::QueryStatus** erneut auf.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jederzeit aufgerufen werden, nachdem die [CreateNPPInterface-Methode](createnppinterface.md) aufgerufen wurde. Sie können diese Methode aufrufen, um festzustellen, ob das NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu ermitteln und um festzustellen, ob Trigger ausstehend sind. Vor dem Aufrufen dieser Methode müssen Sie jedoch den für die [NETWORKSTATUS-Struktur](networkstatus.md) benötigten Arbeitsspeicher zuordnen und diesen Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[Networkstatus](networkstatus.md)
</dt> </dl>

 

 




