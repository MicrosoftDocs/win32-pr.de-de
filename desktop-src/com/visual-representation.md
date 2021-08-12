---
title: Visuelle Darstellung
description: Ein Steuerelement unterstützt die Positionierung und Anzeige in seinem Container durch Verbunddokumenttechnologie und OLE-Drag & Drop-Technologie, die sowohl das Steuerelement als auch seinen Container umfasst.
ms.assetid: a7940560-360c-4c0d-9ac1-d051adb0b83e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1037b9f13d3122d19ec5ca429b2189426ac7ff69145e087828571c62aeb6f741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549429"
---
# <a name="visual-representation"></a>Visuelle Darstellung

Ein Steuerelement unterstützt die Positionierung und Anzeige in seinem Container durch Verbunddokumenttechnologie und OLE-Drag & Drop-Technologie, die sowohl das Steuerelement als auch seinen Container umfasst. Das Steuerelement muss sich selbst zeichnen können, während der Container die Position des Steuerelements und seine Größe verwaltet.

Steuerelemente werden den grundlegenden Funktionen hinzugefügt, die von OLE-Dokumenten bereitgestellt werden. Ein Steuerelement ruft die [**IOleClientSite::RequestNewObjectLayout-Methode**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-requestnewobjectlayout) seines Clients auf, um seinem Container mitzuteilen, dass seine Größe geändert werden soll. Der Client ruft [**IOleObject::GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent) des Steuerelements auf, um die neue Größe abzurufen, und ruft [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects) auf, um das Steuerelement auf seine neue Größe festzulegen.

Steuerelemente, die nur [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) unterstützen, unterstützen keine Zwischenspeicherung über [**IOleCache2,**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2) da der Cache Unterstützung für [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)erfordert. Diese Steuerelemente sollten dem Client jedoch die Möglichkeit bieten, das Steuerelement über [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) zu rendern, damit der Client optional einen eigenen Cache der Präsentationsdaten für das Steuerelement erstellen und verwalten kann.

Steuerelemente verwenden den HIMETRIC-Typ für seine Koordinaten. Unterschiedliche Container können jedoch unterschiedliche Koordinatensysteme verwenden. Der Container möchte Koordinaten in seinem eigenen System empfangen, aber das Steuerelement weiß nicht notwendigerweise, welche Koordinaten sein Container verwendet. Um erfolgreich zu kommunizieren, benötigt das Steuerelement eine Möglichkeit, Werte in die Koordinaten seines Containers zu konvertieren. Der Container stellt ein Standortobjekt mit der [**IOleControlSite::TransformCoords-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) bereit. Das -Steuerelement ruft diese Methode zuerst auf der Clientwebsite des Containers auf, um seine Koordinaten in die entsprechenden Koordinaten für den Container zu konvertieren. Anschließend können die konvertierten Koordinaten an den Container übergeben werden.

Steuerelemente können [**IOleControlSite::LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive) im Standortobjekt des Containers aufrufen, um zu verhindern, dass der Container versucht, das Steuerelement aus dem aktiven Zustand herauszustufen. Das Herabgestuften des Steuerelements auf diese Weise bewirkt, dass das Steuerelement deaktiviert und sein Fenster zerstört wird. Wenn das Steuerelement also sein Fenster für einen bekannten Zeitraum beibehalten muss, kann es **LockInPlaceActive** aufrufen, um seinen Zustand zu gewährleisten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 




