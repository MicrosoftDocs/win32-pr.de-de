---
description: Die QueryStatus-Methode ruft den Status des NPP ab.
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: 'IStats:: QueryStatus-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 02e013d87734b61ad26b6563c402db1b8d4cb4f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760837"
---
# <a name="istatsquerystatus-method"></a>IStats:: QueryStatus-Methode

Die **QueryStatus** -Methode ruft den Status des NPP ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnetworkstatus* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine zurückgegebene [networkstatus](networkstatus.md) -Struktur, die den aktuellen Zustand (aufzeichnen, angehalten, beendet usw.) des NPP angibt. Es ist Aufgabe der Anwendung, den Arbeitsspeicher für die **networkstatus** -Struktur zuzuordnen und freizugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ungültiger nmerr- \_ \_ Parameter**</dt> </dl> | Der *pnetworkstatus* -Parameter verweist nicht auf eine gültige [networkstatus](networkstatus.md) -Struktur. Weisen Sie für diese Struktur Arbeitsspeicher zu, und nennen Sie die **iStats:: QueryStatus** -Methode erneut.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jederzeit aufgerufen werden, nachdem die Methode " [comatenppinterface](createnppinterface.md) " aufgerufen wurde. Es kann aufgerufen werden, um festzustellen, ob der NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu ermitteln und um zu ermitteln, ob Trigger ausstehend sind. Vor dem Aufrufen dieser Methode müssen Sie jedoch den Arbeitsspeicher zuordnen, der für die [networkstatus](networkstatus.md) -Struktur benötigt wird, und diesen Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

["Kreatenppinterface"](createnppinterface.md)
</dt> <dt>

[Vornehmen](networkstatus.md)
</dt> </dl>

 

 




