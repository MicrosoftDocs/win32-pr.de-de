---
description: Steuerung der Collector-Instanz. Erfordert die Administrator Rechte (BA).
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
ms.openlocfilehash: 2681af7425fd5cacf88375e11e4658e5d4b1a2c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522912"
---
# <a name="control-class"></a>Control-Klasse

Steuerung der Collector-Instanz. Erfordert die Administrator Rechte (BA).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Provider("BootEventCollectorWmiProvider"), AMENDMENT]
class Control
{
};
```

## <a name="members"></a>Member

Die **Steuer** Element Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Steuer** Element Klasse verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kal**](control-checkpoint.md)                       | Wenn die aktuelle Konfiguration das Ergebnis der rückgängig/Wiederherstellung/Wiederherstellung ist, kennzeichnet Sie diese als explizit festgelegt, sodass der Verlauf den Zeitpunkt der Festlegung beibehält und bei der nächsten Konfigurationsänderung eine Sicherungsdatei erstellt wird. Wenn die aktuelle Konfiguration bereits explizit festgelegt wurde, hat keine Auswirkungen. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.<br/> |
| [**Dumpdiagnostics**](control-dumpdiagnostics.md)             | Sichern Sie die Diagnoseinformationen im Protokoll.<br/>                                                                                                                                                                                                                                                                                                                  |
| [**Fastshutdown**](control-fastshutdown.md)                   | Hält den Collector schnell an, wobei alle Daten in der Warteschlange verworfen werden.<br/>                                                                                                                                                                                                                                                                                                    |
| [**Leerung**](control-flush.md)                                 | Leert die Weiterleitungs Puffer.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**GetConfiguration**](control-getconfiguration.md)           | Lesen Sie die aktive Konfiguration des Sammlers.<br/>                                                                                                                                                                                                                                                                                                                |
| [**Isconfigurationequal**](control-isconfigurationequal.md)   | Vergleichen Sie das-Argument mit der aktiven Konfiguration des Sammlers. Gibt 1 zurück, wenn Sie einander entsprechen. andernfalls wird 0 zurückgegeben.<br/>                                                                                                                                                                                                                                                 |
| [**Listbackups**](control-listbackups.md)                     | Gibt die Liste der gespeicherten Sicherungs Konfigurationsdateien zurück, die wieder hergestellt werden können.<br/>                                                                                                                                                                                                                                                                                  |
| [**Wiederholen**](control-redo.md)                                   | Setzt die aktive Konfiguration des Sammlers aus der späteren Sicherungsdatei zurück (festgelegt durch Weiterleiten vom aktuellen ursprünglichen Zeitstempel). Wenn die Konfiguration rückgängig gemacht wurde, bedeutet dies, dass die rückgängig gemachte Änderung rückgängig gemacht wird. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.<br/>                                                                                                    |
| [**Restorefile**](control-restorefile.md)                     | Stellen Sie die aktive Konfiguration des Sammlers aus einer Sicherungsdatei wieder her. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.<br/>                                                                                                                                                                                                                                                        |
| [**Restorefromtime**](control-restorefromtime.md)             | Stellen Sie die aktive Konfiguration des Sammlers aus einer Sicherungsdatei wieder her, die durch einen Zeitstempel ausgewählt wird. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.<br/>                                                                                                                                                                                                                               |
| [**SetConfiguration**](control-setconfiguration.md)           | Legen Sie die neue aktive Konfiguration des Sammlers fest. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.<br/>                                                                                                                                                                                                                                                                           |
| [**Abschlusses**](control-shutdown.md)                           | Stoppt den Collector. Wenn der Collector als Dienst ausgeführt wird, ist das Beenden des Dienstanbieter der bessere Ansatz.<br/>                                                                                                                                                                                                                                                     |
| [**Rückgängig**](control-undo.md)                                   | Stellen Sie die aktive Konfiguration des Sammlers aus der vorherigen Sicherungsdatei wieder her (festgelegt durch zurückkehren vom aktuellen ursprünglichen Zeitstempel). Wenn die Konfiguration gerade festgelegt wurde, bedeutet dies, dass diese Änderung nicht mehr durchgeführt werden muss. Die aufeinander folgenden Aufrufe werden in früheren und früheren Konfigurationen rückgängig gemacht. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.<br/>                           |
| [**Validateconfiguration**](control-validateconfiguration.md) | Überprüfen Sie einen Konfigurations Text auf Richtigkeit, ohne ihn als aktiv festzulegen. Gibt bei Erfolg den Wert 1 zurück, 0 bei Fehler.<br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Stammverzeichnis von \\ Microsoft \\ Windows \\ booteventcollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>Booteventcollector WMI. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

 




