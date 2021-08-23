---
description: Steuerung der Collectorinstanz. Erfordert die Berechtigungen des Administrators (BA).
ms.assetid: 83b485b2-b03b-4882-a3ff-187eac299755
ms.tgt_platform: multiple
title: Control-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5eeccd31f3d9ab1f0b0ec05ebf80ea9f880a73fed21b21fe67fe63257af28871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589020"
---
# <a name="control-class"></a>Control-Klasse

Steuerung der Collectorinstanz. Erfordert die Berechtigungen des Administrators (BA).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Provider("BootEventCollectorWmiProvider"), AMENDMENT]
class Control
{
};
```

## <a name="members"></a>Member

Die **Control-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Control-Klasse** verfügt über diese Methoden.



| Methode                                                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Prüfpunkt**](control-checkpoint.md)                       | Wenn die aktuelle Konfiguration ein Ergebnis von Rückgängig/Wiederholen/Wiederherstellen ist, markiert sie so, als ob sie explizit festgelegt wurde, sodass der Verlauf die Zeit bei der Festlegung beibehalten und bei der nächsten Konfigurationsänderung eine Sicherungsdatei dafür erstellt wird. Wenn die aktuelle Konfiguration bereits explizit festgelegt wurde, hat keine Auswirkungen. Gibt bei Erfolg 1 und bei Fehler 0 zurück.<br/> |
| [**DumpDiagnostics**](control-dumpdiagnostics.md)             | Speichern Sie die Diagnoseinformationen im Protokoll.<br/>                                                                                                                                                                                                                                                                                                                  |
| [**FastShutdown**](control-fastshutdown.md)                   | Beenden Sie den Collector schnell, und verwerfen Sie alle Daten in der Warteschlange.<br/>                                                                                                                                                                                                                                                                                                    |
| [**Leerung**](control-flush.md)                                 | Leeren Sie die Weiterleitungspuffer.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**GetConfiguration**](control-getconfiguration.md)           | Lesen Sie die aktive Konfiguration des Collectors.<br/>                                                                                                                                                                                                                                                                                                                |
| [**IsConfigurationEqual**](control-isconfigurationequal.md)   | Vergleichen Sie das Argument mit der aktiven Konfiguration des Collectors. Gibt 1 zurück, wenn sie übereinstimmen, 0, wenn sie dies nicht tun.<br/>                                                                                                                                                                                                                                                 |
| [**ListBackups**](control-listbackups.md)                     | Gibt die Liste der gespeicherten Sicherungskonfigurationsdateien zurück, die wiederhergestellt werden können.<br/>                                                                                                                                                                                                                                                                                  |
| [**Wiederholen**](control-redo.md)                                   | Setzen Sie die aktive Konfiguration des Collectors aus der späteren Sicherungsdatei zurück (bestimmt durch den aktuellen ursprünglichen Zeitstempel). Wenn die Konfiguration rückgängig gemacht wurde, bedeutet dies, dass die rückgängig gemachte Änderung noch einmal erfolgt. Gibt bei Erfolg 1 und bei Fehler 0 zurück.<br/>                                                                                                    |
| [**RestoreFile**](control-restorefile.md)                     | Stellen Sie die aktive Konfiguration des Collectors aus einer Sicherungsdatei wieder her. Gibt bei Erfolg 1 und bei Fehler 0 zurück.<br/>                                                                                                                                                                                                                                                        |
| [**RestoreFromTime**](control-restorefromtime.md)             | Stellen Sie die aktive Konfiguration des Collectors aus einer Sicherungsdatei wieder her, die durch einen Zeitstempel ausgewählt wurde. Gibt bei Erfolg 1 und bei Fehler 0 zurück.<br/>                                                                                                                                                                                                                               |
| [**SetConfiguration**](control-setconfiguration.md)           | Legen Sie die neue aktive Konfiguration des Collectors fest. Gibt bei Erfolg 1 und bei Fehler 0 zurück.<br/>                                                                                                                                                                                                                                                                           |
| [**Herunterfahren**](control-shutdown.md)                           | Beenden Sie den Collector. Wenn der Collector als Dienst ausgeführt wird, ist das Beenden des Diensts der bessere Ansatz.<br/>                                                                                                                                                                                                                                                     |
| [**Rückgängig**](control-undo.md)                                   | Stellen Sie die aktive Konfiguration des Collectors aus der vorherigen Sicherungsdatei wieder her (bestimmt durch Zurückgehen vom aktuellen ursprünglichen Zeitstempel). Wenn die Konfiguration gerade festgelegt wurde, bedeutet dies, dass diese Änderung rückgängig gemacht wird. Die aufeinanderfolgenden Aufrufe werden auf die früheren und früheren Konfigurationen rückgängig machen. Gibt bei Erfolg 1 und bei Fehler 0 zurück.<br/>                           |
| [**ValidateConfiguration**](control-validateconfiguration.md) | Überprüfen Sie einen Konfigurationstext auf Richtigkeit, ohne ihn aktiv festzulegen. Gibt bei Erfolg 1 und bei Fehler 0 zurück.<br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | \\Stamm-Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

 




