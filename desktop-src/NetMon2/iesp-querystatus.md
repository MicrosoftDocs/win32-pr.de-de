---
description: Ruft den NPP-Status ab.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'IESP:: QueryStatus-Methode (Netmon. h)'
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
ms.openlocfilehash: 3435ed832484042bfeb9229e4b46fa34441cb395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215473"
---
# <a name="iespquerystatus-method"></a>IESP:: QueryStatus-Methode

Die **QueryStatus** -Methode ruft den NPP-Status ab.

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

Ein Zeiger auf eine zurückgegebene [Network Status](networkstatus.md) -Struktur, die den aktuellen Zustand (Erfassung, angehalten, angehalten usw.) des NPP angibt. Der Benutzer muss den Speicher für die networkstatus-Struktur zuordnen und freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert der folgende Fehlercode:



| Rückgabecode                                                                                              | Beschreibung                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ungültiger nmerr- \_ \_ Parameter**</dt> </dl> | Der *pnetworkstatus* -Parameter verweist nicht auf eine gültige [networkstatus](networkstatus.md) -Struktur. Weisen Sie für diese Struktur Arbeitsspeicher zu, und nennen Sie **iESP:: QueryStatus** erneut.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jederzeit aufgerufen werden, nachdem " [comatenppinterface](createnppinterface.md) " aufgerufen wurde. Sie können diese Methode abrufen, um zu ermitteln, ob der NPP mit dem Netzwerk verbunden ist, um den Status der aktuellen Erfassung zu ermitteln und zu überprüfen, ob Trigger ausstehend sind.

Bevor Sie diese Methode aufrufen, müssen Sie den für die [networkstatus](networkstatus.md) -Struktur erforderlichen Arbeitsspeicher zuordnen und diesen Speicher freigeben, wenn die Struktur nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

["Kreatenppinterface"](createnppinterface.md)
</dt> <dt>

[Vornehmen](networkstatus.md)
</dt> </dl>

 

 




