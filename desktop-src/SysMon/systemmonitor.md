---
title: Systemmonitor-Objekt (isysmon. h)
description: Diese Klasse enthält die Methoden und Eigenschaften, die zum Konfigurieren des System Monitor-Steuer Elements verwendet werden.
ms.assetid: 5a6195ee-ed89-4f5d-85dd-88cf4a9b5155
keywords:
- Systemmonitor-Objekt-sysmon
- Systemmonitor-Objekt (Sysmon), beschrieben
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
ms.openlocfilehash: 297f0e3e67134f911932aa7784396c244dc79f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338340"
---
# <a name="systemmonitor-object"></a>Systemmonitor-Objekt

Diese Klasse enthält die Methoden und Eigenschaften, die zum Konfigurieren des System Monitor-Steuer Elements verwendet werden.

## <a name="members"></a>Member

Das **Systemmonitor** -Objekt verfügt über folgende Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **Systemmonitor** -Objekt enthält diese Ereignisse.



| Ereignis                                                         | BESCHREIBUNG                                                                                                                 |
|:--------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Oncounteradded**](systemmonitor-oncounteradded.md)        | Benachrichtigt Sie, wenn der [**Zähler**](counters.md) Sammlung ein Indikator hinzugefügt wird.<br/>                             |
| [**Oncounterdeleted**](-systemmonitor-oncounterdeleted.md)   | Benachrichtigt Sie, bevor ein Indikator aus der [**Zähler**](counters.md) Sammlung gelöscht wird.<br/>                       |
| [**Oncounterselected**](-systemmonitor-oncounterselected.md) | Benachrichtigt Sie, wenn ein Counter ausgewählt wird.<br/>                                                                         |
| [**Ondblclick**](-systemmonitor-ondblclick.md)               | Benachrichtigt Sie, wenn ein Benutzer mit der linken Maustaste auf die Diagramm Linie, die Histogrammleiste oder das Berichts Element doppelklickt.<br/> |
| [**Onsamplecollected**](-systemmonitor-onsamplecollected.md) | Benachrichtigt Sie, wenn Beispiel Werte für die Leistungsindikatoren erfasst wurden.<br/>                                            |



 

### <a name="methods"></a>Methoden

Das **Systemmonitor** -Objekt verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                                                                              |
|:-------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Batch Sperren**](systemmonitor-batchinglock.md)           | Sperrt den System Monitor, um zu verhindern, dass die Stichprobenentnahme von Daten aus dem neu hinzugefügten Wert oder der neuen Protokolldatei<br/>                                                   |
| [**Browsen**](systemmonitor-browsecounters.md)       | Zeigt das Dialogfeld zum **Hinzufügen eines Zählers** an.<br/>                                                                                                                      |
| [**ClearData**](systemmonitor-cleardata.md)                 | Löscht alle Datenfelder im-Steuerelement.<br/>                                                                                                                        |
| [**Collectsample**](systemmonitor-collectsample.md)         | Gibt einen Wert für **jeden Zähler im indikatorensammlungs Objekt** aus.<br/>                                                                                       |
| [**Kopieren**](systemmonitor-copy.md)                           | Kopiert die Eigenschafts Einstellungen des Steuer Elements, die Liste der Leistungsindikatoren und die Indikator Daten als HTML-Objekt in die Zwischenablage.<br/>                                                |
| [**DisplayProperties**](systemmonitor-displayproperties.md) | Zeigt das Dialogfeld **Diagramm Eigenschaften** an.<br/>                                                                                                                 |
| [**Getlogviewrange**](systemmonitor-getlogviewrange.md)     | Ruft das Startdatum ab, das zum Abrufen von Counter-Werten aus den Protokolldateien verwendet wird.<br/>                                                                               |
| [**LoadSettings**](systemmonitor-loadsettings.md)           | Fügt dem System Monitor die Indikatoren in der HTML-Vorlagen Datei hinzu.<br/>                                                                                            |
| [**Einfügen**](systemmonitor-paste.md)                         | Fügt die Liste der Indikatoren, die in die Zwischenablage kopiert wurden, der aktuellen Auflistung von Indikatoren hinzu. <br/>                                                        |
| [**Erneut aufzuzeichnen**](systemmonitor-relog.md)                         | Protokolliert die Daten des Zählers erneut in einer neuen Datei. Sie können diese Methode auch verwenden, um einen neuen Dateityp anzugeben und die Anzahl der in der Protokolldatei enthaltenen Beispiele zu verringern.<br/> |
| [**Zurücksetzen**](systemmonitor-reset.md)                         | Entfernt alle [**zähltem**](counteritem.md) -Objekte **aus dem** indikatorensammlungs Objekt.<br/>                                                               |
| [**SaveAs**](systemmonitor-saveas.md)                       | Speichert die Werte der Werte in der Diagramm Ansicht in einer Protokolldatei.<br/>                                                                                                     |
| [**Scaleum anpassen**](systemmonitor-scaletofit.md)               | Skalierungs Wert Werte, die in das Diagramm passen.<br/>                                                                                                                     |
| [**Setlogviewrange**](systemmonitor-setlogviewrange.md)     | Legt das Startdatum fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.<br/>                                                                                    |
| [**Updategraph**](systemmonitor-updategraph.md)             | Aktualisiert den Inhalt der System Monitor Fenster.<br/>                                                                                                         |



 

