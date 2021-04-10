---
description: Eine COM+-Serveranwendung kann als Dienst erstellt werden, um entweder automatisch während des Systemstarts oder manuell durch Aktivierungen gestartet zu werden.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Konfigurieren einer com+-Server Anwendung als Dienst Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860852"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a>Konfigurieren einer com+-Server Anwendung als Dienst Anwendung

Eine COM+-Serveranwendung kann als Dienst erstellt werden, um entweder automatisch während des Systemstarts oder manuell durch Aktivierungen gestartet zu werden. Wenn der Dienst nicht gestartet werden kann, gibt die Option für die Fehlerbehandlung den Schweregrad des Fehlers an und legt fest, welche Aktion ausgeführt werden soll. Die Option zum Konfigurieren eines Dienstanbieter, der als lokales Systemkonto ausgeführt werden soll, ist ebenfalls verfügbar, und die Option zum Zuweisen eines bestimmten Benutzerkontos, für das die COM+-Serveranwendung ausgeführt wird. Abhängigkeiten können auch in einer Liste der Dienste ausgewählt werden, die mithilfe von Komponenten Diensten auf dem Computer registriert sind. Dadurch wird festgelegt, welche Dienste vor dem Start dieses Diensts ausgeführt werden müssen.

**So konfigurieren Sie eine COM+-Anwendung für die Durchführung als Dienst**

1.  Suchen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste die COM+-Serveranwendung, die Sie als Dienst ausführen möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung com+ Server, und klicken Sie dann auf **Eigenschaften**.

3.  Klicken Sie im Dialogfeld **Eigenschaften** auf die Registerkarte **Aktivierung** .

4.  Aktivieren Sie im Feld **Aktivierungstyp** das Kontrollkästchen **Anwendung als NT-Dienst ausführen** .

    > [!Note]  
    > Das Kontrollkästchen **Anwendung als NT-Dienst ausführen** ist nur für Server Anwendungen aktiviert und für Bibliotheksanwendungen deaktiviert.

     

5.  Klicken Sie auf die Schaltfläche **neuen Dienst einrichten** .

6.  Wählen Sie im Feld **Starttyp** im Dialogfeld **Dienst Name** die Option **automatisch** oder **manuell** aus.

7.  Optionale Um die Aktion anzugeben, die für einen bestimmten Fehler ausgeführt werden soll, wählen Sie im Feld **Fehlerbehandlung** die Option **ignorieren**, **Normal**, **schwerwiegend** oder **kritisch** aus. Die einzelnen Optionen zugeordneten Verhalten lauten wie folgt:

    1.  **Ignore** (Ignorieren): Der Fehler wird vom Start Programm protokolliert, aber der Startvorgang wird fortgesetzt.
    2.  **Normal**. Der Fehler wird protokolliert, ein Meldungs Feld wird angezeigt, und der Startvorgang wird vom Start Programm fortgesetzt.
    3.  **Schwerwiegend**. Der Fehler wird protokolliert, und das System wird mit der letzten als funktionierend bekannten Konfiguration neu gestartet. Wenn es sich um die letzte bekannte, gute Konfiguration handelt, die beim Protokollieren des Fehlers gestartet wird, wird der Startvorgang fortgesetzt.
    4.  **Kritisch**. Der Fehler wird protokolliert, und das System wird mit der letzten als funktionierend bekannten Konfiguration neu gestartet. Wenn es sich um die letzte als funktionierend bekannte Konfiguration handelt, die beim Protokollieren des Fehlers gestartet wird, tritt beim Startvorgang ein Fehler auf.

8.  Optionale Um andere Dienste als abhängig festzulegen, wählen Sie die abhängigen Dienste aus der Liste im Feld **Abhängigkeiten** aus.

9.  Optionale Aktivieren Sie das Kontrollkästchen **Dienst für die Interaktion mit dem Desktop zulassen** , um anzugeben, dass der Dienst mit dem Desktop interagieren darf.

10. Klicken Sie auf **Erstellen**.

11. Optionale So weisen Sie den Dienst einem Benutzerkonto zu:

    1.  Wählen Sie auf der Registerkarte **Identität** den **Benutzer** aus.
    2.  Geben Sie den Benutzernamen in das Feld **Benutzer** ein, oder klicken Sie auf die Schaltfläche **Durchsuchen** , um den Benutzer auszuwählen.
    3.  Geben Sie im Feld **Kennwort** das Kennwort für das Benutzerkonto ein.
    4.  Geben Sie das gleiche Kennwort in das Feld **Kennwort bestätigen** ein.

 

 



