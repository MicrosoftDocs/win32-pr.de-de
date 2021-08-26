---
description: In diesem Thema wird beschrieben, wie sie dem Benutzer den Fortschritt des Druckauftrags anzeigen und ihm die Option zum Abbrechen eines druckauftrags geben, der gerade in Bearbeitung ist.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'How To: Anzeigen des Druckauftragsfortschritts'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec61c07844262b258fb052d08d8d20e9285a8f7e9bb83808ea61eddaf32f3a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950610"
---
# <a name="how-to-display-the-print-job-progress"></a>How To: Anzeigen des Druckauftragsfortschritts

In diesem Thema wird beschrieben, wie sie dem Benutzer den Fortschritt des Druckauftrags anzeigen und ihm die Option zum Abbrechen eines druckauftrags geben, der gerade in Bearbeitung ist.

## <a name="overview"></a>Übersicht

Eine Dialogfeldprozedur für den Druckfortschritt führt in der Regel die folgenden Funktionen aus.

-   Zeigt dem Benutzer den Fortschritt des Druckauftrags an.
-   Starten Sie den Druckverarbeitungsthread.
-   Zeigen Sie die **Schaltfläche Abbrechen** an, damit der Benutzer einen Druckauftrag beenden kann, bevor er abgeschlossen wird.

Streng genommen muss die Prozedur des Dialogfelds "Druckfortschritt" nur den Fortschritt des Druckauftrags für den Benutzer anzeigen. Da die beiden anderen Funktionen in der vorherigen Liste jedoch eng miteinander verknüpft sind, wurden sie auch in dieses Modul aufgenommen.

## <a name="displaying-print-job-progress"></a>Anzeigen des Status des Druckauftrags

Eine Dialogfeldprozedur für den Druckfortschritt verarbeitet die folgenden Fenstermeldungen.

-   **WM \_ INITDIALOG**

    Initialisiert die Steuerelemente, die das Dialogfeld verwendet.

-   **WM \_ SETCURSOR**

    Legt den Cursor auf einen Zeiger fest, wenn der Benutzer einen Druckauftrag abbrechen kann, und auf den Wartecursor, wenn sich der Druckauftrag an einem Punkt befindet, an dem er nicht abgebrochen werden kann.

-   **DRUCKEN \_ DES BENUTZERS STARTEN DES \_ \_ DRUCKS**

    Legt die Statusanzeigeparameter für den Druckauftrag fest und erstellt den Druckthread, um mit der Verarbeitung des Druckauftrags zu beginnen.

    Dies ist eine anwendungsspezifische Fenstermeldung.

-   **\_WM-BEFEHL – IDCANCEL**

    Legt das Cancel-Ereignis fest, um den Druckverarbeitungsthread an den Abbricht des Druckauftrags zu informieren.

-   **STATUSAKTUALISIERUNG \_ DES \_ \_ BENUTZERDRUCKS**

    Aktualisiert die Statusanzeige und den Statustext, um den aktuellen Status des Druckauftrags anzuzeigen.

    Dies ist eine anwendungsspezifische Fenstermeldung.

-   **SCHLIEßEN \_ DES \_ BENUTZERDRUCKS**

    Legt den Schließen-Statustext im Statusdialogfeld fest, um anzugeben, dass der Druckauftrag geschlossen wird.

    Dies ist eine anwendungsspezifische Fenstermeldung.

-   **BENUTZERDRUCK \_ \_ ABGESCHLOSSEN**

    Zeigt dem Benutzer die Meldung "Auftrag drucken abgeschlossen" an und gibt Handles und Ereignisse frei, die in diesem Druckauftrag verwendet wurden.

    Dies ist eine anwendungsspezifische Fenstermeldung.

 

 



