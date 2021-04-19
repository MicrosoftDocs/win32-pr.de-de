---
description: Die QueryStatus-Methode ruft den Status des NPP ab.
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: 'Idelta-DC:: QueryStatus-Methode (Netmon. h)'
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
ms.openlocfilehash: cff92dfec95555076f9edba5a1b591f0ef905c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356654"
---
# <a name="idelaydcquerystatus-method"></a>Idelta aydc:: QueryStatus-Methode

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

Ein Zeiger auf eine zurückgegebene [networkstatus](networkstatus.md) -Struktur, die den aktuellen Zustand (aufzeichnen, angehalten, beendet usw.) des NPP angibt. Es liegt in ihrer Verantwortung, den der **Network Status** -Struktur zugeordneten Arbeitsspeicher zuzuordnen und freizugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ungültiger nmerr- \_ \_ Parameter**</dt> </dl> | Der *pnetworkstatus* -Parameter verweist nicht auf eine gültige [networkstatus](networkstatus.md) -Struktur. Weisen Sie für diese Struktur Arbeitsspeicher zu, und nennen Sie die **idelta-DC:: QueryStatus** -Methode erneut.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jederzeit aufgerufen werden, nachdem " [comatenppinterface](createnppinterface.md) " aufgerufen wurde. Es kann aufgerufen werden, um festzustellen, ob der NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu ermitteln und um zu ermitteln, ob Trigger ausstehend sind.

Bevor Sie diese Methode aufrufen, müssen Sie den für die [networkstatus](networkstatus.md) -Struktur benötigten Arbeitsspeicher zuordnen und diesen Arbeitsspeicher freigeben, wenn die Struktur nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC](idelaydc.md)
</dt> <dt>

["Kreatenppinterface"](createnppinterface.md)
</dt> <dt>

[Vornehmen](networkstatus.md)
</dt> </dl>

 

 




