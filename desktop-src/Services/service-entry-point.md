---
description: Dienste werden im Allgemeinen als Konsolen Anwendungen geschrieben.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Dienst Einstiegspunkt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9e2683c4a69949b6f51c7d000c0ee3571fe118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958864"
---
# <a name="service-entry-point"></a>Dienst Einstiegspunkt

Dienste werden im Allgemeinen als Konsolen Anwendungen geschrieben. Der Einstiegspunkt einer Konsolenanwendung ist die **Haupt** Funktion. Die **Main** -Funktion empfängt Argumente aus dem **ImagePath** -Wert aus dem Registrierungsschlüssel für den Dienst. Weitere Informationen finden Sie im Abschnitt "Hinweise" der Funktion "| [**ateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ".

Wenn der SCM ein Dienstprogramm startet, wartet er darauf, dass er die Funktion " [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) " aufruft. Verwenden Sie die folgenden Richtlinien.

-   Ein Dienst vom Typ "Dienst \_ Win32- \_ eigener Prozess" \_ sollte [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) direkt aus seinem Haupt Thread aufrufen. Sie können nach dem Starten des Diensts eine beliebige Initialisierung ausführen, wie in der [Service Main-Funktion des Diensts](service-servicemain-function.md)beschrieben.
-   Wenn der Diensttyp ein \_ Win32-Freigabeprozess des Diensts ist \_ \_ und eine allgemeine Initialisierung für alle Dienste im Programm vorhanden ist, können Sie die Initialisierung im Haupt Thread ausführen, bevor Sie [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)aufrufen, solange Sie weniger als 30 Sekunden benötigt. Andernfalls müssen Sie einen weiteren Thread erstellen, um die allgemeine Initialisierung durchzuführen, während der Haupt Thread **StartServiceCtrlDispatcher** aufruft. Nach dem Starten des Diensts sollten Sie weiterhin eine beliebige Dienst spezifische Initialisierung ausführen.

Die [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) -Funktion nimmt für jeden Dienst, der im Prozess enthalten ist, eine [**Dienst \_ Tabellen \_ Eintrags**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) Struktur. Jede Struktur gibt den Dienstnamen und den Einstiegspunkt für den Dienst an. Ein Beispiel finden Sie unter [Schreiben der Hauptfunktion eines Dienstprogramms](writing-a-service-program-s-main-function.md).

Wenn [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) erfolgreich ist, gibt der aufrufende Thread erst dann zurück, wenn alle laufenden Dienste im Prozess den Status "beendet" eingegeben haben \_ . Der SCM sendet Steuerungsanforderungen über eine Named Pipe an diesen Thread. Der Thread fungiert als Steuerelement Verteiler und führt die folgenden Aufgaben aus:

-   Erstellen Sie einen neuen Thread, um den entsprechenden Einstiegspunkt aufzurufen, wenn ein neuer Dienst gestartet wird.
-   Ruft die entsprechende [Handlerfunktion](service-control-handler-function.md) auf, um Dienst Steuerungsanforderungen zu verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben der Hauptfunktion eines Dienstprogramms](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



