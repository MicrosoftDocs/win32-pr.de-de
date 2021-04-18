---
description: In diesem Thema wird beschrieben, wie Sie den Status des Druckauftrags für den Benutzer anzeigen und die Option zum Abbrechen eines Druckauftrags, der gerade ausgeführt wird, zur Verfügung stellen.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Vorgehensweise: Anzeigen des Status des Druckauftrags'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9effc778f6affaba5b53cbd96a7a428ea5554d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358437"
---
# <a name="how-to-display-the-print-job-progress"></a>Vorgehensweise: Anzeigen des Status des Druckauftrags

In diesem Thema wird beschrieben, wie Sie den Status des Druckauftrags für den Benutzer anzeigen und die Option zum Abbrechen eines Druckauftrags, der gerade ausgeführt wird, zur Verfügung stellen.

## <a name="overview"></a>Übersicht

Ein Dialogfeld zum Drucken des Status führt in der Regel die folgenden Funktionen aus.

-   Zeigt den Status des Druckauftrags für den Benutzer an.
-   Starten Sie den druckverarbeitungs Thread.
-   Zeigen Sie eine Schaltfläche **Abbrechen** an, damit der Benutzer einen Druckauftrag beenden kann, bevor er abgeschlossen wird.

Streng genommen muss die Prozedur zum Drucken des Dialog Felds nur den Druckauftrag für den Benutzer anzeigen. Da die anderen beiden Funktionen in der vorangehenden Liste jedoch eng miteinander verknüpft sind, sind Sie auch in diesem Modul enthalten.

## <a name="displaying-print-job-progress"></a>Anzeigen des Status des Druckauftrags

Im Dialogfeld "Druck Status" werden die folgenden Fenster Meldungen behandelt.

-   **WM \_ InitDialog**

    Initialisiert die Steuerelemente, die im Dialogfeld verwendet werden.

-   **WM- \_ SetCursor**

    Legt den Cursor auf einen Zeiger fest, wenn der Benutzer einen Druckauftrag abbrechen kann, und auf den warte Cursor, wenn sich der Druckauftrag an einem Punkt befindet, an dem er nicht abgebrochen werden kann.

-   **Drucken \_ des \_ \_ Druckens des Benutzers**

    Legt die Statusanzeige Parameter für den Druckauftrag fest und erstellt den Druck Thread, um mit der Verarbeitung des Druckauftrags zu beginnen.

    Dies ist eine anwendungsspezifische Fenster Meldung.

-   **WM \_ -Befehl-IDCANCEL**

    Legt das Ereignis abbrechen fest, um den Druck Verarbeitungs Thread anzuweisen, den Druckauftrag abzubrechen.

-   **Benutzer \_ Druck \_ Status- \_ Update**

    Aktualisiert die Statusanzeige und den Status Text, um den aktuellen Status des Druckauftrags anzuzeigen.

    Dies ist eine anwendungsspezifische Fenster Meldung.

-   **Benutzer \_ Druck \_ Schließen**

    Legt den schließenden Status Text im Dialogfeld "Status" fest, um anzugeben, dass der Druckauftrag geschlossen wird.

    Dies ist eine anwendungsspezifische Fenster Meldung.

-   **Benutzer \_ Druck \_ vollständig**

    Zeigt die Meldung "Druckauftrag vollständig" für den Benutzer an und gibt Handles und Ereignisse frei, die in diesem Druckauftrag verwendet wurden.

    Dies ist eine anwendungsspezifische Fenster Meldung.

 

 



