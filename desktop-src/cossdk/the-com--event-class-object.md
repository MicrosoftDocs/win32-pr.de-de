---
description: Der com+-Ereignis Dienst verwendet ein Ereignis Klassenobjekt zum Verwalten der Verbindung zwischen Verleger und Abonnent.
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: Das com+-Ereignis Klassenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae397f647354ac24395fa073365160829a687a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958352"
---
# <a name="the-com-event-class-object"></a>Das com+-Ereignis Klassenobjekt

Der com+-Ereignis Dienst verwendet ein *Ereignis Klassenobjekt* zum Verwalten der Verbindung zwischen Verleger und Abonnent. Das Ereignis Klassenobjekt ist eine COM+-Komponente, die vom com+-Ereignis System verwaltet und gespeichert wird und die Schnittstellen und Methoden enthält, die von einem Verleger zum Auslösen von Ereignissen verwendet werden. Es handelt sich um ein dauerhaftes Objekt, das die Ereignisse angibt, die auftreten können, und optional den Verleger identifiziert. Sie geben die Schnittstellen und Methoden an, die eine Ereignisklasse enthalten soll, indem Sie eine Typbibliothek bereitstellen.

Zum Auslösen eines Ereignisses instanziiert der Verleger das Ereignis Klassenobjekt durch Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder der Microsoft Visual Basic **CreateObject** -Methode, und es wird angefordert, dass die Ereignis Schnittstelle zurückgegeben wird. Das instanziierte Ereignis Klassenobjekt enthält die Implementierung der angeforderten Schnittstelle des Ereignis Systems. Ein interessierter Abonnent muss auch die Ereignis Klassen Schnittstelle implementieren, um Ereignisse von einem bestimmten Verleger zu empfangen. Wenn das Ereignis Klassenobjekt instanziiert wird, ordnet das Ereignis System es den entsprechenden Abonnenten zu. Die Liste der Abonnenten wird für die Lebensdauer des Ereignis Klassen Objekts beibehalten. Ein Ereignis kann entweder seriell oder parallel an mehrere Abonnenten übermittelt werden.

Wenn Sie ein Ereignis Klassenobjekt implementieren, sollten Sie eine selbst Registrierungs-dll bereitstellen, die die Funktionen [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) exportiert. Die **DllRegisterServer** -Funktion registriert eine COM-Klasse, und die **DllUnregisterServer** -Funktion hebt die Registrierung der Komponente auf. Ereignis Klassen Objekte werden im com+-Katalog gespeichert, entweder mithilfe des Komponenten Dienst-Verwaltungs Tools oder Programm gesteuert mithilfe der Methoden der Schnittstellen [**icomadmincatalog:: installeventclass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) oder [**icomadmincatalog:: installmultipleeventclasses**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) . Ausführliche Informationen zum Registrieren von Ereignis Klassen Objekten finden Sie unter [Registrieren einer Ereignis](registering-an-event-class.md)Klasse.

Da Ereignis Klassen Objekte konfigurierte Komponenten sind, können andere Attribute (z. b. Warteschlangen, Transaktionen, Sicherheit usw.) für Sie konfiguriert werden, indem entweder das Verwaltungs Tool Komponenten Dienste oder die com+-Verwaltungs-SDK-Funktionen verwendet werden.

> [!Note]  
> Der com+-Ereignis Dienst verwendet das Marshalling von Typbibliotheken. Dies stellt einige Einschränkungen für Ereignis Klassen Schnittstellen dar. Der Typbibliothek-Mars Haller unterstützt z. b. die [**Größe \_**](/windows/desktop/Midl/size-is) der mittleren Attribute nicht, und die [**Länge \_ ist**](/windows/desktop/Midl/length-is).

 

Ein Ereignis Klassenobjekt besitzt Veröffentlichungs Attribute, die bestimmen, wie Ereignisse veröffentlicht werden, sowie die folgenden Eigenschaften:

-   **Eventclsid**. Ein eindeutiger Bezeichner, der die CLSID der Komponente angibt.
-   **EventClassName**. Ein eindeutiger Bezeichner, der die ProgID der Komponente angibt.
-   **Typbibliothek**. Stellt eine Liste der Schnittstellen bereit, die vom Ereignis Klassenobjekt angeboten werden. Es ist nicht erforderlich, die in der Typbibliothek angegebenen auslösenden Schnittstellen zu implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheitsüberlegungen für COM+-Ereignisse](com--events-security-considerations.md)
</dt> <dt>

[Filtern von Ereignissen in com+](filtering-events-in-com-.md)
</dt> <dt>

[Veröffentlichen und Bereitstellung von Ereignissen in com+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
