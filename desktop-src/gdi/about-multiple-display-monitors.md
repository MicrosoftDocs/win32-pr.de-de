---
description: Wenn mehrere Monitore Teil des Desktops sind, können Objekte nahtlos zwischen Monitoren übertragen werden.
ms.assetid: eb7576c6-322c-48d0-abbb-bdc3b34976c3
title: Informationen zu mehreren Anzeige Monitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5997e39768d01522ae1fdd2e976c611e67826350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978192"
---
# <a name="about-multiple-display-monitors"></a>Informationen zu mehreren Anzeige Monitoren

Wenn mehrere Monitore Teil des Desktops sind, können Objekte nahtlos zwischen Monitoren übertragen werden. Das heißt, Sie können Fenster oder Verknüpfungen von einem Monitor auf einen anderen ziehen, und Sie können die Größe von Fenstern anpassen, um mehr als einen Monitor abzudecken. Wenn außerdem ein Monitor oberhalb eines anderen Monitors installiert wird, wird ein Cursor, der den unteren Rand des oberen Monitors verlässt, oben im unteren Monitor angezeigt.

In der Regel ordnet ein Benutzer die Monitore im System an, um die Anordnung der physischen Anzeigeeinheiten widerzuspiegeln. z. b. nebeneinander oder eins auf der obersten Seite der anderen. Der Benutzer führt dies über die Registerkarte Monitore durch, die im Dialogfeld **Anzeigeeigenschaften** über die Systemsteuerung die Registerkarte **Einstellungen** ersetzt. Die Monitore müssen einen zusammenhängenden Bereich bilden, d. h. jeder Monitor berührt einen anderen Monitor auf mindestens einem Teil eines Edge.

Wenn ein Fenster verschoben oder seine Größe geändert wird, ist ein Teil der Beschriftung immer sichtbar, sodass der Benutzer das Fenster mit der Maus verschieben und die Größe ändern kann. Die Cursor Bewegung ist auf den Bereich der Monitore beschränkt, sodass Sie immer sichtbar ist. Shellsymbole befinden sich auf demselben Monitor wie die Taskleiste, und die Taskleiste kann sich auf einem beliebigen Monitor befinden. Weitere Informationen finden Sie unter über [Legungen zum Monitor für ältere Programme](multiple-monitor-considerations-for-older-programs.md).

Ein System mit mehreren Monitoren wirkt sich auf bestimmte Tastenkombinationen aus. Die Tastenkombination ALT + PRINTSCRN erstellt eine Momentaufnahme des Vordergrund Fensters, wie immer. Der PRINTSCRN-Schlüssel erstellt jedoch eine Momentaufnahme des Monitors mit der Maus. Die Tastenkombination STRG + PRINTSCRN erstellt eine Momentaufnahme des gesamten virtuellen Bildschirms. Weitere Informationen finden Sie auf [dem virtuellen Bildschirm](the-virtual-screen.md).

Die Unterstützung für mehrere Monitore wirkt sich nicht auf die Leistung von Anwendungen aus, wenn Sie in einer einzigen Anzeige Umgebung ausgeführt wird. Dies bedeutet, dass bei der Ausführung auf einem einzelnen Anzeigesystem kein zusätzlicher mehr Aufwand im Hochleistungs-Grafik Vorgangs Code vorhanden ist. In einem System mit mehreren Monitoren ist die Leistung jedoch geringfügig beeinträchtigt, wenn eine Anwendung nur auf einem der Grafikgeräte ausgeführt wird. Außerdem kann die Leistung erheblich beeinträchtigt werden, wenn eine Anwendung mehrere anzeigen umfasst, insbesondere für grafikintensive Vorgänge.

Der *voll Bildschirm* ist eine vom Betriebssystem bereitgestellte Funktion, mit der ein Benutzer eine Anwendung in einen bestimmten Zustand umschalten kann, in dem die Anwendung direkt auf die VGA-Grafikhardware zugreifen kann. Dies ist ein wichtiges Feature für Spiele und andere Grafik orientierte Anwendungen, die eine hohe Leistung erfordern. Außerdem wird es häufig von Entwicklern für die Textbearbeitung verwendet, da es sehr schnelles Scrollen von Text ermöglicht.

In einer Umgebung mit mehreren Monitoren kann nur ein Grafikgerät mit VGA kompatibel sein. Dies ist eine Einschränkung der Computer Hardware, die erfordert, dass nur ein Gerät auf Hardware Adressen antwortet. Da der VGA-Hardware Kompatibilitäts Standard bestimmte Hardware Adressen erfordert, kann nur ein VGA-Grafikgerät auf einem Computer vorhanden sein, und nur dieses Gerät kann physisch auf VGA-Adressen reagieren. Anwendungen, die einen Vollbildmodus erfordern, werden daher nur auf einem bestimmten Gerät ausgeführt, das die VGA-Hardware Kompatibilität unterstützt.

Diese Übersicht enthält Informationen zu den folgenden Themen.

-   [Der virtuelle Bildschirm](the-virtual-screen.md)
-   [Hmonitor und der Gerätekontext](hmonitor-and-the-device-context.md)
-   [Enumeration und Anzeige Steuerung](enumeration-and-display-control.md)
-   [Mehrere Monitor Systemmetriken](multiple-monitor-system-metrics.md)
-   [Verwenden mehrerer Monitore als unabhängige Anzeige](using-multiple-monitors-as-independent-displays.md)
-   [Farben auf mehreren Anzeige Monitoren](colors-on-multiple-display-monitors.md)
-   [Positionieren von Objekten auf mehreren Anzeige Monitoren](positioning-objects-on-multiple-display-monitors.md)
-   [Mehrere Monitor Anwendungen auf verschiedenen Systemen](multiple-monitor-applications-on-different-systems.md)
-   [Überlegungen zu mehreren überwachen für ältere Programme](multiple-monitor-considerations-for-older-programs.md)

 

 



