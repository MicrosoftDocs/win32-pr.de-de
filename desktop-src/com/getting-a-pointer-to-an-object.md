---
title: Einen Zeiger auf ein Objekt zu erhalten
description: Einen Zeiger auf ein Objekt zu erhalten
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0476d36390e7077e7fdd75eef8d95e8173683891
ms.sourcegitcommit: 307b14e9847ced354a52a1ac12d7f659722d99bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2020
ms.locfileid: "106338046"
---
# <a name="getting-a-pointer-to-an-object"></a>Einen Zeiger auf ein Objekt zu erhalten

Da com nicht über ein Strict-Klassenmodell verfügt, gibt es vier Möglichkeiten, wie ein Client instanziieren oder einen Zeiger auf eine Schnittstelle für ein Objekt erhalten kann:

-   Ruft eine com-Bibliotheksfunktion auf, die ein Objekt eines vordefinierten Typs erstellt. Das heißt, die Funktion gibt einen Zeiger auf eine bestimmte Schnittstelle für eine bestimmte Objektklasse zurück.
-   Rufen Sie eine com-Bibliotheksfunktion auf, die ein Objekt auf der Grundlage eines Klassen Bezeichners (CLSID) erstellen kann, und der jeden angeforderten angeforderte Typ von Schnittstellen Zeiger zurückgibt.
-   Ruft eine Methode einer Schnittstelle auf, die ein anderes Objekt erstellt (oder eine Verbindung mit einer vorhandenen herstellt) und einen Schnittstellen Zeiger für dieses separate Objekt zurückgibt.
-   Implementieren Sie ein Objekt mit einer Schnittstelle, über die andere Objekte ihren Schnittstellen Zeiger direkt an den Client übergeben.

Weitere Informationen zum Abrufen von Zeigern auf andere Schnittstellen eines Objekts, nachdem Sie das erste-Objekt erhalten haben, finden Sie unter [QueryInterface: Navigation in einem Objekt](queryinterface--navigating-in-an-object.md).

## <a name="creating-an-object-of-a-predetermined-type"></a>Erstellen eines Objekts eines vordefinierten Typs

Es gibt zahlreiche com-Funktionen, wie z. b. [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc), die Zeiger auf bestimmte Schnittstellen Implementierungen zurückgeben. (**CoGetMalloc** Ruft einen Zeiger auf die Standard-com-Speicherzuweisung ab.) Die meisten dieser Funktionen sind Hilfsfunktionen, und die meisten dieser Funktionen werden in den Referenz Abschnitten dieser Dokumentation unter dem jeweiligen Bereich beschrieben, mit dem Sie verknüpft sind, wie z. b. Speicher oder Datenübertragung.

## <a name="creating-an-object-based-on-a-clsid"></a>Erstellen eines Objekts auf der Grundlage einer CLSID

Es gibt mehrere Funktionen, die bei einer CLSID von einem Client aufgerufen werden können, um eine Objektinstanz zu erstellen und einen Zeiger darauf zu erhalten. Alle diese Funktionen basieren auf der Funktion [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), die ein Klassenobjekt erstellt und einen Zeiger auf eine Schnittstelle bereitstellt, die Ihnen ermöglicht, Instanzen dieser Klasse zu erstellen. Es müssen zwar Informationen vorhanden sein, auf denen sich der Server befindet, aber es ist nicht erforderlich, dass diese Informationen im Client enthalten sind. Der Client muss nur die CLSID und nie den absoluten Pfad des Server Codes kennen. Weitere Informationen finden Sie unter [Erstellen eines Objekts mit einem Klassenobjekt](creating-an-object-through-a-class-object.md).

## <a name="returning-a-pointer-to-a-separate-object"></a>Zurückgeben eines Zeigers auf ein separates Objekt

Zu den zahlreichen Schnittstellen Methoden, die einen Zeiger auf ein separates Objekt zurückgeben, handelt es sich um mehrere, die erstellen und einen Zeiger auf ein *Enumeratorobjekt* zurückgeben, mit dem Sie bestimmen können, wie viele Elemente eines bestimmten Typs von einem Objekt verwaltet werden. COM definiert Schnittstellen zum Auflisten einer Vielzahl von Elementen, z. b. Zeichen folgen, wichtige Strukturen, Moniker und [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstellen Zeiger. Die typische Methode zum Erstellen einer Enumeratorinstanz und zum Abrufen eines Zeigers auf die-Schnittstelle besteht darin, eine Methode von einer anderen Schnittstelle aus aufzurufen. Die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle definiert z. b. zwei Methoden, [**enumdrat**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) und [**enumformatusw**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)., die Zeiger auf Schnittstellen für zwei unterschiedliche enumerationsobjekte zurückgeben. Es gibt viele weitere Beispiele in com von Methoden, die Zeiger auf Objekte zurückgeben, z. b. die OLE-Verbund Dokument Schnittstelle [**IOleObject:: GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite), die bei Aufruf für das eingebettete oder verknüpfte Objekt einen Zeiger auf die Implementierung von [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)des Container Objekts zurückgibt.

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a>Implementieren eines Objekts, über das ein Schnittstellen Zeiger direkt an den Client übergeben wird

Wenn zwei-Objekte, z. b. ein OLE-Verbund Dokument Container und-Server, eine bidirektionale Kommunikation benötigen, wird jedes Objekt implementiert, das eine Schnittstellen Methode enthält, über die ein Schnittstellen Zeiger an das andere Objekt übergeben werden kann. Das implementierende Objekt, das auch der Client des erstellten Objekts ist, kann dann die-Methode aufzurufen und den Zeiger abrufen, der weitergegeben wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und-Server](com-clients-and-servers.md)
</dt> <dt>

[Zuständigkeiten von com-Servern](com-server-responsibilities.md)
</dt> </dl>

 

 




