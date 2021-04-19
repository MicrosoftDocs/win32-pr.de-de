---
description: Der WDM-Anbieter (Windows-Treibermodell) gewährt den Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardware Treibern, die dem WDM-Modell entsprechen.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Zugreifen auf Daten von Gerätetreibern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a59b59116ca0f71178fb2faed290d6bc76c9d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350168"
---
# <a name="accessing-data-from-device-drivers"></a>Zugreifen auf Daten von Gerätetreibern

Der WDM-Anbieter (Windows-Treibermodell) gewährt den Zugriff auf die Klassen, Instanzen, Methoden und Ereignisse von Hardware Treibern, die dem WDM-Modell entsprechen. Die Klassen für Hardwaretreiber befinden sich im Stamm- \\ \\ \\ WMI-Namespace.

Der WDM-Anbieter ist für Benutzer, die Gerätetreiber schreiben, und für Administratoren, die an Gerätetreiber Daten interessiert sind, von Interesse.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Informationen für Gerätetreiber Schreiber](#information-for-device-driver-writers)
-   [Informationen für Administratoren und Benutzer von Treiber Daten](#information-for-administrators-and-users-of-driver-data)
-   [Zugehörige Themen](#related-topics)

## <a name="information-for-device-driver-writers"></a>Informationen für Gerätetreiber Schreiber

WMI-Klassen, die mit einem bestimmten Gerätetreiber verknüpft sind, werden erstellt, wenn der WDM-Anbieter die binäre MOF aus der ausführbaren Datei des Gerätetreibers extrahiert. Dies erfolgt immer dann, wenn WMI gestartet wird, ein neuer Gerätetreiber installiert wird oder die Instanz von [wmibinarymufresource](/windows/desktop/WmiCoreProv/wmibinarymofresource) für einen bestimmten Treiber gelöscht wird. Durch Überprüfen von wmiprov. Log können Sie feststellen, ob beim Extrahieren der binären MOF-Datei ein Fehler aufgetreten ist. Die Details [der Fehler](mofcomp.md) Meldungen werden in der Datei "" in "" "" Weitere Informationen finden Sie unter [WMI-Protokolldateien](wmi-log-files.md). Aus Leistungsgründen generiert der WDM-Anbieter keine Ereignisse beim Erstellen oder Löschen von Klassen, da ein WDM-Anbieter gestartet oder beendet wird.

Der WDM-Anbieter transformiert alle wnode-Daten in Klassen Informationen. Wenn beim Transformieren der Daten von wnode in Klassen Daten ein Fehler auftritt, wird er in wmiprov. log mit dem formatierten Header und den gerenderten Bytes in derselben Form wie ein Speicher Abbild gemeldet.

An den Sicherheitseinstellungen für den Treiber vorgenommene Änderungen werden erst wirksam, wenn der WDM-Anbieter entladen und erneut geladen wurde. Weitere Informationen finden Sie unter [Entladen eines Anbieters](unloading-a-provider.md).

WMI kann auch Leistungsindikatoren für Hardwaretreiber verfügbar machen. Weitere Informationen zum Erstellen von hochleistungsklassen und zum Anzeigen von Daten im Perfmon-System Monitor finden Sie unter [verbessern der Effizienz eines Instanzanbieters](improving-the-efficiency-of-an-instance-provider.md). Weitere Informationen zum Schreiben von WMI-fähigen Gerätetreibern finden Sie unter [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Weitere Informationen zu WDM-spezifischen Qualifizierern in der MOF-Datei finden [**Sie unter Qualifizierer für den WDM-Anbieter**](qualifiers-specific-to-the-wdm-provider.md).

## <a name="information-for-administrators-and-users-of-driver-data"></a>Informationen für Administratoren und Benutzer von Treiber Daten

Wenn Sie die Instanzen der [wmibinarymufresource](/windows/desktop/WmiCoreProv/wmibinarymofresource) -Klasse auflisten, finden Sie eine Liste der Treiber im System sowie Informationen dazu, ob der WDM-Anbieter das Kompilieren der-Dateien für die einzelnen Treiber erfolgreich durchführen konnte. Sie können erzwingen, dass der Anbieter die Klassen für einen Treiber erneut kompiliert und erneut generiert, indem Sie die Instanz von wmibinarymufresource löschen, die diesen Treiber darstellt. Details zu [den Fehlermeldungen in der Datei](mofcomp.md) "".

Wenn der WMI-Namespace beschädigt ist, kann er gelöscht und erneut geöffnet werden, um zu erzwingen, dass die Treiber Klassen von WDM neu erstellt werden. Weitere Informationen zum Öffnen eines Namespaces finden Sie unter [Erstellen von Hierarchien in WMI](creating-hierarchies-within-wmi.md).

Treiber Klassen können gelegentlich "Gestrandet" werden, wenn das Laden des Treibers unterbrochen wird oder andere ungewöhnliche Vorgänge stattfinden. Der WDM-Anbieter sucht und bereinigt nur "gestrandete" Klassen, wenn ein neuer Treiber installiert wird, oder wenn der **Software- \\ Microsoft \\ WBEM \\ wdmprovider** -Registrierungsschlüssel Wert " **processstrandclasses** " auf " **true**" festgelegt ist. Wenn dieser Wert auf **true** festgelegt wird, wird die WMI-Startleistung aufgrund des Bereinigungs Vorgangs verlangsamt. Der Standardwert ist **FALSE**. Der WDM-Anbieter überprüft nur diesen Registrierungs Wert, wenn der "root \\ WMI"-Namespace zum ersten Mal geöffnet wird.

Wenn an einem WDM-Gerätetreiber Sicherheitsänderungen vorgenommen werden, werden die Änderungen erst wirksam, wenn der WDM-Anbieter entladen und neu geladen wird. Der Windows-Verwaltungsdienst muss beendet und neu gestartet werden, um dies zu erreichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 
