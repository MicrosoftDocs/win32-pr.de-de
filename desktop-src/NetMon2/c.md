---
description: Glossar Netzwerkmonitor Begriffe, die mit dem Buchstaben C beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31993c18307ab1beaa1b6cff379626b9398987d6ad9475947c4aeb4d09dd32e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367436"
---
# <a name="c-network-monitor"></a>C (Netzwerkmonitor)

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**Erfassen**
</dt> <dd>

Daten zum Netzwerkdatenverkehr, die in Frames erfasst werden. Ein Netzwerkpaketanbieter (Network Packet Provider, NPP) führt eine Erfassung durch. Siehe auch [*verzögerte Erfassung*](d.md)und *Echtzeiterfassung.*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**Erfassungsdatei**
</dt> <dd>

Eine Datei, die Netzwerkmonitor erstellt, um erfasste Daten zu speichern. Die Dateinamenerweiterung .cap identifiziert eine Erfassungsdatei. Netzwerkmonitor generiert nach dem Zufallsprinzip einen Namen für die Erfassungsdatei, aber Sie können den Dateinamen ändern, wenn Sie die Erfassungsdatei speichern.

Netzwerkmonitor erstellt bei jedem Start des Aufzeichnungsprozesses eine Erfassungsdatei und hält die Datei während des Erfassungsprozesses geöffnet. Sie können erst auf den Inhalt einer Erfassungsdatei zugreifen, wenn der Erfassungsprozess beendet und die Aufzeichnungsdatei geschlossen wurde.

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**Erfassungsfilter**
</dt> <dd>

Eine Reihe von Netzwerkmonitor Funktionen, die verwendet werden, um eingehende Frames einzuschränken, die von einer NPP-Anwendung (Network Packet Provider) verwendet werden.

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**Erfassungstrigger**
</dt> <dd>

Ein Triggerereignis, das festgelegt ist, um den Erfassungsprozess zu beenden. Das Erfassungstriggerereignis kann eine temporäre Erfassungsdatei sein, die an eine bestimmte Ebene oder ein bestimmtes Datenmuster weitergeleitet wird, die in einem erfassten Frame auftritt.

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**Erfasste Daten**
</dt> <dd>

Frames, die einen definierten Kriteriensatz aufweisen. Die Datenrahmen sind in einer temporären Erfassungsdatei enthalten.

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**Konversationsstatistiken**
</dt> <dd>

Statistiken zum Netzwerkdatenverkehr, der während einer Erfassung gespeichert wurde. Diese Statistiken enthalten Stations- und Sitzungsinformationen, die beim Start des Erfassungsprozesses beginnen und beendet werden, wenn die Erfassung beendet wird. Wenn Sie den Erfassungsprozess anhalten, fügt Netzwerkmonitor weiterhin Statistiken hinzu, wenn Sie den Prozess fortsetzen. Rufen Sie zum Abrufen von **Konversationsstatistiken die GetConversationStatistics-Methode** für die schnittstelle auf, die Sie verwenden.

</dd> </dl>

 

 



