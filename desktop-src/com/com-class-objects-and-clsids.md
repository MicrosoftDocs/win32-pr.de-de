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

Ein COM-Server wird als COM-Klasse implementiert. Eine *COM-Klasse* ist eine Implementierung einer Gruppe von Schnittstellen im Code, die ausgeführt wird, wenn Sie mit einem bestimmten Objekt interagieren. Es gibt einen wichtigen Unterschied zwischen einer C++-Klasse und einer COM-Klasse: In C++ ist eine Klasse ein Typ, während eine COM-Klasse einfach eine Definition des Objekts ist und keinen Typ enthält, obwohl ein C++-Programmierer sie mithilfe einer C++-Klasse implementieren kann. COM ist so konzipiert, dass eine Klasse von verschiedenen Anwendungen verwendet werden kann, einschließlich Anwendungen, die ohne Kenntnis des Vorhandenseins dieser bestimmten Klasse geschrieben wurden. Daher ist Klassencode für einen bestimmten Objekttyp entweder in einer dll (Dynamic Linked Library) oder in einer anderen ausführbaren Anwendung (EXE) vorhanden.

Jede COM-Klasse wird durch eine *CLSID* identifiziert, eine eindeutige 128-Bit-GUID, die der Server registrieren muss. COM verwendet diese CLSID auf Anforderung eines Clients, um bestimmte Daten der DLL oder EXE-Datei zu zuordnen, die den Code enthält, der die -Klasse implementiert, wodurch eine Instanz des -Objekts erstellt wird.

Für Clients und Server auf demselben Computer ist die CLSID des Servers alles, was der Client jemals benötigt. Auf jedem Computer verwaltet COM eine Datenbank (sie nutzt die Systemregistrierung auf Microsoft Windows- und Macintosh-Plattformen) aller CLSIDs für die auf dem System installierten Server. Dies ist eine Zuordnung zwischen jeder CLSID und dem Speicherort der DLL oder EXE, die den Code für diese CLSID enthält. COM verwendet diese Datenbank immer dann, wenn ein Client eine Instanz einer COM-Klasse erstellen und seine Dienste verwenden möchte, sodass der Client nie den absoluten Speicherort des Codes auf dem Computer kennen muss.

Für verteilte Systeme stellt COM Registrierungseinträge zur Verfügung, mit denen sich ein Remoteserver für die Verwendung durch einen Client registrieren kann. Während Anwendungen nur die CLSID eines Servers kennen müssen, da sie sich auf die Registrierung verlassen können, um den Server zu finden, ermöglicht COM Clients das Überschreiben von Registrierungseinträgen und das Angeben von Serverstandorten, um das Netzwerk voll zu nutzen. (Siehe [Suchen eines Remoteobjekts](locating-a-remote-object.md).)

Die grundlegende Methode zum Erstellen einer Instanz einer Klasse ist über ein *COM-Klassenobjekt.* Dies ist einfach ein Zwischenobjekt, das Funktionen unterstützt, die zum Erstellen neuer Instanzen einer bestimmten Klasse gemeinsam sind. Die meisten Klassenobjekte, die zum Erstellen von Objekten aus einer CLSID verwendet werden, unterstützen die [**IClassFactory-Schnittstelle,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) eine Schnittstelle, die die wichtige [**CreateInstance-Methode**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) enthält. Sie implementieren eine **IClassFactory-Schnittstelle** für jede Objektklasse, die Instanziiert werden soll. (Weitere Informationen zum Implementieren von **IClassFactory finden** Sie unter [Implementieren von IClassFactory](implementing-iclassfactory.md).)

> [!Note]  
> Server, die eine andere benutzerdefinierte Klassenfactoryschnittstelle unterstützen, sind nicht erforderlich, um [**IClassFactory speziell zu**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) unterstützen. Aufrufe anderer Aktivierungsfunktionen als [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (z. B. [**CoCreateInstanceEx)**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)erfordern jedoch, dass der Server **IClassFactory unterstützt.**

 

Wenn ein Client eine Instanz des -Objekts des Servers erstellen möchte, verwendet er die CLSID des gewünschten Objekts in einem Aufruf von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). (Dieser Aufruf kann entweder direkt oder implizit über eine der Hilfsfunktionen für die Objekterstellung sein.) Diese Funktion sucht den code, der der CLSID zugeordnet ist, erstellt ein Klassenobjekt und stellt einen Zeiger auf die angeforderte Schnittstelle bereit. (**CoGetClassObject** verwendet einen *riid-Parameter,* der den gewünschten Schnittstellenzeiger des Clients angibt.)

> [!Note]  
> COM verfügt nur über einige Wenige Funktionen, auf denen viele der anderen Funktionen aufgebaut sind. Das wichtigste davon ist wahrscheinlich [**CoGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)das allen Instanzerstellungsfunktionen zugrunde liegt.

 

Mit diesem Zeiger kann der Aufrufer eine Instanz des -Objekts erstellen und einen Zeiger auf eine angeforderte Schnittstelle für das Objekt abrufen. Dies ist normalerweise eine Initialisierungsschnittstelle, die verwendet wird, um das Objekt zu aktivieren (es in den Ausführungszustand zu bringen), sodass der Client mit dem Objekt arbeiten kann, das er verwenden möchte. Mithilfe der grundlegenden COM-Funktionen muss der Client auch darauf achten, alle Objektze0er frei zu geben.

Ein weiterer Mechanismus zum Aktivieren von Objektinstanzen ist der Klassenmoniker. Klassenmoniker werden an das Klassenobjekt der Klasse gebunden, für die sie erstellt werden. Weitere Informationen finden Sie unter [Klassenmoniker.](class-monikers.md)

COM stellt mehrere Hilfsfunktionen zur Verfügung, die die Erstellung von Objektinstanzen reduzieren. Diese werden unter [Instanzerstellungs-Hilfsfunktionen beschrieben.](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Objekts über ein Klassenobjekt](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 