---
description: 'IDelaydC::Resume-Methode: Die Resume-Methode startet eine angehaltene Erfassung neu.'
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: IDelaydC::Resume-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109188"
---
# <a name="idelaydcresume-method"></a>IDelaydC::Resume-Methode

Die **Resume-Methode** startet eine angehaltene Erfassung neu.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                | Beschreibung                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ NOT \_ PAUSED**</dt> </dl> | Die Erfassung wird nicht angehalten. Rufen Sie [**IDelaydC::P ause**](idelaydc-pause.md) auf, um die Erfassung anzuhalten.<br/>                                |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>       | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [**IDelaydC::Connect**](idelaydc-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>         | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [**IDelaydC::Connect-Methode.**](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während die Erfassung angehalten wird, werden der aktuellen [*Erfassungsdatei*](c.md) erst neue Daten hinzugefügt, wenn die **IDelaydC::Resume-Methode** aufgerufen wird, um die Erfassung neu zu starten. Wenn [**Anhalten**](idelaydc-pause.md) und **Fortsetzen** zum Beenden und Neustarten der Erfassung verwendet werden, werden alle erfassten Informationen in derselben Erfassungsdatei gespeichert.

Wenn [**Sie anhalten**](idelaydc-pause.md) und **fortsetzen** verwenden, um die Erfassung zu steuern, fügt Netzwerkmonitor den vorhandenen Statistiken für die aktuelle Erfassung weiterhin [*Konversationsstatistiken*](c.md) hinzu.

Um die Erfassung zu beenden, rufen [**Sie IDelaydC::Stop**](idelaydc-stop.md)auf.

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

[**IDelaydC::Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> </dl>

 

 




