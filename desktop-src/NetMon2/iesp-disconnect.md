---
description: Mit der Disconnect-Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: IESP::D isconnect-Methode (Netmon. h)
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
ms.openlocfilehash: b0dac1843083d77121883b2609c32addffbae290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128328"
---
# <a name="iespdisconnect-method"></a>IESP::D isconnect-Methode

Mit der **Disconnect** -Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>      | Der NPP erfasst Daten. Die Verbindung mit dem Netzwerk kann während der Datenerfassung nicht getrennt werden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl> | Der npp ist nicht mit dem Netzwerk verbunden.<br/>                                                             |
| <dl> <dt>**nmerr \_ nicht \_ ESP**</dt> </dl>       | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst. Sie müssen vor dem Aufrufen von **iESP::D isconnect** die **iESP:: Station** -Methode aufrufen.

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

[IESP:: Connect](iesp-connect.md)
</dt> <dt>

[IESP:: Beendigung](iesp-stop.md)
</dt> </dl>

 

 




