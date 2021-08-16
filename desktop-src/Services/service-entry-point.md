---
description: Dienste werden im Allgemeinen als Konsolenanwendungen geschrieben.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Diensteinstiegspunkt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8f44322048351161bb8f3b8afdd619129d18b5effb5dc850d8909afbb3673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888972"
---
# <a name="service-entry-point"></a>Diensteinstiegspunkt

Dienste werden im Allgemeinen als Konsolenanwendungen geschrieben. Der Einstiegspunkt einer Konsolenanwendung ist die **Hauptfunktion.** Die **main-Funktion** empfängt Argumente vom **ImagePath-Wert** aus dem Registrierungsschlüssel für den Dienst. Weitere Informationen finden Sie im Abschnitt "Hinweise" der [**CreateService-Funktion.**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)

Wenn der SCM ein Dienstprogramm startet, wartet er darauf, dass er die [**Funktion StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) aufruft. Befolgen Sie die folgenden Richtlinien.

-   Ein Dienst vom Typ SERVICE \_ WIN32 \_ OWN PROCESS sollte \_ [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) sofort über seinen Hauptthread aufrufen. Sie können eine beliebige Initialisierung nach dem Start des Diensts ausführen, wie unter [Service ServiceMain-Funktion](service-servicemain-function.md)beschrieben.
-   Wenn der Diensttyp SERVICE \_ WIN32 SHARE PROCESS lautet und es eine gemeinsame \_ \_ Initialisierung für alle Dienste im Programm gibt, können Sie die Initialisierung im Hauptthread ausführen, bevor [**Sie StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)aufrufen, sofern dies weniger als 30 Sekunden dauert. Andernfalls müssen Sie einen anderen Thread erstellen, um die allgemeine Initialisierung durchzuführen, während der Hauptthread **StartServiceCtrlDispatcher** aufruft. Sie sollten nach dem Start des Diensts weiterhin eine dienstspezifische Initialisierung ausführen.

Die [**StartServiceCtrlDispatcher-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) übernimmt eine [**SERVICE TABLE \_ \_ ENTRY-Struktur**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) für jeden im Prozess enthaltenen Dienst. Jede -Struktur gibt den Dienstnamen und den Einstiegspunkt für den Dienst an. Ein Beispiel finden Sie unter [Schreiben der Hauptfunktion eines Dienstprogramms.](writing-a-service-program-s-main-function.md)

Wenn [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) erfolgreich ist, gibt der aufrufende Thread erst dann zurück, wenn alle ausgeführten Dienste im Prozess den Status SERVICE STOPPED erreicht \_ haben. Der SCM sendet Über eine Named Pipe Steuerungsanforderungen an diesen Thread. Der Thread fungiert als Steuerungsdisponent und führt die folgenden Aufgaben aus:

-   Erstellen Sie einen neuen Thread, um den entsprechenden Einstiegspunkt aufzurufen, wenn ein neuer Dienst gestartet wird.
-   Rufen Sie die entsprechende [Handlerfunktion](service-control-handler-function.md) auf, um Dienststeuerungsanforderungen zu verarbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben der Hauptfunktion eines Dienstprogramms](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



