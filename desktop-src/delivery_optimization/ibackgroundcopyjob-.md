---
title: Ibackgroundcopyjob-Schnittstelle (deliveryoptimization. h)
description: Verwenden Sie die ibackgroundcopyjob-Schnittstelle, um dem Auftrag Dateien hinzuzufügen, die Prioritätsstufe des Auftrags festzulegen, den Status des Auftrags zu ermitteln und den Auftrag zu starten und anzuhalten.
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- Ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, beschrieben
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
ms.openlocfilehash: 04572f11afd51c3354c5adabd9950e2a3942287a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040518"
---
# <a name="ibackgroundcopyjob-interface"></a>Ibackgroundcopyjob-Schnittstelle

Verwenden Sie die [**ibackgroundcopyjob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) -Schnittstelle, um dem Auftrag Dateien hinzuzufügen, die Prioritätsstufe des Auftrags festzulegen, den Status des Auftrags zu ermitteln und den Auftrag zu starten und anzuhalten.

Um einen Auftrag zu erstellen, rufen Sie die [**ibackgroundcopymanager:: kreatejob**](ibackgroundcopymanager-createjob.md) -Methode auf. Um einen [**ibackgroundcopyjob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) -Schnittstellen Zeiger auf einen vorhandenen Auftrag abzurufen, müssen Sie die [**ibackgroundcopymanager:: GetJob**](ibackgroundcopymanager-getjob.md) -Methode aufrufen.

## <a name="members"></a>Member

Die **ibackgroundcopyjob** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ibackgroundcopyjob** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ibackgroundcopyjob** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbrechen**](ibackgroundcopyjob-cancel.md)                             | Bricht den Auftrag ab und entfernt temporäre Dateien vom Client.<br/>                                                                                                                                                           |
| [**Abgeschlossen**](ibackgroundcopyjob-complete.md)                         | Beendet den Auftrag und speichert die übertragenen Dateien auf dem Client.<br/>                                                                                                                                                            |
| [**EnumFiles**](ibackgroundcopyjob-enumfiles.md)                       | Gibt einen Schnittstellen Zeiger auf ein Enumeratorobjekt zurück, das Sie verwenden, um die Dateien im Auftrag aufzuzählen.<br/>                                                                                                                   |
| [**GetDisplayName**](ibackgroundcopyjob-getdisplayname.md)             | Ruft den anzeigen Amen ab, der den Auftrag identifiziert.<br/>                                                                                                                                                                    |
| [**GetError**](ibackgroundcopyjob-geterror.md)                         | Ruft einen Schnittstellen Zeiger auf das Fehler Objekt ab, nachdem ein Fehler aufgetreten ist.<br/>                                                                                                                                              |
| [**GetId**](ibackgroundcopyjob-getid.md)                               | Ruft den Bezeichner des Auftrags in der Warteschlange ab.<br/>                                                                                                                                                                      |
| [**Getnoprogresstimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | Ruft die Zeitspanne ab, die nach dem Auftreten eines vorübergehenden Fehler Zustands weiterhin versucht, die Datei zu übertragen.<br/>                                                                                             |
| [**Getnotifyflags**](ibackgroundcopyjob-getnotifyflags.md)             | Ruft die Ereignis Benachrichtigungs Flags (Rückruf) ab, die Sie für Ihre Anwendung festgelegt haben.<br/>                                                                                                                                   |
| [**Getnotifyinterface**](ibackgroundcopyjob-getnotifyinterface.md)     | Ruft einen Zeiger auf Ihre Implementierung der [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle (Rückrufe) ab.<br/>                                                                                    |
| [**GetPriority**](ibackgroundcopyjob-getpriority.md)                   | Ruft die Prioritätsstufe ab, die Sie für den Auftrag festgelegt haben.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Ruft auftragsbezogene Statusinformationen ab, wie z. b. die Anzahl von Bytes und Dateien, die an den Client übertragen werden.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Ruft den Status des Auftrags ab.<br/>                                                                                                                                                                                        |
| [**Gettimes**](ibackgroundcopyjob-gettimes.md)                         | Ruft Zeitstempel für Aktivitäten im Zusammenhang mit dem Auftrag ab, wie z. b. den Zeitpunkt, zu dem der Auftrag erstellt wurde.<br/>                                                                                                                         |
| [**GetType**](ibackgroundcopyjob-gettype.md)                           | Ruft den Typ der Übertragung ab, z. b. einen Datei Download.<br/>                                                                                                                                               |
| [**Fortsetzen**](ibackgroundcopyjob-resume.md)                             | Startet einen neuen Auftrag oder startet einen angehaltenen Auftrag neu.<br/>                                                                                                                                                                          |
| [**Setnoprogresstimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | Gibt an, wie lange versucht wird, die Datei zu übertragen, nachdem ein vorübergehender Fehler aufgetreten ist.<br/>                                                                                             |
| [**Setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md)             | Gibt den Typ der zu empfangenden Ereignis Benachrichtigung an.<br/>                                                                                                                                                                   |
| [**Setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md)     | Gibt einen Zeiger auf die Implementierung der [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle (Rückrufe) an. Die-Schnittstelle empfängt eine Benachrichtigung auf der Grundlage der festgelegten ereignisbenachrichtigungsflags.<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | Gibt die Priorität des Auftrags relativ zu anderen Aufträgen in der Übertragungs Warteschlange an.<br/>                                                                                                                                        |
| [**Angehalten**](ibackgroundcopyjob-suspend.md)                           | Hält den Auftrag an.<br/>                                                                                                                                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyfile**](ibackgroundcopyfile.md)
</dt> <dt>

[**Ibackgroundcopymanager**](ibackgroundcopymanager.md)
</dt> </dl>

 

