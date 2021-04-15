---
description: Die Pause-Methode hält die aktuelle Erfassung an.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: IESP::P ause-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525118"
---
# <a name="iesppause-method"></a>IESP::P ause-Methode

Die **Pause** -Methode hält die aktuelle Erfassung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpstats* 
</dt> <dd>

Veraltet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung \_ angehalten**</dt> </dl> | Die Erfassung wurde bereits angehalten.<br/>                                                                                     |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl>  | Der NPP erfasst keine Daten. Wenden Sie [iESP:: Start](iesp-start.md) an, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>  | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [iESP:: Connect](iesp-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ ESP**</dt> </dl>        | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden der aktuellen [*Erfassungs Datei*](c.md) keine neuen Daten hinzugefügt, bis Sie die [iESP:: Resume](iesp-resume.md) -Methode zum Neustarten der Erfassung aufgerufen haben. Wenn anhalten und **fortsetzen verwendet** werden, um die Erfassung zu **beenden und neu** zu starten, werden alle erfassten Informationen in derselben Erfassungs Datei abgelegt.

Wenn Sie die **iESP::P ause** -Methode und die **iESP:: Resume** -Methode verwenden, um die Erfassung zu steuern, werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) hinzufügen, sobald die Erfassung ausgeführt wird.

Um die Erfassung neu zu starten, nennen Sie [iESP:: Resume](iesp-resume.md). Um die Erfassung anzuhalten, nennen Sie [iESP:: Beendigung](iesp-stop.md).

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

[IESP:: Resume](iesp-resume.md)
</dt> <dt>

[IESP:: Start](iesp-start.md)
</dt> <dt>

[IESP:: Beendigung](iesp-stop.md)
</dt> </dl>

 

 




