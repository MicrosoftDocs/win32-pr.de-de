---
title: COM-Klassenobjekte und CLSIDs
description: Ein COM-Server wird als COM-Klasse implementiert.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6bcd00f886d3a754a44658e669189d28fd2fa121248b667ba2a3928b626f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550624"
---
# <a name="com-class-objects-and-clsids"></a>COM-Klassenobjekte und CLSIDs

Ein COM-Server wird als COM-Klasse implementiert. Eine *COM-Klasse* ist eine Implementierung einer Gruppe von Schnittstellen in Code, die immer dann ausgeführt wird, wenn Sie mit einem bestimmten Objekt interagieren. Es gibt einen wichtigen Unterschied zwischen einer C++-Klasse und einer COM-Klasse: In C++ ist eine Klasse ein Typ, während eine COM-Klasse einfach eine Definition des Objekts ist und keinen Typ enthält, obwohl ein C++-Programmierer sie möglicherweise mithilfe einer C++-Klasse implementiert. COM ist so konzipiert, dass eine Klasse von verschiedenen Anwendungen verwendet werden kann, einschließlich Anwendungen, die ohne Kenntnis der Existenz dieser bestimmten Klasse geschrieben wurden. Daher ist Klassencode für einen bestimmten Objekttyp entweder in einer dll -Datei (Dynamic Linked Library) oder in einer anderen ausführbaren Anwendung (EXE) vorhanden.

Jede COM-Klasse wird durch eine *CLSID* identifiziert, eine eindeutige 128-Bit-GUID, die der Server registrieren muss. COM verwendet diese CLSID auf Anforderung eines Clients, um der DLL oder EXE, die den Code enthält, der die Klasse implementiert, bestimmte Daten zuzuordnen und so eine Instanz des -Objekts zu erstellen.

Für Clients und Server auf demselben Computer ist die CLSID des Servers alles, was der Client jemals benötigt. Auf jedem Computer verwaltet COM eine Datenbank (die die Systemregistrierung auf Microsoft Windows- und Macintosh-Plattformen nutzt) aller CLSIDs für die auf dem System installierten Server. Dies ist eine Zuordnung zwischen jeder CLSID und dem Speicherort der DLL oder EXE, die den Code für diese CLSID enthält. COM verwendet diese Datenbank immer dann, wenn ein Client eine Instanz einer COM-Klasse erstellen und deren Dienste verwenden möchte, sodass der Client nie den absoluten Speicherort des Codes auf dem Computer kennen muss.

Für verteilte Systeme stellt COM Registrierungseinträge bereit, die es einem Remoteserver ermöglichen, sich für die Verwendung durch einen Client zu registrieren. Während Anwendungen nur die CLSID eines Servers kennen müssen, da sie sich auf die Registrierung verlassen können, um den Server zu finden, ermöglicht COM Clients, Registrierungseinträge zu überschreiben und Serverspeicherorte anzugeben, um das Netzwerk voll zu nutzen. (Weitere Informationen finden Sie unter [Suchen eines Remoteobjekts.)](locating-a-remote-object.md)

Die grundlegende Möglichkeit, eine Instanz einer Klasse zu erstellen, besteht in einem *COM-Klassenobjekt.* Dies ist einfach ein Zwischenobjekt, das Funktionen unterstützt, die beim Erstellen neuer Instanzen einer bestimmten Klasse üblich sind. Die meisten Klassenobjekte, die zum Erstellen von Objekten aus einer CLSID verwendet werden, unterstützen die [**IClassFactory-Schnittstelle,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) eine Schnittstelle, die die wichtige [**CreateInstance-Methode**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) enthält. Sie implementieren eine **IClassFactory-Schnittstelle** für jede Objektklasse, die Instanziiert werden soll. (Weitere Informationen zum Implementieren von **IClassFactory** finden Sie unter [Implementing IClassFactory](implementing-iclassfactory.md).)

> [!Note]  
> Server, die eine andere benutzerdefinierte Klassenfactoryschnittstelle unterstützen, sind nicht erforderlich, um [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) speziell zu unterstützen. Für Aufrufe anderer Aktivierungsfunktionen als [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (z. B. [**CoCreateInstanceEx)**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)muss der Server **jedoch IClassFactory** unterstützen.

 

Wenn ein Client eine Instanz des Serverobjekts erstellen möchte, verwendet er die CLSID des gewünschten Objekts in einem Aufruf von [**CoGetClassObject.**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (Dieser Aufruf kann entweder direkt oder implizit über eine der Hilfsfunktionen für die Objekterstellung erfolgen.) Diese Funktion sucht den Code, der der CLSID zugeordnet ist, erstellt ein Klassenobjekt und stellt einen Zeiger auf die angeforderte Schnittstelle bereit. (**CoGetClassObject** verwendet einen *riid-Parameter,* der den gewünschten Schnittstellenzeiger des Clients angibt.)

> [!Note]  
> COM verfügt nur über wenige Funktionen, auf denen viele der anderen basieren. Die wichtigste davon ist wahrscheinlich [**CoGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)das allen Funktionen zur Instanzerstellung zugrunde liegt.

 

Mit diesem Zeiger kann der Aufrufer eine Instanz des Objekts erstellen und einen Zeiger auf eine angeforderte Schnittstelle für das Objekt abrufen. Dies ist in der Regel eine Initialisierungsschnittstelle, die zum Aktivieren des Objekts verwendet wird (versetzen Sie es in den Ausführungszustand), sodass der Client mit dem gewünschten Objekt arbeiten kann. Bei Verwendung der grundlegenden FUNKTIONEN von COM muss der Client auch darauf achten, alle Objektzeiger freizugeben.

Ein weiterer Mechanismus zum Aktivieren von Objektinstanzen ist der Klassenmoniker. Klassenmoniker werden an das Klassenobjekt der Klasse gebunden, für die sie erstellt werden. Weitere Informationen finden Sie unter [Klassenmoniker.](class-monikers.md)

COM stellt mehrere Hilfsfunktionen bereit, die die Arbeit beim Erstellen von Objektinstanzen reduzieren. Diese werden unter [Hilfsfunktionen für die Instanzerstellung](instance-creation-helper-functions.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Objekts über ein Klassenobjekt](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 