---
description: Der Windows Driver Model (WDM)-Anbieter gewährt Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardwaretreibern, die dem WDM-Modell entsprechen.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Zugreifen auf Daten von Gerätetreibern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bec478f83ddbc6d58419710fb868ddd233f820a06004210c1dac495de86b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131913"
---
# <a name="accessing-data-from-device-drivers"></a>Zugreifen auf Daten von Gerätetreibern

Der Windows Driver Model (WDM)-Anbieter gewährt Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardwaretreibern, die dem WDM-Modell entsprechen. Die Klassen für Hardwaretreiber befinden sich im \\ \\ \\ wmi-Stammnamespace.

Der WDM-Anbieter ist für Diejenigen von Interesse, die Gerätetreiber schreiben, und für Administratoren, die an Gerätetreiberdaten interessiert sind.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Informationen für Gerätetreiberschreiber](#information-for-device-driver-writers)
-   [Informationen für Administratoren und Benutzer von Treiberdaten](#information-for-administrators-and-users-of-driver-data)
-   [Zugehörige Themen](#related-topics)

## <a name="information-for-device-driver-writers"></a>Informationen für Gerätetreiberschreiber

WMI-Klassen, die mit einem bestimmten Gerätetreiber verknüpft sind, werden erstellt, wenn der WDM-Anbieter die binäre MOF aus der ausführbaren Datei des Gerätetreibers extrahiert. Dies erfolgt immer dann, wenn WMI gestartet wird, ein neuer Gerätetreiber installiert oder die Instanz von [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) für einen bestimmten Treiber gelöscht wird. Indem Sie "Wmiprov.log" überprüfen, können Sie ermitteln, ob beim Extrahieren der MOF-Binärdatei ein Fehler aufgetreten ist. Details zu [mofcomp-Fehlern](mofcomp.md) werden in Mofcomp.log gemeldet. Weitere Informationen finden Sie unter [WMI-Protokolldateien.](wmi-log-files.md) Aus Leistungsgründen generiert der WDM-Anbieter keine Ereignisse beim Erstellen oder Löschen von Klassen, da ein WDM-Anbieter gestartet oder beendet wird.

Der WDM-Anbieter transformiert alle WNODE-Daten in Klasseninformationen. Wenn beim Transformieren der Daten von WNODE in Klassendaten ein Fehler auftritt, wird er in Wmiprov.log mit dem Headerformat und bytes gemeldet, die in der gleichen Form wie ein Speicherabbild gerendert werden.

Änderungen an den Treibersicherheitseinstellungen werden erst wirksam, wenn der WDM-Anbieter entladen und erneut geladen wird. Weitere Informationen finden Sie unter [Entladen eines Anbieters.](unloading-a-provider.md)

WMI kann auch Leistungsindikatoren für Hardwaretreiber verfügbar machen. Weitere Informationen zum Erstellen von Hochleistungsklassen und zum Anzeigen von Daten im Perfmon-Systemmonitor finden Sie unter Verbessern der Effizienz [eines Instanzanbieters.](improving-the-efficiency-of-an-instance-provider.md) Weitere Informationen zum Schreiben von WMI-fähigen Gerätetreibern finden Sie unter [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Weitere Informationen zu WDM-spezifischen Qualifizierern in der MOF-Datei finden Sie unter Für den [**WDM-Anbieter spezifische Qualifizierer.**](qualifiers-specific-to-the-wdm-provider.md)

## <a name="information-for-administrators-and-users-of-driver-data"></a>Informationen für Administratoren und Benutzer von Treiberdaten

Das Auflisten der Instanzen der [WMIBinaryMofResource-Klasse](/windows/desktop/WmiCoreProv/wmibinarymofresource) enthält eine Liste der Treiber im System und Informationen darüber, ob der WDM-Anbieter die MOFs für jeden Treiber erfolgreich kompiliert hat. Sie können den Anbieter zwingen, die Klassen für einen Treiber neu zu kompilieren und neu zu generieren, indem Sie die Instanz von WMIBinaryMofResource löschen, die diesen Treiber darstellt. Details zu [mofcomp-Fehlern](mofcomp.md) werden in der Datei Mofcomp.log gemeldet.

Wenn der WMI-Namespace beschädigt ist, kann er gelöscht und erneut geöffnet werden, um zu erzwingen, dass WDM die Treiberklassen neu erstellt. Weitere Informationen zum Öffnen eines Namespace finden Sie unter [Erstellen von Hierarchien in WMI.](creating-hierarchies-within-wmi.md)

Treiberklassen können gelegentlich "versängstig" werden, wenn das Laden des Treibers unterbrochen wird oder andere ungewöhnliche Vorgänge auftreten. Der WDM-Anbieter sucht nur dann nach "gesteinerten" Klassen und bereinigt sie, wenn ein neuer Treiber installiert ist oder wenn der Registrierungsschlüsselwert Von **\\ Software Microsoft \\ WBEM \\ WDMProvider** **ProcessProvideredClasses** auf TRUE festgelegt **ist.** Wenn Sie diesen Wert auf **TRUE** festlegen, wird die WMI-Startleistung aufgrund des Bereinigungsvorganges verlangsamt. Der Standardwert ist **FALSE**. Der WDM-Anbieter überprüft diesen Registrierungswert nur, wenn der Namespace "Root \\ Wmi" zum ersten Mal geöffnet wird.

Wenn Sicherheitsänderungen an einem WDM-Gerätetreiber vorgenommen werden, werden die Änderungen erst wirksam, wenn der WDM-Anbieter entladen und erneut geladen wird. Der Windows-Verwaltungsdienst muss beendet und neu gestartet werden, um dies zu erreichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 
