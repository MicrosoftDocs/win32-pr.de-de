---
description: Dieses Thema bietet eine allgemeine Überprüfung von TSP-Vorgängen.
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: Lebenszyklus eines Telefoniedienstanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 830bc16ca606bb5bd38c4bce7c1e6e39dadb65a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568126"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>Lebenszyklus eines Telefoniedienstanbieters

Dieses Thema bietet eine allgemeine Überprüfung von TSP-Vorgängen.

Eine Sitzung ist die Zeit, während der eine bestimmte Konfiguration gültig bleibt und telefonienvorgänge durchgeführt werden. Ein Dienstanbieter kann viele Sitzungen zwischen dem Zeitpunkt, zu dem er zum ersten Mal geladen wird, und dem Zeitpunkt, zu dem er freigegeben wird Für jede Sitzung aushandiert TAPI die Version der Schnittstelle, startet die Sitzung, führt Vorgänge aus und fährt schließlich die Sitzung herunter. Der Dienstanbieter darf keine Informationen von einer Sitzung zur nächsten beibehalten.

Nachdem die Schnittstellen Version bekannt ist, ruft TAPI die [**TSPI \_ providerinit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) -Funktion auf, um alle operativen Parameter festzulegen. Der Dienstanbieter stellt sicher, dass alle Konfigurationsinformationen in der Registrierung stabil sind, wenn die **TSPI \_ providerinit** -Funktion aufgerufen wird. Die meisten Dienstanbieter lesen alle Konfigurationsinformationen zu diesem Zeitpunkt.

Normaler Betrieb kann in beliebiger Reihenfolge fortgesetzt werden, nachdem der Dienstanbieter initialisiert wurde.

TAPI verhandelt gerätespezifische Informationen auf Gerätebasis. TAPI und der Dienstanbieter Commit für eine Version durch, wenn ein Gerät geöffnet wird.

Der Dienstanbieter kann Anforderungen zum auswählen und Abbrechen von Erweiterungs Versionen empfangen. Wenn eine Erweiterungs Version ausgewählt ist, funktioniert das Gerät strikt entsprechend der gerätespezifischen Erweiterungs Version.

Die Aushandlung einer gerätespezifischen Erweiterungs Version kann mehrmals erfolgen, und zwar sowohl vor als auch nach dem Öffnen des Geräts. TAPI übergibt einen Versions Bereich, und der Dienstanbieter wählt einen Wert aus diesem Bereich aus und gibt ihn zurück. Normalerweise sind gerätespezifische Erweiterungen für den Dienstanbieter deaktiviert.

Dies führt dazu, dass TAPI und der Dienstanbieter auf dieser Erweiterungs Versions Ebene betrieben werden, bis die Auswahl abgebrochen wird. Während der Zeit, in der eine gerätespezifische Erweiterung wirksam ist, sollte der Versuch, eine Erweiterungs Versions Ebene auszuhandeln, nur die Versions Ebene zulassen, die zurzeit wirksam ist. Nachdem die gerätespezifische Erweiterung abgebrochen wurde, kann eine andere Version ausgehandelt und ausgewählt werden.

Telefon Vorgänge innerhalb des Paars " **Öffnen/Schließen** " sind in der folgenden Abbildung dargestellt. Einige dieser Vorgänge sind synchron, andere sind asynchron. Wenn ein Vorgang asynchron abgeschlossen wird, kann ein anderer Vorgang vor dem Abschluss des ersten Berichts angefordert werden. Folglich können sich Vorgänge in beliebiger Weise überlappen. Der Dienstanbieter muss letztendlich den Abschluss eines asynchronen Vorgangs, der angefordert wird, melden. Durch das Schließen eines Telefons erzwingen Sie, dass ausstehende asynchrone Vorgänge abgeschlossen werden (möglicherweise mit dem Hinweis "Fehler").

Der Lebenszyklus für Linien Geräte ähnelt dem Lebenszyklus für Smartphones, außer dass die Zeilen über eigene Aushandlungs-, Initialisierungs-, Öffnungs-und Schluss Prozeduren verfügen. Vorgänge für geöffnete Zeilen werden durch ein eigenes **Open/Close-** Paar in Klammern gesetzt. Dieses Paar wird zwischen dem gleichen **Initialisierungs-** /Beendigungs-Paar in Klammern gesetzt, das beim **Öffnen/Schließen** des Telefons geöffnet ist.

Die Lebenszyklen von Aufrufen werden genau zwischen dem **Öffnen/Schließen** der Zeile, in der Sie enthalten sind, in Klammern gesetzt. Die Lebensdauer von aufrufen kann auf verschiedene Weise beginnen:

-   Von TAPI durch Funktionen wie [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)oder [**linesetupconference**](/windows/win32/api/tapi/nf-tapi-linesetupconference)angefordert.
-   Wird von dem Dienstanbieter als neue eingehende Anrufe, von Benutzern initiierte Aufrufe an einem angehängten Telefongerät oder als Nebeneffekt von anderen Vorgängen, wie z. b. dem Platzieren eines vorhandenen Aufrufs, generiert.

Die Lebensdauer von eindeutigen aufrufen in derselben Zeile kann einander in beliebiger Weise überlappen. Alle Aufrufe beenden ihre Lebensdauer zu dem Zeitpunkt, zu dem die TSPI-Funktion " [**TSPI \_ lineclosecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) " aufgerufen wird. Der Lebenszyklus mehrerer Aufrufe ist in der folgenden Abbildung dargestellt.

![Lebenszyklen von überlappenden aufrufen](images/modell.png)

