---
description: In diesem Thema wird beschrieben, wie eine DLL für einen DirectShow-Filter mithilfe der DirectShow-Basisklassen implementiert wird.
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Klassen-und factoryvorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02699a8ff0740ddcf1d86b8514fd45dac9e32ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104563951"
---
# <a name="class-factories-and-factory-templates"></a>Klassen-und factoryvorlagen

In diesem Thema wird beschrieben, wie eine DLL für einen DirectShow-Filter mithilfe der [DirectShow-Basisklassen](directshow-base-classes.md)implementiert wird.

Bevor ein Client eine Instanz eines COM-Objekts erstellt, erstellt er mithilfe eines Aufrufens der [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) -Funktion eine Instanz der Klassenfactory des Objekts. Der Client ruft dann die **IClassFactory:: | ateinstance** -Methode der Klassenfactory auf. Die Klassenfactory erstellt die Komponente und gibt einen Zeiger auf die angeforderte Schnittstelle zurück. (Die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion kombiniert diese Schritte innerhalb des Funktions Aufrufes.)

Die folgende Abbildung zeigt die Abfolge von Methoden aufrufen.

![Methodenaufrufe zum Erstellen einer Klassenfactory](images/classfactory.png)

[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) Ruft die [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) -Funktion auf, die in der dll definiert ist. Diese Funktion erstellt die Klassenfactory und gibt einen Zeiger auf eine Schnittstelle in der Klassenfactory zurück. DirectShow implementiert **DllGetClassObject** für Sie, aber die Funktion verwendet den Code auf eine bestimmte Weise. Um zu verstehen, wie es funktioniert, müssen Sie verstehen, wie DirectShow Klassenfactorys implementiert.

Eine Klassenfactory ist ein COM-Objekt, das zum Erstellen eines anderen COM-Objekts dient Jede Klassenfactory hat einen Objekttyp, den Sie erstellt. In DirectShow ist jede Klassenfactory eine Instanz der gleichen C++-Klasse, **cclassfactory**. Klassenfactorys werden mithilfe einer anderen Klasse, [**cfactorytemplate**](cfactorytemplate.md), spezialisiert, auch als Factoryvorlage bezeichnet.  Jede Klassenfactory enthält einen Zeiger auf eine Factoryvorlage. Die Factoryvorlage enthält Informationen zu einer bestimmten Komponente, z. b. den Klassen Bezeichner (CLSID) der Komponente und einen Zeiger auf eine Funktion, die die Komponente erstellt.

Die dll deklariert ein globales Array von Factory-Vorlagen, eines für jede Komponente in der dll. Wenn [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) eine neue Klassenfactory erstellt, durchsucht Sie das Array nach einer Vorlage mit einer entsprechenden CLSID. Wenn Sie einen gefunden hat, wird eine Klassenfactory erstellt, die einen Zeiger auf die entsprechende Vorlage enthält. Wenn der Client **IClassFactory:: kreateinstance** aufruft, ruft die Klassenfactory die in der Vorlage definierte instanzizierungsfunktion auf.

Die folgende Abbildung zeigt die Abfolge von Methoden aufrufen.

![klassenfactoryvorlagen in einer dll](images/classfactory2.png)

Der Vorteil dieser Architektur besteht darin, dass Sie nur einige wenige Dinge definieren können, die für Ihre Komponente spezifisch sind, z. b. die instanzizierungsfunktion, ohne die gesamte Klassenfactory zu implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer DirectShow-Filter-dll](how-to-create-a-dll.md)
</dt> </dl>

 

 
