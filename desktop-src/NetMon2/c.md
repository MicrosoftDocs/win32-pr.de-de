---
description: Glossar der Netzwerkmonitor Begriffe, die mit dem Buchstaben C beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Netzwerkmonitor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373025"
---
# <a name="c-network-monitor"></a>C (Netzwerkmonitor)

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**einver**
</dt> <dd>

Netzwerkverkehrs Daten, die in Frames gesammelt werden. Ein Netzwerk Paketanbieter (NPP) führt eine Erfassung aus. Siehe auch [*verzögerte Erfassung*](d.md)und *echt Zeiterfassung*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**Erfassungs Datei**
</dt> <dd>

Eine Datei, die Netzwerkmonitor erstellt, um erfasste Daten zu speichern. Die Dateinamenerweiterung. Cap identifiziert eine Erfassungs Datei. Netzwerkmonitor generiert nach dem Zufallsprinzip einen Aufzeichnungs Dateinamen, aber Sie können den Dateinamen ändern, wenn Sie die Erfassungs Datei speichern.

Netzwerkmonitor erstellt jedes Mal, wenn der Aufzeichnungsprozess startet, eine Erfassungs Datei und speichert die Datei dann während des Erfassungs Vorgangs geöffnet. Der Zugriff auf den Inhalt einer Erfassungs Datei ist erst möglich, nachdem der Aufzeichnungsprozess beendet und die Aufzeichnungsdatei geschlossen wurde.

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**Erfassungs Filter**
</dt> <dd>

Eine Reihe von Netzwerkmonitor Funktionen, die verwendet werden, um eingehende Frames einzuschränken, die von einer Netzwerk Paketanbieter-Anwendung verwendet werden.

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**Erfassungs-**
</dt> <dd>

Ein Auslöserereignis, das festgelegt wird, um den Aufzeichnungsprozess zu verhindern. Das Erfassungs Auslöserereignis kann eine temporäre Erfassungs Datei sein, die an eine bestimmte Ebene oder ein bestimmtes Datenmuster weitergeleitet wird, das in einem aufgezeichneten Frame auftritt.

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**erfasste Daten**
</dt> <dd>

Frames, die über einen definierten Satz von Kriterien verfügen. Die Datenrahmen sind in einer temporären Erfassungs Datei enthalten.

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**Konversations Statistik**
</dt> <dd>

Statistik von Netzwerk Datenverkehr, die während einer Erfassung gespeichert wird. Diese Statistiken enthalten Stations-und Sitzungsinformationen, beginnend beim Start des Aufzeichnungsprozesses und beenden, wenn die Erfassung angehalten wird. Wenn Sie den Aufzeichnungsprozess anhalten, werden Netzwerkmonitor weiterhin Statistiken hinzufügen, wenn Sie den Prozess fortsetzen. Um Konversations Statistiken abzurufen, rufen Sie die **getconversation ationstatistics** -Methode für die verwendete Schnittstelle auf.

</dd> </dl>

 

 



