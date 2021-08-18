---
description: Dieses Thema bietet eine übersichtliche Übersicht über TSP-Vorgänge.
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: Lebenszyklus eines Telefoniedienstanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6282f4e7b946ffb79bd6233688869616cc0b0259a1d491834452290474c552a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012700"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>Lebenszyklus eines Telefoniedienstanbieters

Dieses Thema bietet eine übersichtliche Übersicht über TSP-Vorgänge.

Eine Sitzung ist die Zeit, in der eine bestimmte Konfiguration gültig bleibt und Telefonievorgänge ausgeführt werden. Ein Dienstanbieter kann viele Sitzungen zwischen dem zeitpunkt des ersten Ladens und dem Zeitpunkt der letzten Kostenlosung unterstützen. Für jede Sitzung handelt TAPI die Version der Schnittstelle aus, startet die Sitzung, führt Vorgänge aus und fährt die Sitzung schließlich herunter. Der Dienstanbieter darf keine Informationen von einer Sitzung zur nächsten beibehalten.

Nachdem die Schnittstellenversion bekannt ist, ruft TAPI die [**TSPI \_ providerInit-Funktion**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) auf, um alle betriebsbereiten Parameter festzulegen. Der Dienstanbieter stellt sicher, dass alle Konfigurationsinformationen in der Registrierung stabil sind, wenn die **TSPI \_ providerInit-Funktion** aufgerufen wird. Die meisten Dienstanbieter lesen alle Konfigurationsinformationen zu diesem Zeitpunkt.

Normale Vorgänge können in beliebiger Reihenfolge fortgesetzt werden, nachdem der Dienstanbieter initialisiert wurde.

TAPI handelt gerätespezifische Informationen pro Gerät aus. TAPI und der Dienstanbieter committen eine Version, wenn ein Gerät geöffnet wird.

Der Dienstanbieter kann Anforderungen zum Auswählen und Abbrechen von Erweiterungsversionen empfangen. Während eine Erweiterungsversion ausgewählt ist, arbeitet das Gerät streng nach dieser gerätespezifischen Erweiterungsversion.

Die Aushandlung einer gerätespezifischen Erweiterungsversion kann mehrmals erfolgen, sowohl vor als auch nach dem Öffnen des Geräts. TAPI übergibt einen Versionsbereich, und der Dienstanbieter wählt einen Wert aus diesem Bereich aus und gibt diesen zurück. Normalerweise sind gerätespezifische Erweiterungen für den Dienstanbieter deaktiviert.

Dadurch wird sowohl TAPI als auch der Dienstanbieter für den Betrieb auf dieser Erweiterungsversionsebene committet, bis die Auswahl abgebrochen wird. Während des Zeitraums, in dem eine gerätespezifische Erweiterung wirksam ist, sollte ein Versuch, eine Erweiterungsebene auszuhandeln, nur die derzeit geltende Versionsebene zulassen. Nachdem die gerätespezifische Erweiterung abgebrochen wurde, kann eine andere Version ausgehandelt und ausgewählt werden.

Telefon Vorgänge innerhalb des **Paars Öffnen/Schließen** sind in der folgenden Abbildung dargestellt. Einige dieser Vorgänge sind synchron, andere asynchron. Wenn ein Vorgang asynchron abgeschlossen wird, kann ein anderer Vorgang angefordert werden, bevor der erste Abschluss meldet. Daher können sich Vorgänge in beliebiger Weise überschneiden. Der Dienstanbieter muss schließlich den Abschluss für jeden angeforderten asynchronen Vorgang melden. Das Schließen eines Telefons erzwingt den Abschluss ausstehender asynchroner Vorgänge (möglicherweise mit einer Fehleranzeige).

Der Lebenszyklus für Liniengeräte ähnelt dem Lebenszyklus für Smartphones, mit der Ausnahme, dass Zeilen eigene Aushandlungs-, Initialisierungs-, Offene- und Schließverfahren aufweisen. Vorgänge für geöffnete Zeilen werden durch ein eigenes **Open/Close-Paar** in Klammern gesetzt. Dieses Paar befindet sich wiederum in Klammern zwischen demselben Paar aus **Initialisierung/Herunterfahren** wie das Telefon **, öffnen/schließen.**

Die Lebenszyklen von Aufrufen werden streng zwischen dem **Öffnen/Schließen** der Zeile, die sie enthält, in Klammern gesetzt. Die Lebensdauer von Aufrufen kann auf verschiedene Weise beginnen:

-   Wird von TAPI über Funktionen wie [**lineMakeCall,**](/windows/win32/api/tapi/nf-tapi-linemakecall) [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)oder [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference)angefordert.
-   Ursprünglich stammen vom Dienstanbieter neue eingehende Anrufe, vom Benutzer initiierte Anrufe an einem angefügten Telefonhandset oder Anrufe, die als Nebeneffekt anderer Vorgänge generiert werden, z. B. das Zurückhalten eines vorhandenen Anrufs.

Die Lebensdauer unterschiedlicher Aufrufe innerhalb derselben Zeile kann sich in beliebiger Weise überlappen. Alle Aufrufe enden ihre Lebensdauer zum Zeitpunkt des Aufrufs der [**TSPI-Funktion TSPI \_ lineCloseCall.**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) Der Lebenszyklus mehrerer Aufrufe wird in der folgenden Abbildung dargestellt.

![Lebenszyklen überlappender Aufrufe](images/modell.png)

