---
description: In der msiserviceconfigfailureactions-Tabelle sind die Vorgänge aufgeführt, die ausgeführt werden, nachdem ein Dienst fehlgeschlagen ist. Die in dieser Tabelle angegebenen Vorgänge werden beim nächsten Start des Systems ausgeführt.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Msiserviceconfigfailureactions-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353868"
---
# <a name="msiserviceconfigfailureactions-table"></a>Msiserviceconfigfailureactions-Tabelle

In der msiserviceconfigfailureactions-Tabelle sind die Vorgänge aufgeführt, die ausgeführt werden, nachdem ein Dienst fehlgeschlagen ist. Die in dieser Tabelle angegebenen Vorgänge werden beim nächsten Start des Systems ausgeführt.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 5,0 verfügbar.

Die msiserviceconfigfailureactions-Tabelle weist die folgenden Spalten auf.



| Spalte                         | Typ                         | Schlüssel | Nullwerte zulässig |
|--------------------------------|------------------------------|-----|----------|
| Msiserviceconfigfailureactions | [Bezeichner](identifier.md) | J   | N        |
| Name                           | [Großformatige](formatted.md)   | N   | N        |
| Ereignis                          | [Integer](integer.md)       | N   | N        |
| Resetperiod                    | [Integer](integer.md)       | N   | J        |
| Rebootmessage                  | [Großformatige](formatted.md)   | N   | J        |
| Get-Help                        | [Großformatige](formatted.md)   | N   | J        |
| Aktionen                        | [Text](text.md)             | N   | J        |
| Delta Actions                   | [Text](text.md)             | N   | J        |
| Komponente\_                    | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>Msiserviceconfigfailureactions
</dt> <dd>

Dies ist der Primärschlüssel dieser Tabelle, der eine Fehler Aktion identifiziert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Diese Spalte enthält den Namen eines dienstanteils, der Teil dieses Pakets ist oder bereits installiert ist.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter
</dt> <dd>

Diese Spalte gibt an, wann die Konfiguration des Dienstanbieter geändert werden soll. Die folgenden Werte sind Bitfelder, die kombiniert werden können, um mehrere Vorgänge darzustellen. Alle anderen Bitfeldwerte werden ignoriert.



| Konstante                                         | BESCHREIBUNG                                     |
|--------------------------------------------------|-------------------------------------------------|
| **msidbserviceconfgeventinstall** 1<br/>   | Änderung während der Installation der Komponente.    |
| **msidbserviceconfgeventuninstall** 2<br/> | Änderung während der deinstalstallation der Komponente.  |
| **msidbserviceconfgeventreinstall** 4<br/> | Änderung während der erneuten Installation der Komponente. |



 

</dd> <dt>

<span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>Resetperiod
</dt> <dd>

Der Zurücksetzungs Zeitraum (in Sekunden) der Fehler Anzahl für den Dienst. Der [Dienststeuerungs-Manager (Service Control Manager](../services/service-control-manager.md) , SCM) zählt, wie oft der Dienst seit dem letzten Neustart des Systems fehlgeschlagen ist. Die Anzahl wird auf 0 (null) zurückgesetzt, wenn der Dienst für den Zurücksetzungs Zeitraum nicht ausfällt. Wenn der Dienst für die n-te Zeit fehlschlägt, führt das System die Aktion aus, die im \[ -Element N-1 des Arrays angegeben ist, das \] im Aktionsfeld angegeben ist.

Lassen Sie das Feld resetperiod leer, um anzugeben, dass die Fehler Anzahl nie zurückgesetzt werden sollte.

</dd> <dt>

<span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>Rebootmessage
</dt> <dd>

Die Nachricht, die vor dem Neustart des Computers als Reaktion auf eine Aktion **zum \_ \_ Neustart der SC-Aktion** gesendet wurde, die in der Spalte Aktionen angegeben wurde. Sie können eine leere Zeichenfolge ("") verwenden, um die aktuelle Nachricht unverändert zu senden. Sie können \[ ~ \] die Syntax des [formatierten](formatted.md) Datentyps verwenden, um die aktuelle Nachricht zu löschen und keine Nachricht zu senden.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>S
</dt> <dd>

Die Befehlszeile, die von dem Prozess ausgeführt wird [**, der von der Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) up" als Antwort auf eine Aktion zum **Ausführen eines SC- \_ Aktions \_ \_ Befehls** erstellt wurde. Der neue Prozess wird unter dem gleichen Konto ausgeführt wie der Dienst und nur dann, wenn das Aktionsfeld den **\_ \_ \_ Befehl SC Action Run** hat. Sie können eine leere Zeichenfolge ("") verwenden, um die aktuelle Befehlszeile unverändert zu verwenden. Sie können \[ ~ \] die Syntax des [formatierten](formatted.md) Datentyps verwenden, um die aktuelle Befehlszeile zu löschen und keinen Vorgang auszuführen, wenn der Dienst fehlschlägt.

</dd> <dt>

<span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Handlungs
</dt> <dd>

Dieses Feld enthält ein Array von ganzzahligen Werten, die die Aktionen angeben, die vom SCM durchgeführt werden, wenn der Dienst fehlschlägt. Trennen Sie die Werte im Array durch \[ ~ \] . Der ganzzahlige Wert im Nth-Element des Arrays gibt die Aktion an, die ausgeführt wird, wenn der Dienst für die n-te Zeit fehlschlägt. Jeder Member des Arrays ist einer der folgenden ganzzahligen Werte.



| Konstante                                 | BESCHREIBUNG           |
|------------------------------------------|-----------------------|
| **SC \_ Aktion " \_ None** 0"<br/>         | Keine Aktion.            |
| **SC \_ Aktions \_ Neustart** 2<br/>       | Starten Sie den Computer neu. |
| **SC \_ Aktion \_ neu starten** 1<br/>      | Starten Sie den Dienst neu.  |
| **SC \_ \_ \_ Befehl zum Ausführen von Aktionen** 3<br/> | Führen Sie einen Befehl aus.        |



 

</dd> <dt>

<span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>Delta Actions
</dt> <dd>

Dieses Feld enthält ein Array von ganzzahligen Werten, die die Zeit in Millisekunden angeben, die gewartet werden soll, bevor die in der Aktionsspalte angegebene Aktion durchgeführt wird. Trennen Sie die Werte im Array durch \[ ~ \] . Die Anzahl der Elemente im delayactions-Array muss gleich der Anzahl der Elemente im Aktions Array sein. Das n-te Element des delayactions-Arrays gibt die Zeitverzögerung für das n-te Element des Aktions Arrays an.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel für Spalte einer der [Komponenten Tabellen](component-table.md).

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE102](ice-102.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 
