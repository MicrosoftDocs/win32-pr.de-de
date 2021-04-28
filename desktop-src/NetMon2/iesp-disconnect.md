---
description: 'IESP::D isconnect-Methode: Die Disconnect-Methode trennt den NPP vom Netzwerk.'
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: IESP::D isconnect-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d0a07748781a567c889e879e2e99462d8cfb876a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110758"
---
# <a name="iespdisconnect-method"></a>IESP::D isconnect-Methode

Die **Disconnect-Methode** trennt den Netzwerk-NPP vom Netzwerk.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR-ERFASSUNG \_**</dt> </dl>      | Das NPP erfasst Daten. Sie können die Verbindung mit dem Netzwerk nicht trennen, während die Datenerfassung läuft.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der NPP ist nicht mit dem Netzwerk verbunden.<br/>                                                             |
| <dl> <dt>**NMERR \_ NICHT \_ ESP**</dt> </dl>       | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IESP::Connect-Methode.](iesp-connect.md)<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst. Sie müssen die **IESP::Stop-Methode aufrufen,** bevor **Sie IESP::D isconnect aufrufen.**

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Connect](iesp-connect.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 




