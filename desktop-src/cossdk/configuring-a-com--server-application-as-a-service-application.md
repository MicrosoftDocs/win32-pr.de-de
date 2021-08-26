---
description: Eine COM+-Serveranwendung kann als Dienst erstellt werden, um entweder automatisch während des Systemstarts oder manuell durch Aktivierungen zu starten.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Konfigurieren einer COM+-Serveranwendung als Dienstanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ad6ec0af4ddf6d7ac7bf703209af2412e1ca4e128a942e7e1ecd089b69e278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991190"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a>Konfigurieren einer COM+-Serveranwendung als Dienstanwendung

Eine COM+-Serveranwendung kann als Dienst erstellt werden, um entweder automatisch während des Systemstarts oder manuell durch Aktivierungen zu starten. Wenn der Dienst nicht gestartet werden kann, gibt die Option für die Fehlerbehandlung den Schweregrad des Fehlers an und bestimmt die zu ergreifende Aktion. Die Option zum Konfigurieren eines Diensts für die Ausführung als lokales Systemkonto ist ebenfalls verfügbar, sowie die Option zum Zuweisen eines bestimmten Benutzerkontos, für das die COM+-Serveranwendung ausgeführt wird. Abhängigkeiten können auch aus einer Liste von Diensten ausgewählt werden, die mithilfe von Komponentendiensten auf dem Computer registriert sind. Dadurch wird bestimmt, welche Dienste ausgeführt werden müssen, bevor dieser Dienst gestartet wird.

**So konfigurieren Sie eine COM+-Anwendung für die Ausführung als Dienst**

1.  Suchen Sie in der Konsolenstruktur des Komponentendienste-Verwaltungstools die COM+-Serveranwendung, die Sie als Dienst ausführen möchten.

2.  Klicken Sie mit der rechten Maustaste auf die COM+-Serveranwendung, und klicken Sie dann auf **Eigenschaften.**

3.  Klicken Sie **im** Dialogfeld Eigenschaften auf die **Registerkarte Aktivierung.**

4.  Aktivieren Sie **im Feld Aktivierungstyp** das Kontrollkästchen **Anwendung als NT-Dienst** ausführen.

    > [!Note]  
    > Das **Kontrollkästchen Anwendung als NT-Dienst ausführen** ist nur für Serveranwendungen und für Bibliotheksanwendungen deaktiviert.

     

5.  Klicken Sie auf **die Schaltfläche Neuen Dienst** einrichten.

6.  Wählen Sie **im Dialogfeld** Dienstname im Feld Starttyp die Option **Automatisch oder** **Manuell aus.** 

7.  (Optional) Wählen Sie im Feld Fehlerbehandlung die Option **Ignorieren,** **Normal,** Schwerwiegend oder Kritisch aus, um die Aktion anzugeben, die für einen **bestimmten Fehler ergriffen werden** soll.   Jede Option ist wie folgt verhalten:

    1.  **Ignore** (Ignorieren): Das Startprogramm protokolliert den Fehler, setzt den Startvorgang jedoch fort.
    2.  **Normal.** Der Fehler wird protokolliert, ein Meldungsfeld wird angezeigt, und das Startprogramm setzt den Startvorgang fort.
    3.  **Schwerwiegend.** Der Fehler wird protokolliert, und das System wird mit der letzten als fehlerfrei bekannten Konfiguration neu gestartet. Wenn es sich um die letzte als funktionierend bekannte Konfiguration handelt, die gestartet wird, wenn der Fehler protokolliert wird, wird der Startvorgang fortgesetzt.
    4.  **Kritisch**. Der Fehler wird protokolliert, und das System wird mit der letzten als fehlerfrei bekannten Konfiguration neu gestartet. Wenn es sich um die letzte als funktionierend bekannte Konfiguration handelt, die gestartet wird, wenn der Fehler protokolliert wird, schlägt der Startvorgang fehl.

8.  (Optional) Wenn Sie andere Dienste als abhängig festlegen möchten, wählen Sie die abhängigen Dienste aus der Liste im Feld **Abhängigkeiten** aus.

9.  (Optional) Aktivieren Sie das Kontrollkästchen Dienst die Interaktion mit Desktop zulassen, um anzugeben, dass der Dienst mit dem Desktop **interagieren** darf.

10. Klicken Sie auf **Erstellen**.

11. (Optional) So weisen Sie den Dienst einem Benutzerkonto zu:

    1.  Wählen Sie **auf der** Registerkarte Identität die Option Dieser **Benutzer aus.**
    2.  Um den Benutzer auszuwählen, geben Sie den Benutzernamen in das Feld **Benutzer ein,** oder klicken Sie **auf die Schaltfläche** Durchsuchen.
    3.  Geben Sie im Feld Kennwort das Kennwort für das **Benutzerkonto** ein.
    4.  Geben Sie das gleiche Kennwort in das Feld **Kennwort bestätigen** ein.

 

 



