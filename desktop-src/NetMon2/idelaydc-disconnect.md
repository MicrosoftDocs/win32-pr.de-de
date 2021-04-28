---
description: 'IDelaydC::D isconnect-Methode: Die Disconnect-Methode trennt das NPP vom Netzwerk.'
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: IDelaydC::D isconnect-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 967bd9674cb28363804b8c8af12c541bcb8675ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110808"
---
# <a name="idelaydcdisconnect-method"></a>IDelaydC::D isconnect-Methode

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



| Rückgabecode                                                                                          | Beschreibung                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR-ERFASSUNG \_**</dt> </dl>      | Das NPP erfasst Daten. Sie können das Netzwerksicherheits-Netzwerk während einer Erfassung nicht vom Netzwerk trennen.<br/>            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der NPP ist nicht mit dem Netzwerk verbunden.<br/>                                                               |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>   | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst. Sie müssen die **IDelaydC::Stop-Methode aufrufen,** bevor Sie **Disconnect aufrufen.**

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

[IDelaydC::Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




