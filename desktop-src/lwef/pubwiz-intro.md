---
title: Einführung in die Veröffentlichungsassistenten
description: Mit Windows XP werden der Webpublishing-Assistent und der Assistent für die Online druckbestellung eingeführt.
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- Veröffentlichungs-Assistenten, Informationen zu
- Webpublishing-Assistent, Informationen zu
- Online-druckbestell-Assistent, Info
- Veröffentlichungs-Assistenten, Webpublishing-Assistent
- Veröffentlichungs-Assistenten, Assistent für Online-Druck Bestellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b4e6d3c515edae23d0e74f550e000bdfdfacf03
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472797"
---
# <a name="publishing-wizards-introduction"></a>Einführung in die Veröffentlichungsassistenten

Mit Windows XP werden der Webpublishing-Assistent und der Assistent für die Online druckbestellung eingeführt. Basierend auf demselben Framework bieten diese Assistenten dem Benutzer einen einfachen Mechanismus zum Veröffentlichen von Inhalten auf einer Website oder zum Bestellen von Druck Vorzügen aus digitalen Bilddateien. Der Vorteil dieser Assistenten besteht darin, HTML-Inhalte von unterschiedlichen Anbietern auf den Seiten des Assistenten zu hosten, sodass die Optionen für das Aussehen, die Prozedur und die verfügbaren Benutzer vollständig vom Anbieter gesteuert werden und von Ihnen jederzeit geändert werden können, ohne dass sich dies auf den Client-Assistenten auswirkt, der Sie hostet. Obwohl diese vorhandenen Assistenten bereits mit digitaler Abbild Erstellung erstellt wurden, können das Framework und die Konzepte für viele andere Zwecke verwendet werden, wie z. b. einen Dokument Druckdienst oder als Methode zum Freigeben von Bildern für Freunde und Familien.

-   [Wie funktioniert es?](#how-does-it-work)
-   [Dokumentation des Veröffentlichungs-Assistenten](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>Wie funktioniert es?

Die Benutzeroberfläche für den Webpublishing-Assistenten und den Assistenten für die Online druckbestellung ist ähnlich, aber der Einstiegspunkt für die einzelnen Assistenten ist unterschiedlich. Für den Webpublishing-Assistenten ist eine Aufgabe mit dem Titel **diesen Ordner im Web veröffentlichen** in der Liste **Datei-und Ordner Aufgaben** links neben den meisten Ordneransichten verfügbar. Der Text für die Aufgabe variiert je nach ausgewähltem Inhalt. Wenn z. b. eine Datei ausgewählt ist, liest der Task **Diese Datei im Web veröffentlichen** , wie im folgenden Beispiel gezeigt.

![Datei-und Ordner Aufgaben](images/shell-pubwiz-tasks.png)

Der Benutzer klickt auf die Aufgabe, um den Assistenten zu starten. Wenn Sie mit dem Assistenten fortfahren, wird dem Benutzer eine Liste mit Anbietern angezeigt, wie im folgenden Beispiel gezeigt. Internet Dienstanbieter (ISPs) können Ihre eigenen Anbieter Seiten entwickeln und registrieren, die in dieser Liste angezeigt werden.

![Liste der Veröffentlichungs-Assistenten Anbieter](images/shell-pubwiz-provs.png)

Sobald ein Anbieter ausgewählt ist, stellt der Assistent eine Verbindung mit dieser Site her und die ersten HTML-Seiten Downloads für die Anzeige im Assistenten. Wenn Benutzer über kein Konto mit dem ausgewählten Anbieter verfügen, können Sie eine einrichten.

Mehrere HTML-Seiten sind auf einer einzelnen Seite des Assistenten enthalten. Das heißt, das Handle der Assistenten Seite, die diese Prozession von HTML-Seiten gehostet, bleibt konstant. Die HTML-Seiten werden im mittleren Bereich wie bei jeder Standard Assistenten Seite verfügbar gemacht. Die Anbieter Site stellt Methoden bereit, mit denen gesteuert werden kann, wo die Schaltflächen **zurück**, **weiter** und **Abbrechen** des Assistenten angezeigt werden, während die HTML-Seiten angezeigt werden. Innerhalb dieser HTML-Seiten werden Benutzer möglicherweise aufgefordert, einen Ordner anzugeben, in dem Sie Dateien kopieren oder den Namen einer Website speichern können, die Sie erstellen möchten. Nachdem ein Benutzer alle erforderlichen Schritte ausgeführt hat, ruft die Website eine Methode auf, um mit dem Hochladen zu beginnen, und gibt die Steuerung an den Assistenten zurück. Der Assistent selbst verarbeitet den Upload und alle zugehörigen Grafiken, wie z. b. eine Statusanzeige. Nachdem der Upload abgeschlossen ist, kann die Anbieter Website eine URL angeben, mit der der Benutzer nach dem Schließen des Assistenten fortfahren kann.

Im Assistenten für die Online Druck Sortierung wird online ausgegeben, dass die Task **Reihenfolge** nur in Bild Ordnern wie z. b. "meine Bilder" angezeigt wird, wie im folgenden Beispiel gezeigt. Der Prozess ist jedoch dem Webpublishing-Assistenten sehr ähnlich. Der Anbieter Standort fordert Benutzer zur Eingabe von Optionen wie Bildauswahl, Druckgröße, Anzahl der Kopien und Zahlungsinformationen auf.

![Bild Aufgaben](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>Dokumentation des Veröffentlichungs-Assistenten

Der Webpublishing-Assistent und der Assistent für die Online druckbestellung werden in den folgenden Dokumenten ausführlich erläutert. Außerdem finden Sie Anweisungen zum Entwickeln von Anwendungen, die von Ihnen gehostet werden.

-   [Client seitiges Design](pubwiz-client.md)
-   [Server seitiges Design](pubwiz-server.md)
-   [Registrieren eines Dienstanbieter](pubwiz-reg.md)
-   [Verwenden des Übertragungs Manifests](pubwiz-manifest.md)
-   [Schema des Übertragungs Manifests](/windows/desktop/shell/interfaces)

 

 