Ein Aufruf kann aus TAPI stammen, wie im **MakeCall/CloseCall-Paar** gezeigt. Ein Aufruf kann auch vom Dienstanbieter stammen. Der Dienstanbieter kündigt dies mit einer [**LINE \_ NEWCALL-Nachricht**](line-newcall.md) an eine vom TAPI bereitgestellte Rückrufprozedur an. In einem solchen Fall gibt TAPI seinen Bezeichner für den Aufruf zurück, der in nachfolgenden Rückrufen enthalten ist, die Ereignisse melden, die beim Aufruf auftreten. Bei Aufrufen, deren Lebensdauer aus TAPI stammt, ist dieser Bezeichner im TSPI-Vorgang enthalten, der den Aufruf erstellt.

Alle Vorgänge, die die Lebensdauer eines Aufrufs starten, führen dazu, dass TAPI und der Dienstanbieter Bezeichner für den neuen Aufruf austauschen. Im Fall von TAPI-Aufrufen übergibt TAPI seinen Bezeichner und empfängt den Bezeichner des Dienstanbieters als Rückgabeparameter. Wenn der Aufruf vom Dienstanbieter stammt, übergibt der Dienstanbieter seinen Bezeichner an TAPI und empfängt den TAPI-Bezeichner als Rückgabeparameter.

Die folgende Abbildung bietet eine sehr übersichtliche Ansicht der Installation, Konfiguration und Entfernung von Dienstanbietern. Lebenszyklussequenzen, die viele Sitzungen umfassen. Der typische Lebenszyklus für diese Vorgänge kann mit der folgenden Zeitlinie angezeigt werden.

![Installation, Konfiguration und Entfernung von Dienstanbietern](images/model2.png)

Der typische Installations- und Entfernungslebenszyklus wird über mehrere Sitzungen hinweg angezeigt. Aufrufe der **Installations-** und [**Remove-Prozeduren**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) sind streng gekoppelt und überlappen sich nicht. Aufrufe  der Konfigurationsprozedur können innerhalb dieses Paars mehrmals erfolgen. Eine wird in der Regel vom Dienstanbieter als interner Nebeneffekt des **Installationsvorgangs** zum Erstellen von Zeilen- und Telefoneinträgen durchgeführt. Die  Konfigurationsprozedur kann zu anderen Zeiten aufgerufen werden, um ein vorhandenes Setup zu ändern. Die  Installationsprozedur muss ausgeführt werden, bevor eine andere TSPI-Funktion zugelassen wird. Im idealen Szenario sind alle Sitzungen  streng innerhalb des Installations-/Remove-Prozedurpaars geschachtelt.

Die Funktionen [**\_ TSPI-AnbieterInstall,**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall) [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)und [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) interagieren mit dem Dienstanbieter selbst und nicht mit einem bestimmten Gerät. Sie wirken sich auf statische Konfigurationsinformationen aus, die über mehrere Sitzungen hinweg bestehen bleiben und vorhanden sein müssen, damit jeder andere Vorgang fortgesetzt werden kann. Daher werden alle anderen Vorgänge zwischen dem Aufruf von **TSPI \_ providerInstall** und dem Abschluss des entsprechenden **\_ TSPI-AnbietersRemove** geschachtelt. Diese beiden Vorgänge erfolgen in der Regel sehr weit voneinander entfernt, höchstwahrscheinlich bei einer anderen Last des Dienstanbieters oder einem anderen Start des Computers. Das externe Aufrufen der **Config-Funktion** ist optional, da die Installationsprozedur zusätzlich zum eigenen **Konfigurationsverhalten** erforderlich ist.  Der übliche Grund für den externen Aufruf besteht darin, eine vorhandene Konfiguration zu ändern.

In das Konzept des Abschlusses eines [**\_ TSPI-AnbietersRemove-Vorgangs**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) ist eine Feinheit eingebettet. Es ist wünschenswert, dem Benutzer die Ausführung des telefoniediensts bereitgestellten Telefoniediensts Systemsteuerung zu ermöglichen, um die Konfigurationen des Dienstanbieters zu ändern, auch wenn Telefonievorgänge (Sitzungen) ausgeführt werden. Daher ermöglichen sowohl die [**TSPI \_ providerConfig-**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) als auch **die TSPI \_ providerRemove-Spezifikationen** einen Aufruf, während eine ausstehende Sitzung vorhanden ist. Änderungen an der Konfiguration müssen jedoch verzögert werden, bis Telefonievorgänge heruntergefahren und neu gestartet werden. Daher erfolgt streng genommen der Abschluss eines **\_ TSPI-Anbieterkonfigurations-** oder **\_ TSPI-AnbieterRemove-Vorgangs** außerhalb jeder Sitzung. Die Schachtelung von Aktionen ist wie in der Abbildung dargestellt, auch wenn die Prozeduraufrufe in einer etwas anderen Reihenfolge angezeigt werden können. Es ist zulässig, dass ein **Dienstanbieter** die Konfiguration oder das [**Entfernen**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) einfach nicht zulässt, während Vorgänge ausgeführt werden, obwohl der Benutzer über ein Dialogfeld benachrichtigt werden sollte. Eine benutzerfreundlichere Implementierung, die mindestens eine Teilmenge von Vorgängen zulässt, wird bevorzugt.

Diese **Install-,** **Config-** und [**Remove-Vorgänge**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) haben alle den Nebeneffekt, dass alle ausgeführten Telefonieanwendungen signalisiert werden, was schließlich dazu führt, dass sie ihre Nutzung des Telefoniediensts herunterfahren. Dadurch werden alle ausstehenden Sitzungen für Dienstanbieter beendet. Dies bedeutet für Dienstanbieter, dass sie die neue Registrierungskonfiguration lesen müssen, wenn neue Sitzungen beginnen. Alle Änderungen, die aufgrund einer **Konfiguration** oder eines [**Entfernens**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) ausstehen, während Vorgänge ausgeführt wurden, werden dann wirksam.

 

 
