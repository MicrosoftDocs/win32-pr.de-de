---
description: Der COM+-Ereignisdienst verwendet ein Ereignisklassenobjekt, um die Verbindung zwischen Verleger und Abonnent zu verwalten.
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: Das COM+-Ereignisklassenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5650969895cdfa63f07e6ba77e617a962335101d4f56aeb21a5b439b27daaf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546152"
---
# <a name="the-com-event-class-object"></a>Das COM+-Ereignisklassenobjekt

Der COM+-Ereignisdienst verwendet ein *Ereignisklassenobjekt,* um die Verbindung zwischen Verleger und Abonnent zu verwalten. Das Ereignisklassenobjekt ist eine COM+-Komponente, die vom COM+-Ereignissystem verwaltet und gespeichert wird und die Schnittstellen und Methoden enthält, mit denen ein Herausgeber Ereignisse ausschalten kann. Es handelt sich um ein persistentes Objekt, das die Ereignisse angibt, die auftreten können, und optional den Herausgeber identifiziert. Sie geben die Schnittstellen und Methoden an, die eine Ereignisklasse enthalten soll, indem Sie eine Typbibliothek bereitstellen.

Um ein Ereignis zu erzeugen, instanziiert der Herausgeber das Ereignisklassenobjekt, indem er [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder die Microsoft Visual Basic **CreateObject-Methode** aufruft und die Ereignisschnittstelle anfing, zurückgegeben zu werden. Das instanziierte Ereignisklassenobjekt enthält die Implementierung der angeforderten Schnittstelle des Ereignissystems. Ein interessierter Abonnent muss auch die Ereignisklassenschnittstelle implementieren, um Ereignisse von einem bestimmten Herausgeber zu empfangen. Wenn das Ereignisklassenobjekt instanziiert wird, ordnet das Ereignissystem es den entsprechenden Abonnenten zu. Die Liste der Abonnenten wird für die Lebensdauer des Ereignisklassenobjekts beibehalten. Ein Ereignis kann entweder seriell oder parallel an mehrere Abonnenten übermittelt werden.

Wenn Sie ein Ereignisklassenobjekt implementieren, sollten Sie eine selbstregistrierungsbasierte DLL bereitstellen, die die [**Funktionen DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) und [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) exportiert. Die **DllRegisterServer-Funktion** registriert eine COM-Klasse, und die **DllUnregisterServer-Funktion** aufheben die Registrierung der Komponente. Ereignisklassenobjekte werden im COM+-Katalog gespeichert, entweder mit dem Component Services-Verwaltungstool oder programmgesteuert mithilfe der Methoden der [**Schnittstellen ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) oder [**ICOMAdminCatalog::InstallMultipleEventClasses.**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) Ausführliche Informationen zum Registrieren von Ereignisklassenobjekten finden Sie unter [Registrieren einer Ereignisklasse.](registering-an-event-class.md)

Da Ereignisklassenobjekte konfigurierte Komponenten sind, können andere Attribute, z. B. Warteschlangen, Transaktionen, Sicherheit und so weiter, für sie konfiguriert werden, indem entweder das Verwaltungstool Komponentendienste oder die COM+-Verwaltungs-SDK-Funktionen verwendet werden.

> [!Note]  
> Der COM+-Ereignisdienst verwendet das Marshalling von Typbibliotheken. Dadurch gelten einige Einschränkungen für Ereignisklassenschnittstellen. Der Typbibliotheks-Marshaller unterstützt beispielsweise nicht die Größe der MIDL-Attribute [**\_ und**](/windows/desktop/Midl/size-is) [**die Länge \_ ist**](/windows/desktop/Midl/length-is).

 

Ein Ereignisklassenobjekt besitzt Veröffentlichungsattribute, die bestimmen, wie Ereignisse veröffentlicht werden, sowie die folgenden Eigenschaften:

-   **EventCLSID**. Ein eindeutiger Bezeichner, der die CLSID der Komponente angibt.
-   **EventClassName**. Ein eindeutiger Bezeichner, der die PROGID der Komponente angibt.
-   **TypeLibrary**. Stellt eine Liste der Schnittstellen bereit, die vom Ereignisklassenobjekt angeboten werden. Es ist nicht notwendig, die in der Typbibliothek angegebenen auslobenden Schnittstellen zu implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheitsüberlegungen zu COM+-Ereignissen](com--events-security-considerations.md)
</dt> <dt>

[Filtern von Ereignissen in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Veröffentlichen und Bereitstellen von Ereignissen in COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Verwenden von COM+-Ereignissen mit COM+-Komponenten in der Warteschlange](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
