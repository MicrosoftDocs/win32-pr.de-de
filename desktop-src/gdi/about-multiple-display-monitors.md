---
description: Wenn mehrere Monitore Teil des Desktops sind, können Objekte nahtlos zwischen Monitoren ausgeführt werden.
ms.assetid: eb7576c6-322c-48d0-abbb-bdc3b34976c3
title: Informationen zu mehreren Anzeigemonitoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c28c8ccbd9abbcbcee696bb927c5aa484df7b23d6aba811ff95145d447109b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400510"
---
# <a name="about-multiple-display-monitors"></a>Informationen zu mehreren Anzeigemonitoren

Wenn mehrere Monitore Teil des Desktops sind, können Objekte nahtlos zwischen Monitoren ausgeführt werden. Das heißt, Sie können Fenster oder Tastenkombinationen von einem Monitor auf einen anderen ziehen, und Sie können Fenster so sgrößern, dass sie mehrere Monitore abdecken. Wenn ein Monitor über einem anderen installiert ist, wird oben auf dem unteren Monitor ein Cursor angezeigt, der den unteren Rand des oberen Monitors verlässt.

In der Regel ordnet ein Benutzer die Monitore im System so an, dass sie die Anordnung der physischen Anzeigeeinheiten widerspiegeln. z. B. nebeneinander oder 1-on-top-of-the-other. Der Benutzer führt dies mit der  Registerkarte Monitore durch, wodurch die Registerkarte Einstellungen registerkarte im Dialogfeld "Anzeigeeigenschaften"  durch Systemsteuerung. Die Monitore müssen einen zusammenhängenden Bereich bilden, d.&a; jeder Monitor berührt einen anderen Monitor an mindestens einem Teil eines Edges.

Wenn ein Fenster verschoben oder seine Größe geändert wird, ist ein Teil der Beschriftung immer sichtbar, damit der Benutzer das Fenster mit der Maus verschieben und seine Größe ändern kann. Die Cursorbewegung ist auf den Bereich der Monitore beschränkt, sodass sie immer sichtbar ist. Shellsymbole werden auf demselben Monitor wie die Taskleiste positioniert, und die Taskleiste kann sich auf jedem Monitor befinden. Weitere Informationen finden Sie unter Überlegungen zu mehreren Monitoren [für ältere Programme.](multiple-monitor-considerations-for-older-programs.md)

Ein System mit mehreren Monitoren wirkt sich auf bestimmte Tastenkombinationen aus. Die Tastenkombination ALT+PRINTSCRN erstellt wie immer eine Momentaufnahme des Vordergrundfensters. Der PRINTSCRN-Schlüssel erstellt jedoch eine Momentaufnahme des Monitors mit der Maus. Die Tastenkombination STRG+PRINTSCRN erstellt eine Momentaufnahme des gesamten virtuellen Bildschirms. Weitere Informationen finden Sie unter [Der virtuelle Bildschirm](the-virtual-screen.md).

Die Unterstützung mehrerer Monitore wirkt sich nicht auf die Leistung von Anwendungen aus, wenn sie in einer einzelnen Anzeigeumgebung ausgeführt werden. Das bedeutet, dass bei der Ausführung auf einem einzelnen Anzeigesystem kein zusätzlicher Mehraufwand im Code für leistungsstarke Grafikvorgänge vorhanden ist. In einem System mit mehreren Monitoren wird die Leistung jedoch geringfügig beeinträchtigt, wenn eine Anwendung nur auf einem der Grafikgeräte ausgeführt wird. Darüber hinaus kann die Leistung stark beeinträchtigt werden, wenn eine Anwendung mehrere Anzeigen umfasst, insbesondere bei grafikintensiven Vorgängen.

*Der Vollbildmodus* ist ein Feature des Betriebssystems, mit dem ein Benutzer eine Anwendung in einen speziellen Zustand umschalten kann, in dem die Anwendung direkt auf VGA-Grafikhardware zugreifen kann. Dies ist ein wichtiges Feature für Spiele und andere grafikorientierte Anwendungen, die eine hohe Leistung erfordern. Außerdem wird es häufig von Entwicklern für die Textbearbeitung verwendet, da es ein sehr schnelles Scrollen von Text ermöglicht.

In einer Umgebung mit mehreren Monitoren kann nur ein Grafikgerät VGA-kompatibel sein. Dies ist eine Einschränkung der Computerhardware, die erfordert, dass nur ein Gerät auf eine Hardwareadresse reagiert. Da der VGA-Hardwarekompatibilitätsstandard bestimmte Hardwareadressen erfordert, kann auf einem Computer nur ein VGA-Grafikgerät vorhanden sein, und nur dieses Gerät kann physisch auf VGA-Adressen reagieren. Daher werden Anwendungen, für die ein Vollbildmodus erforderlich ist, nur auf dem gerät ausgeführt, das VGA-Hardwarekompatibilität unterstützt.

Diese Übersicht enthält Informationen zu den folgenden Themen.

-   [Der virtuelle Bildschirm](the-virtual-screen.md)
-   [HMONITOR und der Gerätekontext](hmonitor-and-the-device-context.md)
-   [Enumerations- und Anzeigesteuer steuerelement](enumeration-and-display-control.md)
-   [Mehrere Systemmetriken überwachen](multiple-monitor-system-metrics.md)
-   [Verwenden mehrerer Monitore als unabhängige Anzeigen](using-multiple-monitors-as-independent-displays.md)
-   [Farben auf mehreren Anzeigemonitoren](colors-on-multiple-display-monitors.md)
-   [Positionieren von Objekten auf mehreren Anzeigemonitoren](positioning-objects-on-multiple-display-monitors.md)
-   [Mehrere Monitoranwendungen auf unterschiedlichen Systemen](multiple-monitor-applications-on-different-systems.md)
-   [Überlegungen zu mehreren Monitoren für ältere Programme](multiple-monitor-considerations-for-older-programs.md)

 

 



