---
title: COM-Klassen Objekte und CLSIDs
description: Ein com-Server wird als com-Klasse implementiert.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfde2f379c4c7589db4cde283c8c67d720b21d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341334"
---
# <a name="com-class-objects-and-clsids"></a>COM-Klassen Objekte und CLSIDs

Ein com-Server wird als com-Klasse implementiert. Eine *com-Klasse* ist eine Implementierung einer Gruppe von Schnittstellen im Code, die ausgeführt wird, wenn Sie mit einem bestimmten Objekt interagieren. Es gibt einen wichtigen Unterschied zwischen einer C++-Klasse und einer com-Klasse: in C++ handelt es sich bei einer Klasse um einen-Typ, während eine COM-Klasse lediglich eine Definition des-Objekts ist und keinen Typ aufweist, obwohl ein C++-Programmierer ihn mithilfe einer C++-Klasse implementieren kann. COM ist so konzipiert, dass eine Klasse von verschiedenen Anwendungen verwendet werden kann, einschließlich Anwendungen, die ohne Kenntnis der Existenz der jeweiligen Klasse geschrieben wurden. Daher ist der Klassen Code für einen bestimmten Objekttyp entweder in einer Dynamic Linked Library (dll) oder in einer anderen ausführbaren Anwendung (exe) vorhanden.

Jede com-Klasse wird durch eine *CLSID* identifiziert, eine eindeutige 128-Bit-GUID, die vom Server registriert werden muss. COM verwendet diese CLSID bei der Anforderung eines Clients, um der DLL oder exe, die den Code enthält, der die-Klasse implementiert, bestimmte Daten zuzuordnen und so eine Instanz des-Objekts zu erstellen.

Für Clients und Server auf demselben Computer ist die CLSID des Servers alles, was der Client jemals benötigt. Auf jedem Computer verwaltet com eine Datenbank (die Systemregistrierung auf Microsoft Windows-und Macintosh-Plattformen nutzt) aller CLSIDs für die auf dem System installierten Server. Dabei handelt es sich um eine Zuordnung zwischen jeder CLSID und dem Speicherort der DLL oder exe-Datei, die den Code für diese CLSID enthält. COM konsultiert diese Datenbank immer dann, wenn ein Client eine Instanz einer com-Klasse erstellen und seine Dienste verwenden möchte, damit der Client niemals den absoluten Speicherort des Codes auf dem Computer kennen muss.

Bei verteilten Systemen stellt com Registrierungseinträge bereit, mit denen sich ein Remote Server selbst für die Verwendung durch einen Client registrieren kann. Obwohl Anwendungen nur eine CLSID eines Servers benötigen, da Sie sich auf die Registrierung des Servers verlassen können, ermöglicht com Clients das Überschreiben von Registrierungs Einträgen und das Angeben von Serverstandorten, um das Netzwerk in vollem Umfang zu nutzen. (Siehe suchen [eines Remote Objekts](locating-a-remote-object.md).)

Die grundlegende Möglichkeit zum Erstellen einer Instanz einer-Klasse ist die Verwendung eines com- *Klassen Objekts*. Dabei handelt es sich einfach um ein zwischen Objekt, das Funktionen unterstützt, die zum Erstellen neuer Instanzen einer bestimmten Klasse gemeinsam sind. Die meisten Klassen Objekte, die zum Erstellen von Objekten aus einer CLSID verwendet werden, unterstützen die [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -Schnittstelle, eine Schnittstelle mit der wichtigen Methode " [**kreateinstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) " Sie implementieren eine **IClassFactory** -Schnittstelle für jede Objektklasse, die Sie instanziiert werden. (Weitere Informationen zum Implementieren von **IClassFactory** finden Sie unter [Implementieren von IClassFactory](implementing-iclassfactory.md).)

> [!Note]  
> Server, die eine andere benutzerdefinierte Klassenfactoryschnittstelle unterstützen, müssen [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) nicht speziell unterstützen. Aufrufe von anderen Aktivierungs Funktionen als [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (z. b. [**cokreateinstanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)) erfordern jedoch, dass der Server **IClassFactory** unterstützt.

 

Wenn ein Client eine Instanz des Server Objekts erstellen möchte, verwendet er die CLSID des gewünschten Objekts in einem Aufrufen von [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). (Dieser-Befehl kann entweder direkt oder implizit über eine der Hilfsfunktionen für die Objekt Erstellung erfolgen.) Diese Funktion dient zum Lokalisieren des mit der CLSID verknüpften Codes, erstellt ein Klassenobjekt und stellt einen Zeiger auf die angeforderte-Schnittstelle bereit. (**CoGetClassObject** nimmt einen *riid* -Parameter an, der den gewünschten Schnittstellen Zeiger des Clients angibt.)

> [!Note]  
> COM verfügt nur über einige Funktionen, auf denen viele der anderen erstellt werden. Die wichtigste davon ist wahrscheinlich [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), das allen Instanzen Erstellungs Funktionen zugrunde liegt.

 

Mit diesem Zeiger kann der Aufrufer eine Instanz des Objekts erstellen und einen Zeiger auf eine angeforderte Schnittstelle für das Objekt abrufen. Dabei handelt es sich normalerweise um eine Initialisierungs Schnittstelle, mit der das Objekt aktiviert (in den Zustand "wird ausgeführt" versetzt wird), sodass der Client die Arbeit mit dem gewünschten Objekt erledigen kann. Mit den grundlegenden Funktionen von com muss der Client auch darauf achten, alle Objekt Zeiger freizugeben.

Ein weiterer Mechanismus zum Aktivieren von Objektinstanzen ist der klassenmoniker. Klassenmoniker binden an das Klassenobjekt der Klasse, für die Sie erstellt werden. Weitere Informationen finden Sie unter [klassenmoniker](class-monikers.md).

COM bietet mehrere Hilfsfunktionen, die das Erstellen von Objektinstanzen reduzieren. Diese werden in [Hilfsfunktionen](instance-creation-helper-functions.md)für die Instanzerstellung beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Objekts über ein Klassenobjekt](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 