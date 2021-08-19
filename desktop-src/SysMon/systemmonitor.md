---
title: SystemMonitor-Objekt (Isysmon.h)
description: Diese Klasse enthält die Methoden und Eigenschaften, die zum Konfigurieren des Systemmonitor-Steuerelements verwendet werden.
ms.assetid: 5a6195ee-ed89-4f5d-85dd-88cf4a9b5155
keywords:
- SystemMonitor-Objekt SysMon
- SystemMonitor-Objekt SysMon , beschrieben
topic_type:
- apiref
api_name:
- SystemMonitor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b9489c2e966abdf3c329d952a76bd30de487cca99a3e00c8ff46431a163ec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954505"
---
# <a name="systemmonitor-object"></a>SystemMonitor-Objekt

Diese Klasse enthält die Methoden und Eigenschaften, die zum Konfigurieren des Systemmonitor-Steuerelements verwendet werden.

## <a name="members"></a>Member

Das **SystemMonitor-Objekt** verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **SystemMonitor-Objekt** verfügt über diese Ereignisse.



| Ereignis                                                         | Beschreibung                                                                                                                 |
|:--------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**OnCounterAdded**](systemmonitor-oncounteradded.md)        | Benachrichtigt Sie, wenn der [**Counters-Auflistung**](counters.md) ein Zähler hinzugefügt wird.<br/>                             |
| [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)   | Benachrichtigt Sie, bevor ein Indikator aus der [**Counters-Auflistung**](counters.md) gelöscht wird.<br/>                       |
| [**OnCounterSelected**](-systemmonitor-oncounterselected.md) | Benachrichtigt Sie, wenn ein Zähler ausgewählt ist.<br/>                                                                         |
| [**OnDblClick**](-systemmonitor-ondblclick.md)               | Benachrichtigt Sie, wenn ein Benutzer mit der linken Maustaste auf die Diagrammlinie, die Histogrammleiste oder das Berichtselement doppelklickt.<br/> |
| [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) | Benachrichtigt Sie, wenn Beispielwerte für die Leistungsindikatoren erfasst wurden.<br/>                                            |



 

### <a name="methods"></a>Methoden

Das **SystemMonitor-Objekt** verfügt über diese Methoden.



| Methode                                                       | Beschreibung                                                                                                                                                              |
|:-------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchLocking**](systemmonitor-batchinglock.md)           | Sperrt den Systemmonitor, um zu verhindern, dass Leistungsindikatordaten aus der neu hinzugefügten Indikator- oder Protokolldatei stichprobeniert werden.<br/>                                                   |
| [**BrowseCounters**](systemmonitor-browsecounters.md)       | Zeigt das Dialogfeld **Leistungsindikator hinzufügen** an.<br/>                                                                                                                      |
| [**ClearData**](systemmonitor-cleardata.md)                 | Löscht alle Datenfelder im -Steuerelement.<br/>                                                                                                                        |
| [**CollectSample**](systemmonitor-collectsample.md)         | Erfasst einen Wert für jeden Indikator im **Counters-Auflistungsobjekt.**<br/>                                                                                       |
| [**Kopieren**](systemmonitor-copy.md)                           | Kopiert die Eigenschafteneinstellungen, die Liste der Indikatoren und die Indikatordaten des Steuerelements als HTML-Objekt in die Zwischenablage.<br/>                                                |
| [**DisplayProperties**](systemmonitor-displayproperties.md) | Zeigt das Dialogfeld **Graph Eigenschaften** an.<br/>                                                                                                                 |
| [**GetLogViewRange**](systemmonitor-getlogviewrange.md)     | Ruft das Startdatum ab, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird.<br/>                                                                               |
| [**LoadSettings**](systemmonitor-loadsettings.md)           | Fügt dem Systemmonitor die Leistungsindikatoren in der HTML-Vorlagendatei hinzu.<br/>                                                                                            |
| [**Einfügen**](systemmonitor-paste.md)                         | Fügt die Liste der Leistungsindikatoren, die in die Zwischenablage kopiert wurden, an die aktuelle Sammlung von Indikatoren an. <br/>                                                        |
| [**Relog**](systemmonitor-relog.md)                         | Erfasst die Indikatordaten erneut in einer neuen Datei. Sie können diese Methode auch verwenden, um einen neuen Dateityp anzugeben und die Anzahl der in der Protokolldatei enthaltenen Beispiele zu reduzieren.<br/> |
| [**Zurücksetzen**](systemmonitor-reset.md)                         | Entfernt alle [**CounterItem-Objekte**](counteritem.md) aus dem **Counters-Auflistungsobjekt.**<br/>                                                               |
| [**SaveAs**](systemmonitor-saveas.md)                       | Speichert die Indikatorwerte in der Diagrammansicht in einer Protokolldatei.<br/>                                                                                                     |
| [**ScaleToFit**](systemmonitor-scaletofit.md)               | Skalieren Sie Indikatorwerte so, dass sie in das Diagramm passen.<br/>                                                                                                                     |
| [**SetLogViewRange**](systemmonitor-setlogviewrange.md)     | Legt das Startdatum fest, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird.<br/>                                                                                    |
| [**UpdateGraph**](systemmonitor-updategraph.md)             | Aktualisiert den Inhalt der Systemmonitorfenster.<br/>                                                                                                         |



 

