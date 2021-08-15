---
description: In diesem Thema wird beschrieben, wie Eine DLL für einen DirectShow-Filter mithilfe der DirectShow-Basisklassen implementiert wird.
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Klassen factorys und Factoryvorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9329a0b8cfd22a316add88664604df190ae96c765359c723aa2302c5b1fa1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402213"
---
# <a name="class-factories-and-factory-templates"></a>Klassen factorys und Factoryvorlagen

In diesem Thema wird beschrieben, wie eine DLL für einen DirectShow-Filter mithilfe der [DirectShow-Basisklassen implementiert wird.](directshow-base-classes.md)

Bevor ein Client eine Instanz eines COM-Objekts erstellt, erstellt er mithilfe eines Aufrufs der [**CoGetClassObject-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) eine Instanz der Klassen factory des Objekts. Der Client ruft dann die **IClassFactory::CreateInstance-Methode** der Klassenfactory auf. Es ist die Klassen factory, die die Komponente tatsächlich erstellt und einen Zeiger auf die angeforderte Schnittstelle zurückgibt. (Die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) kombiniert diese Schritte innerhalb des Funktionsaufrufs.)

Die folgende Abbildung zeigt die Sequenz von Methodenaufrufen.

![Methodenaufrufe zum Erstellen einer Klassen factory](images/classfactory.png)

[**CoGetClassObject ruft**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) die [**DllGetClassObject-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) auf, die in der DLL definiert ist. Diese Funktion erstellt die Klassen factory und gibt einen Zeiger auf eine Schnittstelle in der Klassen factory zurück. DirectShow implementiert **DllGetClassObject** für Sie, aber die Funktion basiert auf einem bestimmten Code. Um die Funktionsweise zu verstehen, müssen Sie verstehen, wie DirectShow Klassen factorys implementiert.

Eine Klassen factory ist ein COM-Objekt, das für die Erstellung eines anderen COM-Objekts de dedicated ist. Jede Klassen factory verfügt über einen Objekttyp, den sie erstellt. In DirectShow ist jede Klassenfactory eine Instanz derselben C++-Klasse, **CClassFactory.** Klassenfactorys werden mit einer anderen Klasse, [**CFactoryTemplate,**](cfactorytemplate.md)spezialisiert, die auch als *Factoryvorlage bezeichnet wird.* Jede Klassen factory enthält einen Zeiger auf eine Factoryvorlage. Die Factoryvorlage enthält Informationen zu einer bestimmten Komponente, z. B. den Klassenbezeichner der Komponente (CLSID) und einen Zeiger auf eine Funktion, die die Komponente erstellt.

Die DLL deklariert ein globales Array von Factoryvorlagen, eine für jede Komponente in der DLL. Wenn [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) eine neue Klassen factory erstellt, durchsucht es das Array nach einer Vorlage mit einer übereinstimmenden CLSID. Wenn eine gefunden wird, wird eine Klassen factory erstellt, die einen Zeiger auf die übereinstimmende Vorlage enthält. Wenn der Client **IClassFactory::CreateInstance** aufruft, ruft die Klassenfactory die in der Vorlage definierte Instanziierungsfunktion auf.

Die folgende Abbildung zeigt die Sequenz von Methodenaufrufen.

![Klassen-Factoryvorlagen in einer DLL](images/classfactory2.png)

Der Vorteil dieser Architektur ist, dass Sie nur einige Komponenten definieren können, die spezifisch für Ihre Komponente sind, z. B. die Instanziierungsfunktion, ohne die gesamte Klassen factory zu implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer DirectShow-Filter-DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 