Ein-Anruf kann aus TAPI stammen, wie im **MakeCall/closecall-** paar gezeigt. Ein-Rückruf kann auch aus dem Dienstanbieter stammen. Der Dienstanbieter kündigt dies mit einer [**Zeile \_ newcallenmeldung**](line-newcall.md) an eine von TAPI bereitgestellte Rückruf Prozedur an. In einem solchen Fall gibt TAPI seinen Bezeichner für den Aufruf zurück, der in nachfolgenden Rückrufen enthalten ist, die Ereignisse für den Aufruf melden. Bei aufrufen, deren Lebensdauer aus TAPI stammt, ist dieser Bezeichner in den TSPI-Vorgang eingeschlossen, der den Aufruf erstellt.

Alle Vorgänge, die die Lebensdauer eines Aufrufes starten, führen dazu, dass TAPI und der Dienstanbieter Bezeichner für den neuen-Befehl austauscht. Im Fall von TAPI-Aufrufen übergibt TAPI seinen Bezeichner und empfängt den Bezeichner des Dienstanbieters als Rückgabe Parameter. Wenn der-Befehl aus dem Dienstanbieter stammt, übergibt der Dienstanbieter seinen Bezeichner an TAPI und empfängt den TAPI-Bezeichner als Rückgabe Parameter.

Die folgende Abbildung bietet eine allgemeine Übersicht über die Installation, Konfiguration und Entfernung von Dienstanbietern. Lebenszyklus Sequenzen, die viele Sitzungen umfassen. Der typische Lebenszyklus für diese Vorgänge kann mit der folgenden zeitzeile angezeigt werden.

![Installation, Konfiguration und Entfernung von Dienstanbietern](images/model2.png)

Der typische Installations-und Entfernungs Lebenszyklus wird in mehreren Sitzungen angezeigt. Aufrufe der **Installations** -und [**Entfernungs**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) Prozeduren werden strikt gekoppelt und überlappen sich nicht. Aufrufe der **Konfigurations** Prozedur können innerhalb dieses Paars mehrmals erfolgen. Eine solche Vorgehensweise erfolgt in der Regel vom Dienstanbieter als interner Nebeneffekt des **Installations** Verfahrens zum Erstellen von Zeilen-und Telefon Einträgen. Die **Konfigurations** Prozedur kann zu anderen Zeitpunkten aufgerufen werden, um ein vorhandenes Setup zu ändern. Die **Installations** Prozedur muss durchgeführt werden, bevor eine andere TSPI-Funktion zulässig ist. Im idealen Szenario sind alle Sitzungen innerhalb des **Installations-/Entfernungs-** Prozedur Paars streng geschachtelt.

Die Funktionen [**TSPI \_ providerinstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall), [**TSPI \_ providerconfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)und [**TSPI \_ providerremove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) interagieren mit dem Dienstanbieter selbst und nicht mit einem bestimmten Gerät. Sie wirken sich auf statische Konfigurationsinformationen aus, die über mehrere Sitzungen hinweg bestehen und vorhanden sein müssen, damit jeder andere Vorgang fortgesetzt werden kann. Folglich werden alle anderen Vorgänge zwischen dem Aufruf von **TSPI \_ providerinstall** und dem Abschluss des entsprechenden **TSPI \_ providerremove**-Vorgangs zwischengespeichert. Diese beiden Vorgänge treten in der Regel sehr weit auseinander, wahrscheinlich in einer anderen Last des Dienstanbieters oder eines anderen Starts des Computers. Das externe Aufrufen der **config** -Funktion ist optional, da die **Installations** Prozedur zusätzlich zu ihrer eigenen das **Konfigurations** Verhalten einschließen muss. Der übliche Grund für einen externen Aufruf besteht darin, eine vorhandene Konfiguration zu ändern.

In das Konzept des Abschlusses eines [**TSPI \_ providerremove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) -Vorgangs ist eine Feinheit eingebettet. Es ist wünschenswert, dass der Benutzer das mit dem Telefoniedienst bereitgestellte Dienstprogramm für die Telefonie-Systemsteuerung ausführen kann, um Dienstanbieter Konfigurationen zu ändern, auch wenn bereits telefonienvorgänge (Sitzungen) ausgeführt werden. Folglich ermöglichen sowohl die [**TSPI \_ providerconfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) -als auch die **TSPI \_ providerremove** -Spezifikationen den Aufruf, während eine ausstehende Sitzung vorhanden ist. Allerdings müssen Änderungen an der Konfiguration verzögert werden, bis die telefonievorgänge heruntergefahren und neu gestartet werden. Folglich findet der Abschluss eines **TSPI \_ providerconfig** -oder **TSPI \_ providerremove** -Vorgangs außerhalb einer Sitzung statt. Die Schachtelung von Aktionen ist wie in der Abbildung dargestellt, auch wenn die Prozeduren Aufrufe in einer etwas anderen Reihenfolge auftreten können. Es ist zulässig, dass ein Dienstanbieter während der Ausführung von Vorgängen einfach **config** oder [**Remove**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) nicht zulässt, obwohl der Benutzer über ein Dialogfeld benachrichtigt werden muss. Eine benutzerfreundliche Implementierung, die mindestens eine Teilmenge von Vorgängen zulässt, wird bevorzugt.

Diese **Installations**-, **Konfigurations**-und [**Entfernungs**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) Vorgänge haben alle den Nebeneffekt, dass alle laufenden Telefonieanwendungen signalisiert werden, was letztendlich dazu führt, dass Sie die Verwendung des Telefoniedienstanbietern beenden. Dadurch werden alle ausstehenden Sitzungen für Dienstanbieter beendet. Dies deutet darauf hin, dass Dienstanbieter die neue Registrierungs Konfiguration lesen müssen, wenn neue Sitzungen beginnen. Alle Änderungen, die aufgrund einer **Konfiguration** oder eines [**Entfernens**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) während der Ausführung von Vorgängen ausstehend waren, treten in Kraft.

 

 
