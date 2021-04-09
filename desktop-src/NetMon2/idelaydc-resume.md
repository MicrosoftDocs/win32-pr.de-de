---
description: Mit der Resume-Methode wird eine angehaltene Erfassung neu gestartet.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'Idelta aydc:: Resume-Methode (Netmon. h)'
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
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750057"
---
# <a name="idelaydcresume-method"></a>Idelta aydc:: Resume-Methode

Mit der **Resume** -Methode wird eine angehaltene Erfassung neu gestartet.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                | Beschreibung                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung wurde \_ nicht \_ angehalten.**</dt> </dl> | Die Erfassung wird nicht angehalten. Wenden Sie [**idelta DC::P ause**](idelaydc-pause.md) an, um die Erfassung anzuhalten.<br/>                                |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>       | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [**idelta-DC:: Connect**](idelaydc-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ verzögert**</dt> </dl>         | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**idelta aydc:: Connect**](idelaydc-connect.md) -Methode.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während die Erfassung angehalten wird, werden neue Daten erst zur aktuellen [*Erfassungs Datei*](c.md) hinzugefügt, wenn die **idelta-DC:: Resume** -Methode aufgerufen wird, um die Erfassung neu zu starten. Wenn anhalten und **fortsetzen verwendet** werden, um die Erfassung zu [**beenden und neu**](idelaydc-pause.md) zu starten, werden alle erfassten Informationen in derselben Erfassungs Datei abgelegt.

Bei der [**Verwendung**](idelaydc-pause.md) von **Anhalten und fort** setzen zur Steuerung der Erfassung werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) zu den vorhandenen Statistiken für die aktuelle Erfassung hinzufügen.

Um die Erfassung anzuhalten, nennen Sie [**idelta aydc:: Stop.**](idelaydc-stop.md)

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

[**Idelta aydc:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**Idelta aydc::P ause**](idelaydc-pause.md)
</dt> <dt>

[**Idelta aydc:: Beendigung**](idelaydc-stop.md)
</dt> </dl>

 

 




