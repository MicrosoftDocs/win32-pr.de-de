---
title: IBackgroundCopyJob-Schnittstelle (Deliveryoptimization.h)
description: Verwenden Sie die IBackgroundCopyJob-Schnittstelle, um dem Auftrag Dateien hinzuzufügen, die Prioritätsebene des Auftrags festzulegen, den Status des Auftrags zu bestimmen und den Auftrag zu starten und zu beenden.
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- IBackgroundCopyJob-Schnittstelle
- IBackgroundCopyJob-Schnittstelle, beschrieben
topic_type:
- apiref
api_name:
- IBackgroundCopyJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27febd08519a06f7ad452882cf0725fed209e0306182ba336343049936795acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543026"
---
# <a name="ibackgroundcopyjob-interface"></a>IBackgroundCopyJob-Schnittstelle

Verwenden Sie [**die IBackgroundCopyJob-Schnittstelle,**](https://www.bing.com/search?q=**IBackgroundCopyJob**) um dem Auftrag Dateien hinzuzufügen, die Prioritätsebene des Auftrags festzulegen, den Status des Auftrags zu bestimmen und den Auftrag zu starten und zu beenden.

Rufen Sie zum Erstellen eines Auftrags die [**IBackgroundCopyManager::CreateJob-Methode**](ibackgroundcopymanager-createjob.md) auf. Um einen [**IBackgroundCopyJob-Schnittstellenzeiger**](https://www.bing.com/search?q=**IBackgroundCopyJob**) auf einen vorhandenen Auftrag abzurufen, rufen Sie die [**IBackgroundCopyManager::GetJob-Methode**](ibackgroundcopymanager-getjob.md) auf.

## <a name="members"></a>Member

Die **IBackgroundCopyJob-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyJob** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IBackgroundCopyJob-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbrechen**](ibackgroundcopyjob-cancel.md)                             | Bricht den Auftrag ab und entfernt temporäre Dateien vom Client.<br/>                                                                                                                                                           |
| [**Abgeschlossen**](ibackgroundcopyjob-complete.md)                         | Beendet den Auftrag und speichert die übertragenen Dateien auf dem Client.<br/>                                                                                                                                                            |
| [**EnumFiles**](ibackgroundcopyjob-enumfiles.md)                       | Gibt einen Schnittstellenzeiger auf ein Enumeratorobjekt zurück, mit dem Sie die Dateien im Auftrag aufzählen.<br/>                                                                                                                   |
| [**GetDisplayName**](ibackgroundcopyjob-getdisplayname.md)             | Ruft den Anzeigenamen ab, der den Auftrag identifiziert.<br/>                                                                                                                                                                    |
| [**GetError**](ibackgroundcopyjob-geterror.md)                         | Ruft einen Schnittstellenzeiger auf das Fehlerobjekt ab, nachdem ein Fehler aufgetreten ist.<br/>                                                                                                                                              |
| [**Getid**](ibackgroundcopyjob-getid.md)                               | Ruft den Bezeichner des Auftrags in der Warteschlange ab.<br/>                                                                                                                                                                      |
| [**GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | Ruft die Zeitdauer ab, die DO weiterhin versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehlerzustand aufgetreten ist.<br/>                                                                                             |
| [**GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)             | Ruft die Ereignisbenachrichtigungsflags (Rückruf) ab, die Sie für Ihre Anwendung festgelegt haben.<br/>                                                                                                                                   |
| [**GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)     | Ruft einen Zeiger auf Ihre Implementierung der [**IBackgroundCopyCallback-Schnittstelle**](ibackgroundcopycallback.md) (Rückrufe) ab.<br/>                                                                                    |
| [**GetPriority**](ibackgroundcopyjob-getpriority.md)                   | Ruft die Prioritätsebene ab, die Sie für den Auftrag festgelegt haben.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Ruft auftragsbezogene Statusinformationen ab, z. B. die Anzahl von Bytes und Dateien, die an den Client übertragen werden.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Ruft den Status des Auftrags ab.<br/>                                                                                                                                                                                        |
| [**GetTimes**](ibackgroundcopyjob-gettimes.md)                         | Ruft Zeitstempel für Aktivitäten im Zusammenhang mit dem Auftrag ab, z. B. die Zeit, zu der der Auftrag erstellt wurde.<br/>                                                                                                                         |
| [**Gettype**](ibackgroundcopyjob-gettype.md)                           | Ruft den Typ der ausgeführten Übertragung ab, z. B. einen Dateidownload.<br/>                                                                                                                                               |
| [**Fortsetzen**](ibackgroundcopyjob-resume.md)                             | Startet einen neuen Auftrag oder startet einen angehaltenen Auftrag neu.<br/>                                                                                                                                                                          |
| [**SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | Gibt den Zeitraum an, für den DO weiterhin versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehlerzustand aufgetreten ist.<br/>                                                                                             |
| [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)             | Gibt den Typ der zu empfangenden Ereignisbenachrichtigung an.<br/>                                                                                                                                                                   |
| [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)     | Gibt einen Zeiger auf Ihre Implementierung der [**IBackgroundCopyCallback-Schnittstelle**](ibackgroundcopycallback.md) (Rückrufe) an. Die Schnittstelle empfängt Benachrichtigungen basierend auf den von Ihnen festgelegten Ereignisbenachrichtigungsflags.<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | Gibt die Priorität des Auftrags relativ zu anderen Aufträgen in der Übertragungswarteschlange an.<br/>                                                                                                                                        |
| [**Angehalten**](ibackgroundcopyjob-suspend.md)                           | Hält den Auftrag an.<br/>                                                                                                                                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668D37-507E-4160-9316-26306D150B12 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> </dl>

 

