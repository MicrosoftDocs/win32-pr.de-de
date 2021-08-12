---
title: Einführung in Veröffentlichungs-Assistenten
description: Windows XP führt den Webpublishing-Assistenten und den Onlinedruckbestellungs-Assistenten ein.
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- Veröffentlichungs-Assistenten,Informationen
- Webpublishing-Assistent,Informationen
- Onlinedruckbestellungs-Assistent,Informationen
- Veröffentlichungs-Assistenten,Webpublishing-Assistent
- Veröffentlichungs-Assistenten,Onlinedruckbestellungs-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d576d04579847d2e65bbc59399d11689259f8e64823a3c3068cafad912ff8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246673"
---
# <a name="publishing-wizards-introduction"></a>Einführung in Veröffentlichungs-Assistenten

Windows XP führt den Webpublishing-Assistenten und den Onlinedruckbestellungs-Assistenten ein. Basierend auf demselben Framework bieten diese Assistenten dem Benutzer einen einfachen Mechanismus zum Veröffentlichen von Inhalten auf einer Website oder zum Bestellen von Drucken aus digitalen Bilddateien. Der Vorteil dieser Assistenten besteht darin, dass sie HTML-Inhalte von verschiedenen Anbietern auf ihren Assistentenseiten hosten können, sodass das Aussehen, die Prozedur und die verfügbaren Benutzeroptionen vollständig vom Anbieter gesteuert werden und jederzeit ohne Auswirkungen auf den Client-Assistenten geändert werden können, der sie hostet. Diese vorhandenen Assistenten wurden zwar mithilfe der digitalen Bildverarbeitung erstellt, aber das Framework und die Konzepte können für viele andere Zwecke verwendet werden, z. B. für einen Dokumentdruckdienst oder als Methode zum Freigeben von Bildern für Freunde und Familienmitglieder.

-   [Wie funktioniert es?](#how-does-it-work)
-   [Dokumentation zum Veröffentlichungs-Assistenten](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a>Wie funktioniert es?

Die Benutzeroberfläche für den Webveröffentlichungs-Assistenten und den Onlinedruckbestellungs-Assistenten ist ähnlich, aber der Einstiegspunkt für jeden Assistenten unterscheidet sich. Für den Webveröffentlichungs-Assistenten ist eine Aufgabe mit dem  Titel Diesen Ordner im **Web veröffentlichen** in der Liste Datei- und Ordneraufgaben links von den meisten Ordneransichten verfügbar. Der Text für die Aufgabe variiert je nach ausgewähltem Inhalt. Wenn beispielsweise eine Datei ausgewählt ist, liest die Aufgabe Diese Datei im **Web** veröffentlichen, wie im folgenden Beispiel gezeigt.

![Datei- und Ordneraufgaben](images/shell-pubwiz-tasks.png)

Der Benutzer klickt auf die Aufgabe, um den Assistenten zu starten. Wenn Sie mit dem Assistenten fortfahren, wird dem Benutzer eine Liste von Anbietern angezeigt, wie im folgenden Beispiel gezeigt. Internetdienstanbieter (ISPs) können eigene Anbieterseiten entwickeln und registrieren, die in dieser Liste angezeigt werden sollen.

![Anbieterliste des Veröffentlichungs-Assistenten](images/shell-pubwiz-provs.png)

Nachdem ein Anbieter ausgewählt wurde, stellt der Assistent eine Verbindung mit dieser Website und die erste HTML-Seite wird zur Anzeige im Assistenten heruntergeladen. Wenn Benutzer kein Konto beim ausgewählten Anbieter haben, können sie eines einrichten.

Mehrere HTML-Seiten sind auf einer einzelnen Seite im Assistenten enthalten. Anders ausgedrückt: Das Handle der Assistentenseite, die diese Verarbeitung von HTML-Seiten hosten soll, bleibt konstant. Die HTML-Seiten werden wie bei jeder Standardseite des Assistenten im mittelpunkten Bereich verfügbar gemacht. Die Anbieterwebsite stellt Methoden zur Verfügung, um zu  steuern, wohin die Schaltflächen **Zurück,** **Weiter** und Abbrechen des Assistenten führen, während die HTML-Seiten angezeigt werden. Innerhalb dieser HTML-Seiten werden Benutzer möglicherweise aufgefordert, einen Ordner anzugeben, in den sie Dateien kopieren oder den Namen einer Website speichern können, die sie erstellen möchten. Nachdem ein Benutzer alle erforderlichen Schritte ausgeführt hat, ruft die Website eine -Methode auf, um den Upload zu starten, und gibt die Steuerung an den Assistenten zurück. Der Assistent selbst verarbeitet den Upload und alle damit wickeln Grafiken, z. B. eine Statusanzeige. Nach Abschluss des Uploads kann die Anbieterwebsite eine URL angeben, zu der der Benutzer wechseln kann, sobald der Assistent geschlossen wurde.

Im Assistenten zum Bestellen von Onlinedrucken wird die Aufgabe Reihenfolge wird **online** gedruckt nur in Bildordnern wie Meine Bilder angezeigt, wie im folgenden Beispiel gezeigt. Der Prozess ähnelt jedoch dem Webveröffentlichungs-Assistenten. Die Anbieterwebsite fordert Benutzer zur Eingabe von Optionen auf, z. B. Bildauswahl, Druckgrößen, Anzahl von Kopien und Zahlungsinformationen.

![Bildaufgaben](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a>Dokumentation zum Veröffentlichungs-Assistenten

Der Webveröffentlichungs-Assistent und der Onlinedruck-Bestell-Assistent werden in den folgenden Dokumenten ausführlich erläutert. Außerdem werden Anweisungen zum Entwickeln von Anwendungen erläutert, die von ihnen gehostet werden sollen.

-   [Clientseitiger Entwurf](pubwiz-client.md)
-   [Serverseitiger Entwurf](pubwiz-server.md)
-   [Registrieren eines Diensts](pubwiz-reg.md)
-   [Verwenden des Übertragungsmanifests](pubwiz-manifest.md)
-   [Manifestschema übertragen](/windows/desktop/shell/interfaces)

 

 