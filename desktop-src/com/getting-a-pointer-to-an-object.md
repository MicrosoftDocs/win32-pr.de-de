---
title: Abrufen eines Zeigers auf ein Objekt
description: Abrufen eines Zeigers auf ein Objekt
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc588518d5c3da884755d7db122738ca2fca257d76a1f8219867da357ef8444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736699"
---
# <a name="getting-a-pointer-to-an-object"></a>Abrufen eines Zeigers auf ein Objekt

Da COM über kein striktes Klassenmodell verfügt, gibt es vier Möglichkeiten, wie ein Client einen Zeiger auf eine Schnittstelle für ein Objekt instanziieren oder abrufen kann:

-   Rufen Sie eine COM-Bibliotheksfunktion auf, die ein Objekt eines vordefinierten Typs erstellt. Das heißt, die Funktion gibt einen Zeiger auf nur eine bestimmte Schnittstelle für eine bestimmte Objektklasse zurück.
-   Rufen Sie eine COM-Bibliotheksfunktion auf, die ein Objekt basierend auf einem Klassenbezeichner (CLSID) erstellen kann und jeden angeforderten Schnittstellenzeigertyp zurückgibt.
-   Rufen Sie eine Methode einer Schnittstelle auf, die ein anderes Objekt erstellt (oder eine Verbindung mit einem vorhandenen objekt herstellt) und einen Schnittstellenzeiger für dieses separate Objekt zurückgibt.
-   Implementieren Sie ein Objekt mit einer Schnittstelle, über die andere Objekte ihren Schnittstellenzeiger direkt an den Client übergeben.

Informationen zum Abrufen von Zeigern auf andere Schnittstellen für ein Objekt, nachdem Sie über die erste verfügen, finden Sie unter [QueryInterface: Navigation in einem Objekt.](queryinterface--navigating-in-an-object.md)

## <a name="creating-an-object-of-a-predetermined-type"></a>Erstellen eines Objekts eines vordefinierten Typs

Es gibt zahlreiche COM-Funktionen wie [**CoGetMalloc,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc)die Zeiger auf bestimmte Schnittstellenimplementierungen zurückgeben. (**CoGetMalloc** ruft einen Zeiger auf die STANDARDMÄßIGE COM-Speicherbezuweisung ab.) Die meisten dieser Funktionen sind Hilfsfunktionen, und die meisten dieser Funktionen werden in den Referenzabschnitten dieser Dokumentation unter dem spezifischen Bereich beschrieben, mit dem sie verknüpft sind, z. B. Speicherung oder Datenübertragung.

## <a name="creating-an-object-based-on-a-clsid"></a>Erstellen eines Objekts basierend auf einer CLSID

Es gibt mehrere Funktionen, die ein Client bei einer CLSID aufrufen kann, um eine Objektinstanz zu erstellen und einen Zeiger darauf abzurufen. Alle diese Funktionen basieren auf der [**CoGetClassObject-Funktion,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)die ein Klassenobjekt erstellt und einen Zeiger auf eine Schnittstelle angibt, mit der Sie Instanzen dieser Klasse erstellen können. Es müssen zwar Informationen darüber vorhanden sein, auf welchem System sich der Server befindet, aber es ist nicht erforderlich, dass diese Informationen im Client enthalten sind. Der Client muss nur die CLSID und nie den absoluten Pfad des Servercodes kennen. Weitere Informationen finden Sie unter [Erstellen eines Objekts über ein Klassenobjekt.](creating-an-object-through-a-class-object.md)

## <a name="returning-a-pointer-to-a-separate-object"></a>Zurückgeben eines Zeigers auf ein separates Objekt

Unter den vielen Schnittstellenmethoden, die einen Zeiger auf ein separates Objekt zurückgeben, gibt es mehrere, die einen Zeiger auf ein *Enumeratorobjekt* erstellen und zurückgeben, wodurch Sie bestimmen können, wie viele Elemente eines bestimmten Typs ein Objekt beibehält. COM definiert Schnittstellen zum Aufzählen einer Vielzahl von Elementen, z. B. [**Zeichenfolgen,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) wichtige Strukturen, Moniker und IUnknown-Schnittstellenzeiger. Die typische Möglichkeit, eine Enumeratorinstanz zu erstellen und einen Zeiger auf ihre Schnittstelle abzurufen, besteht darin, eine Methode von einer anderen Schnittstelle aufzurufen. Die [**IDataObject-Schnittstelle**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) definiert beispielsweise zwei Methoden, [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) und [**EnumFormatEtc,**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)die Zeiger auf Schnittstellen auf zwei verschiedenen Enumerationsobjekten zurückgeben. Es gibt viele weitere Beispiele in COM von Methoden, die Zeiger auf -Objekte zurückgeben, z. B. die OLE-Verbunddokumentschnittstelle [**IOleObject::GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite), die beim Aufruf für das eingebettete oder verknüpfte Objekt einen Zeiger auf die Implementierung des Containerobjekts von [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)zurückgibt.

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a>Implementieren eines Objekts, über das ein Schnittstellenzeiger direkt an den Client übergeben werden soll

Wenn zwei Objekte, z. B. ein OLE-Verbunddokumentcontainer und ein Server, bidirektionale Kommunikation benötigen, implementiert jedes ein Objekt, das eine Schnittstellenmethode enthält, über die ein Schnittstellenzeiger an das andere Objekt übergeben werden kann. Das implementierende Objekt, das auch der Client des erstellten Objekts ist, kann dann die -Methode aufrufen und den übergebenen Zeiger abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM-Clients und -Server](com-clients-and-servers.md)
</dt> <dt>

[ZUSTÄNDIGKEITEN DES COM-Servers](com-server-responsibilities.md)
</dt> </dl>

 

 




