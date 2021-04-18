---
description: Die Start-Methode startet eine Aufzeichnung.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'IESP:: Start-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347922"
---
# <a name="iespstart-method"></a>IESP:: Start-Methode

Die **Start** -Methode startet eine Aufzeichnung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfilename* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Namen der [*Erfassungs Datei*](c.md) , in der die Netzwerkdaten gespeichert werden. Stellen Sie sicher, dass der Dateiname zwischengespeichert wird, wenn er für den zukünftigen Verweis benötigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung \_ angehalten**</dt> </dl> | Die Erfassung wird angehalten und muss beendet werden, bevor Sie neu gestartet werden kann. Wenden Sie [iESP:: Beendigung](iesp-stop.md) an, um die Erfassung anzuhalten.<br/> |
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>       | Die Erfassung wurde bereits gestartet.<br/>                                                                                             |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>  | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [iESP:: Connect](iesp-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.<br/>          |
| <dl> <dt>**nmerr \_ nicht \_ ESP**</dt> </dl>        | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.<br/>                              |



 

## <a name="remarks"></a>Bemerkungen

Der Speicherort der [*Erfassungs Datei*](c.md) wird in der Windows-Registrierung angegeben, aber Sie können Netzwerkmonitor verwenden, um den Speicherort des Verzeichnisses zu ändern.

Wenn Sie die Erfassung mit den Methoden iESP:: Start und [iESP:: beenden](iesp-stop.md) neu starten, müssen Sie die Methode [iESP:: Configure](iesp-configure.md) zum erneuten Konfigurieren der Verbindung mit jedem Aufruf von iESP:: Start zum Neustarten der Datenerfassung verwenden. Wenn Sie die Erfassung mit diesen drei Methoden starten und beenden, wird jedes Mal eine neue Erfassungs Datei erstellt, wenn die Erfassung gestartet wird.

> [!Note]  
> Sie können die Erfassung auch starten und Abbrechen, indem Sie die [iESP::P ause](iesp-pause.md) -Methode und die [iESP:: Resume](iesp-resume.md) -Methode verwenden. Wenn diese beiden Methoden verwendet werden, werden die erfassten Daten in derselben Erfassungs Datei gespeichert.

 

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

[IESP:: Configure](iesp-configure.md)
</dt> <dt>

[IESP:: Connect](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP:: Resume](iesp-resume.md)
</dt> <dt>

[IESP:: Beendigung](iesp-stop.md)
</dt> </dl>

 

 