### <a name="properties"></a>Eigenschaften

Das **SystemMonitor-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                | Beschreibung                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Darstellung**](systemmonitor-appearance.md)<br/>                               | Ruft die Darstellung des Steuerelements ab, um dreidimensionale Anzeigeeffekte einzu- oder auszulassen, oder legt diese fest.<br/>                                                                                                                        |
| [**Backcolor**](systemmonitor-backcolor.md)<br/>                                 | Ruft die Hintergrundfarbe des Diagramms und der Berichtsansichten ab oder legt diese fest.<br/>                                                                                                                                                        |
| [**BackColorCtl**](systemmonitor-backcolorctl.md)<br/>                           | Ruft die Hintergrundfarbe des Steuerelements ab oder legt diese fest.<br/>                                                                                                                                                                       |
| [**Rahmenart**](systemmonitor-borderstyle.md)<br/>                             | Ruft die Rahmenart des Steuerelements ab oder legt diese fest.<br/>                                                                                                                                                                           |
| [**ChartScroll**](systemmonitor-chartscroll.md)<br/>                             | Ruft einen Wert ab, der bestimmt, ob das Liniendiagramm in der Ansicht scrollt, oder legt diesen fest.<br/>                                                                                                                                             |
| [**Counters**](systemmonitor-counters.md)<br/>                                   | Ruft die Auflistung von [**CounterItem-Objekten**](counteritem.md) ab.<br/>                                                                                                                                                      |
| [**DataPointCount**](systemmonitor-datapointcount.md)<br/>                       | Ruft die Anzahl der in einem Liniendiagramm angezeigten Datenpunkte ab oder legt diese fest.<br/>                                                                                                                                                       |
| [**DataSourceType**](systemmonitor-datasourcetype.md)<br/>                       | Ruft die Quelle der Leistungsindikatordaten ab oder legt sie fest.<br/>                                                                                                                                                                |
| [**DisplayType**](systemmonitor-displaytype.md)<br/>                             | Ruft den Graphtyp ab, der zum Graphen der Leistungsindikatordaten verwendet wird, oder legt diesen fest.<br/>                                                                                                                                              |
| [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)<br/>             | Ruft einen Wert ab, der bestimmt, ob SYSMON beim Anzeigen numerischer Werte die Zifferngruppierung verwendet, oder legt diesen fest.<br/>                                                                                                                      |
| [**EnableToolTips**](systemmonitor-enabletooltips.md)<br/>                       | Ruft einen Wert ab, der bestimmt, ob eine QuickInfo angezeigt wird, wenn der Mauszeiger auf einen Zähler in einer der Diagrammansichten zeigt, oder legt diesen fest.<br/>                                                                                             |
| [**Schriftart**](systemmonitor-font.md)<br/>                                           | Ruft die schriftart ab, die im -Steuerelement verwendet wird, oder legt sie fest.<br/>                                                                                                                                                                              |
| [**ForeColor**](systemmonitor-forecolor.md)<br/>                                 | Ruft die Farbe des Texts ab, der im -Steuerelement angezeigt wird, oder legt diese fest.<br/>                                                                                                                                                         |
| [**GraphTitle**](systemmonitor-graphtitle.md)<br/>                               | Ruft den Titel des Diagramms ab oder legt den Titel fest.<br/>                                                                                                                                                                                    |
| [**GridColor**](systemmonitor-gridcolor.md)<br/>                                 | Ruft die Farbe der im Diagramm verwendeten Rasterlinien ab oder legt diese fest.<br/>                                                                                                                                                             |
| [**Markierung**](systemmonitor-highlight.md)<br/>                                 | Ruft einen Wert ab, der angibt, ob die Werte der ausgewählten Leistungsindikatoren im Diagramm hervorgehoben sind, oder legt einen Wert fest.<br/>                                                                                                               |
| [**LogFileName**](systemmonitor-logfilename.md)<br/>                             | Veraltet. Ruft den Namen einer Protokolldatei ab, die als Quelle der im Systemmonitor angezeigten Indikatorwerte verwendet werden soll, oder legt diesen fest.<br/>                                                                                                   |
| [**LogFiles**](systemmonitor-logfilename.md)<br/>                                | Sammlung einer oder mehrerer Protokolldateien, die als Quelle von Indikatorwerten verwendet werden sollen, die im Systemmonitor angezeigt werden.<br/>                                                                                                                  |
| [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)<br/>               | Ruft den Zeitstempel des frühesten Indikatorwerts aus einem Indikator in Ihrer Indikatorsammlung ab, der in den Protokolldateien protokolliert wurde.<br/>                                                                                           |
| [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)<br/>                 | Ruft den Zeitstempel des letzten Indikatorwerts von einem Indikator in Ihrer Indikatorsammlung ab, der in den Protokolldateien protokolliert wurde.<br/>                                                                                             |
| [**LogViewStart**](systemmonitor-logviewstart.md)<br/>                           | Ruft das Startdatum ab, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird, oder legt dieses fest.<br/>                                                                                                                                      |
| [**LogViewStop**](systemmonitor-logviewstop.md)<br/>                             | Ruft das Enddatum ab, das zum Abrufen von Indikatorwerten aus den Protokolldateien verwendet wird, oder legt dieses fest.<br/>                                                                                                                                        |
| [**ManualUpdate**](systemmonitor-manualupdate.md)<br/>                           | Ruft einen Wert ab, der angibt, ob der Inhalt des Systemmonitors manuell oder automatisch in angegebenen Intervallen aktualisiert wird, oder legt den Wert fest.<br/>                                                                           |
| [**MaximumScale**](systemmonitor-maximumscale.md)<br/>                           | Ruft den maximalen Wert der vertikalen Achse (Y) des Diagramms ab oder legt diese fest.<br/>                                                                                                                                                   |
| [**MinimumScale**](systemmonitor-minimumscale.md)<br/>                           | Ruft den Minimalwert der vertikalen (Y)-Achse des Diagramms ab oder legt diese fest.<br/>                                                                                                                                                   |
| [**MonitorDuplicateInstances**](systemmonitor-monitorduplicateinstances.md)<br/> | Ruft einen Wert ab, der bestimmt, ob mehrere Instanzen eines Zählers überwacht werden können, oder legt diesen fest.<br/>                                                                                                                          |
| [**Readonly**](systemmonitor-readonly.md)<br/>                                   | Ruft einen Wert ab, der bestimmt, ob ein Benutzer die Eigenschaftswerte des Steuerelements ändern kann, oder legt diesen fest.<br/>                                                                                                                      |
| [**ReportValueType**](systemmonitor-reportvaluetype.md)<br/>                     | Ruft einen Wert ab, der bestimmt, ob das Histogramm und die Berichtsansicht den letzten wert, der während des Samplingintervalls entnommen wurde, oder einen berechneten Wert aus der Stichprobenentnahme, z. B. den Durchschnitts- oder Mindestzählerwert, darstellt, oder legt diesen fest.<br/> |
| [**ShowHorizontalGrid**](systemmonitor-showhorizontalgrid.md)<br/>               | Ruft einen Wert ab, der bestimmt, ob horizontale Rasterlinien im Diagramm angezeigt werden, oder legt diesen fest.<br/>                                                                                                                          |
| [**ShowLegend**](systemmonitor-showlegend.md)<br/>                               | Ruft einen Wert ab, der bestimmt, ob die Legende angezeigt wird, oder legt diesen fest.<br/>                                                                                                                                                   |
| [**ShowScaleLabels**](systemmonitor-showscalelabels.md)<br/>                     | Ruft einen Wert ab, der bestimmt, ob die Skalierungsbezeichnungen auf der vertikalen Achse des Diagramms angezeigt werden, oder legt diesen fest.<br/>                                                                                                          |
| [**ShowTimeAxisLabels**](systemmonitor-showtimeaxislabels.md)<br/>               | Ruft einen Wert ab, der bestimmt, ob die horizontale (X)-Achse der Diagrammansicht Bezeichnungen enthält, oder legt diesen fest.<br/>                                                                                                                      |
| [**ShowToolbar**](systemmonitor-showtoolbar.md)<br/>                             | Ruft einen Wert ab, der bestimmt, ob die Symbolleiste auf dem Steuerelement angezeigt wird, oder legt diesen fest.<br/>                                                                                                                                   |
| [**ShowValueBar**](systemmonitor-showvaluebar.md)<br/>                           | Ruft einen Wert ab, der bestimmt, ob der Wertbalken (der Satz statistischer Werte unterhalb des Diagramms) auf dem Steuerelement angezeigt wird, oder legt diesen fest.<br/>                                                                                 |
| [**ShowVerticalGrid**](systemmonitor-showverticalgrid.md)<br/>                   | Ruft einen Wert ab, der bestimmt, ob vertikale Rasterlinien im Diagramm angezeigt werden, oder legt diesen fest.<br/>                                                                                                                            |
| [**SqlDsnName**](systemmonitor-sqldsnname.md)<br/>                               | Ruft den ODBC-Datenquellennamen ab oder legt den Namen fest.<br/>                                                                                                                                                                                 |
| [**SqlLogSetName**](systemmonitor-sqllogsetname.md)<br/>                         | Ruft den Anzeigenamen des Protokollsatzes ab oder legt den Anzeigenamen fest.<br/>                                                                                                                                                                          |
| [**TimeBarColor**](systemmonitor-timebarcolor.md)<br/>                           | Ruft die Farbe der Zeitleiste ab oder legt diese fest (die vertikale Leiste, die sich über das Diagrammfenster bewegt, um den Durchlauf jedes Samplingintervalls in der Liniendiagrammansicht anzugeben).<br/>                                                  |
| [**UpdateInterval**](systemmonitor-updateinterval.md)<br/>                       | Ruft die Zeitspanne ab, die SYSMON wartet, bevor das Diagramm oder der Bericht das nächste Mal aktualisiert wird, oder legt diese fest.<br/>                                                                                                                  |
| [**YAxisLabel**](systemmonitor-yaxislabel.md)<br/>                               | Ruft die Bezeichnung der vertikalen Achse (Y) des Graphen ab oder legt diese fest.<br/>                                                                                                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





