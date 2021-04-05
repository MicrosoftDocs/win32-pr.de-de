---
title: Visuelle Darstellung
description: Ein Steuerelement unterstützt die Positionierung und Anzeige innerhalb des Containers mithilfe von Verbund Dokumenten Technologie und OLE-Drag & Drop-Technologie, die sowohl das Steuerelement als auch den zugehörigen Container umfasst.
ms.assetid: a7940560-360c-4c0d-9ac1-d051adb0b83e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9711dccbc7aa17f0b4a2ff228b2e2e4421e5083b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714418"
---
# <a name="visual-representation"></a>Visuelle Darstellung

Ein Steuerelement unterstützt die Positionierung und Anzeige innerhalb des Containers mithilfe von Verbund Dokumenten Technologie und OLE-Drag & Drop-Technologie, die sowohl das Steuerelement als auch den zugehörigen Container umfasst. Das Steuerelement muss sich selbst zeichnen können, während der Container die Position des Steuer Elements und seine Größe verwaltet.

Steuerelemente werden zu den grundlegenden Funktionen von OLE-Dokumenten hinzugefügt. Ein-Steuerelement ruft die [**IOleClientSite:: requestnewobjectlayout**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-requestnewobjectlayout) -Methode des Clients auf, um dem Container mitzuteilen, dass seine Größe geändert werden soll. Der Client ruft das [**IOleObject:: GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent) -Element des Steuer Elements auf, um die neue Größe zu erhalten, und ruft [**IOleInPlaceObject:: SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects) auf, um das Steuerelement auf seine neue Größe festzulegen.

Steuerelemente, die nur [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) unterstützen, unterstützen das Caching über [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2) nicht, da der Cache Unterstützung für [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)benötigt. Diese Steuerelemente sollten jedoch die Möglichkeit bieten, das Steuerelement durch [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) zu rendernden, damit der Client optional seinen eigenen Cache der Präsentationsdaten für das Steuerelement erstellen und verwalten kann.

Steuerelemente verwenden den HIMETRIC-Typ für Ihre Koordinaten. Für verschiedene Container können jedoch unterschiedliche Koordinatensysteme verwendet werden. Der Container möchte Koordinaten in seinem eigenen System empfangen, aber das Steuerelement weiß nicht unbedingt, welche Koordinaten sein Container verwendet. Für eine erfolgreiche Kommunikation benötigt das Steuerelement eine Möglichkeit zum Konvertieren von Werten in die Koordinaten des Containers. Der Container stellt ein Site Objekt mit der [**iolecontrolsite:: transformcoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) -Methode bereit. Das-Steuerelement ruft diese Methode zuerst auf der Client Site des Containers auf, um seine Koordinaten in die entsprechenden Koordinaten für den Container zu konvertieren. Anschließend können die konvertierten Koordinaten an den Container übergeben werden.

Steuerelemente können [**iolecontrolsite:: lockinplaceactive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive) im Site-Objekt des Containers abrufen, um zu verhindern, dass der Container versucht, das Steuerelement aus dem direkten aktiven Zustand herabzusetzen. Wenn Sie das Steuerelement auf diese Weise herabstufen, wird das Steuerelement deaktiviert, und das Fenster wird zerstört, sodass das Steuerelement das Fenster für eine bekannte Dauer beibehalten **muss, um seinen Zustand zu Gewähr** leisten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 