### <a name="properties"></a>Eigenschaften

Das **Systemmonitor** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                                | BESCHREIBUNG                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Darstellung**](systemmonitor-appearance.md)<br/>                               | Ruft die Darstellung des Steuer Elements ab oder legt diese fest, um dreidimensionale Anzeige Effekte einzuschließen oder auszulassen.<br/>                                                                                                                        |
| [**BackColor**](systemmonitor-backcolor.md)<br/>                                 | Ruft die Hintergrundfarbe des Diagramms und der Berichts Ansichten ab oder legt Sie fest.<br/>                                                                                                                                                        |
| [**Backcolorctl**](systemmonitor-backcolorctl.md)<br/>                           | Ruft die Hintergrundfarbe des Steuer Elements ab oder legt diese fest.<br/>                                                                                                                                                                       |
| [**Rahmenart**](systemmonitor-borderstyle.md)<br/>                             | Ruft die Rahmenart des Steuer Elements ab oder legt diese fest.<br/>                                                                                                                                                                           |
| [**Chartscroll**](systemmonitor-chartscroll.md)<br/>                             | Ruft einen Wert ab, der bestimmt, ob das Liniendiagramm in der Ansicht einen Bildlauf ausführt, oder legt diesen fest<br/>                                                                                                                                             |
| [**Counters**](systemmonitor-counters.md)<br/>                                   | Ruft die Auflistung der- [**Objekte ab**](counteritem.md) .<br/>                                                                                                                                                      |
| [**Datapointcount**](systemmonitor-datapointcount.md)<br/>                       | Ruft die Anzahl der Datenpunkte ab, die in einem Liniendiagramm angezeigt werden, oder legt Sie fest.<br/>                                                                                                                                                       |
| [**DataSourceType**](systemmonitor-datasourcetype.md)<br/>                       | Ruft die Quelle der Leistungsdaten des Leistungsindikators ab oder legt Sie fest.<br/>                                                                                                                                                                |
| [**Display Type**](systemmonitor-displaytype.md)<br/>                             | Ruft den Diagrammtyp ab, der zum Diagramm der Leistungs Indikatorendaten verwendet wird, oder legt ihn fest.<br/>                                                                                                                                              |
| [**Enabledigit-Gruppierung**](systemmonitor-enabledigitgrouping.md)<br/>             | Ruft einen Wert ab, der bestimmt, ob sysmon eine Ziffern Gruppierung verwendet, wenn numerische Werte angezeigt werden, oder legt ihn fest.<br/>                                                                                                                      |
| [**EnableToolTips**](systemmonitor-enabletooltips.md)<br/>                       | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob eine QuickInfo angezeigt wird, wenn der Mauszeiger über einen Leistungsindikators in einer der Diagramm Ansichten bewegt wird.<br/>                                                                                             |
| [**Raster**](systemmonitor-font.md)<br/>                                           | Ruft die im-Steuerelement verwendete Schriftart ab oder legt Sie fest.<br/>                                                                                                                                                                              |
| [**ForeColor**](systemmonitor-forecolor.md)<br/>                                 | Ruft die Farbe des Texts ab, der im-Steuerelement angezeigt wird, oder legt diese fest.<br/>                                                                                                                                                         |
| [**Graphtitle**](systemmonitor-graphtitle.md)<br/>                               | Ruft den Titel des Diagramms ab oder legt ihn fest.<br/>                                                                                                                                                                                    |
| [**GridColor**](systemmonitor-gridcolor.md)<br/>                                 | Ruft die Farbe der im Diagramm verwendeten Rasterlinien ab oder legt Sie fest.<br/>                                                                                                                                                             |
| [**Markierung**](systemmonitor-highlight.md)<br/>                                 | Ruft einen Wert ab, der angibt, ob die Werte der ausgewählten Indikatoren im Diagramm hervorgehoben sind, oder legt diesen fest.<br/>                                                                                                               |
| [**Protokoll Dateiname**](systemmonitor-logfilename.md)<br/>                             | Veraltet. Ruft den Namen einer Protokolldatei ab, die als Quelle der im System Monitor angezeigten Indikatorenwerte verwendet werden soll, oder legt ihn fest.<br/>                                                                                                   |
| [**LogFiles**](systemmonitor-logfilename.md)<br/>                                | Sammlung von einer oder mehreren Protokolldateien, die als Quelle der im System Monitor angezeigten Indikatoren verwendet werden sollen.<br/>                                                                                                                  |
| [**Logsourcestarttime**](systemmonitor-logsourcestarttime.md)<br/>               | Ruft den Zeitstempel des frühesten Leistungs Zählers von einem Leistungs-in der Leistungsdaten Sammlung ab, der in den Protokolldateien protokolliert wurde.<br/>                                                                                           |
| [**Logsourcestoptime**](systemmonitor-logsourcestoptime.md)<br/>                 | Ruft den Zeitstempel des letzten Leistungs Zählers von einem Leistungs-in der Leistungsdaten Sammlung ab, der in den Protokolldateien protokolliert wurde.<br/>                                                                                             |
| [**Logviewstart**](systemmonitor-logviewstart.md)<br/>                           | Ruft das Startdatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.<br/>                                                                                                                                      |
| [**Logviewstoppt**](systemmonitor-logviewstop.md)<br/>                             | Ruft das Enddatum ab oder legt dieses fest, das zum Abrufen von indikatorenwerten aus den Protokolldateien verwendet wird.<br/>                                                                                                                                        |
| [**ManualUpdate**](systemmonitor-manualupdate.md)<br/>                           | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der Inhalt des System Monitors manuell oder in angegebenen Intervallen automatisch aktualisiert wird.<br/>                                                                           |
| [**MaximumScale**](systemmonitor-maximumscale.md)<br/>                           | Ruft den maximalen Wert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.<br/>                                                                                                                                                   |
| [**MinimumScale**](systemmonitor-minimumscale.md)<br/>                           | Ruft den Mindestwert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.<br/>                                                                                                                                                   |
| [**Monitordupli-Einhaltungen**](systemmonitor-monitorduplicateinstances.md)<br/> | Ruft einen Wert ab, der bestimmt, ob mehrere Instanzen eines Leistungsindikators überwacht werden können, oder legt ihn fest.<br/>                                                                                                                          |
| [**ReadOnly**](systemmonitor-readonly.md)<br/>                                   | Ruft einen Wert ab, der bestimmt, ob ein Benutzer die Eigenschaftswerte des Steuer Elements ändern kann, oder legt diesen fest.<br/>                                                                                                                      |
| [**Report ValueType**](systemmonitor-reportvaluetype.md)<br/>                     | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob im Histogramm und in den Berichts Ansichten der letzte Wert, der während des Samplingintervalls Stichprobe oder ein berechneter Wert aus der Stichprobe erfasst wurde<br/> |
| [**Showhorizontalgrid**](systemmonitor-showhorizontalgrid.md)<br/>               | Ruft einen Wert ab, der bestimmt, ob horizontale Rasterlinien im Diagramm angezeigt werden, oder legt ihn fest.<br/>                                                                                                                          |
| [**ShowLegend**](systemmonitor-showlegend.md)<br/>                               | Ruft einen Wert ab, der bestimmt, ob die Legende angezeigt wird, oder legt ihn fest.<br/>                                                                                                                                                   |
| [**Showscalelabels**](systemmonitor-showscalelabels.md)<br/>                     | Ruft einen Wert ab, der bestimmt, ob die Skalierungs Bezeichnungen auf der vertikalen Achse des Diagramms angezeigt werden, oder legt ihn fest.<br/>                                                                                                          |
| [**Showtimeaxislabels**](systemmonitor-showtimeaxislabels.md)<br/>               | Ruft einen Wert ab, der bestimmt, ob die horizontale Achse (X) der Diagramm Ansicht Bezeichnungen enthält, oder legt ihn fest.<br/>                                                                                                                      |
| [**ShowToolbar**](systemmonitor-showtoolbar.md)<br/>                             | Ruft einen Wert ab, der bestimmt, ob die Symbolleiste auf dem Steuerelement angezeigt wird, oder legt ihn fest.<br/>                                                                                                                                   |
| [**Showvaluebar**](systemmonitor-showvaluebar.md)<br/>                           | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob der Wert Balken (der Satz von statistischen Werten unterhalb des Diagramms) auf dem Steuerelement angezeigt wird.<br/>                                                                                 |
| [**Showverticalgrid**](systemmonitor-showverticalgrid.md)<br/>                   | Ruft einen Wert ab, der bestimmt, ob vertikale Rasterlinien im Diagramm angezeigt werden, oder legt ihn fest.<br/>                                                                                                                            |
| [**Sqldsnname**](systemmonitor-sqldsnname.md)<br/>                               | Ruft den Namen der ODBC-Datenquelle ab oder legt ihn fest.<br/>                                                                                                                                                                                 |
| [**Sqllogsetname**](systemmonitor-sqllogsetname.md)<br/>                         | Ruft den anzeigen amen des Protokoll Satzes ab oder legt ihn fest.<br/>                                                                                                                                                                          |
| [**Timebarcolor**](systemmonitor-timebarcolor.md)<br/>                           | Ruft die Farbe der Zeitleiste ab oder legt Sie fest (der senkrechte Strich, der sich über das Diagramm Fenster bewegt, um den Durchlauf der einzelnen Samplingintervalle in der Liniendiagramm Ansicht anzugeben).<br/>                                                  |
| [**UpdateInterval**](systemmonitor-updateinterval.md)<br/>                       | Ruft die Zeitspanne ab oder legt diese fest, die von sysmon gewartet wird, wenn das nächste Mal das Diagramm oder der Bericht aktualisiert wird.<br/>                                                                                                                  |
| [**Yaxislabel**](systemmonitor-yaxislabel.md)<br/>                               | Ruft die Bezeichnung der vertikalen Achse (Y-Achse) des Diagramms ab oder legt Sie fest.<br/>                                                                                                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





