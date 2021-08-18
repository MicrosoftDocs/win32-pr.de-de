---
title: Verbunddokumentschnittstellen
description: Verbunddokumentschnittstellen
ms.assetid: 3192ee58-55fd-43cb-b7d5-7270e91b8131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e146bf26ef8d0c5c2fc189255389982a7e737a0556343cb095217c55ff8d712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410510"
---
# <a name="compound-document-interfaces"></a>Verbunddokumentschnittstellen

In den folgenden Tabellen sind die Schnittstellen aufgeführt, die von OLE-Containern, OLE-Servern und zusammengesetzten Dokumentobjekten implementiert werden. Die erforderlichen Schnittstellen müssen für die Komponenten implementiert werden, für die sie aufgeführt sind. Alle anderen Features sind optional. Wenn Sie jedoch ein bestimmtes Feature in Ihre Anwendung integrieren möchten, müssen Sie die Schnittstellen implementieren, die für dieses Feature in der folgenden Tabelle angezeigt werden. Alle anderen Schnittstellen sind nur erforderlich, wenn Sie ein bestimmtes Feature verwenden.

In der folgenden Tabelle sind die erforderlichen und optionalen Verhaltensweisen für OLE-Container und die Schnittstellen aufgeführt, die Sie jeweils implementieren müssen.



| Verhalten                               | Schnittstellen                                                                                                                                                              |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erforderliches Verhalten<br/>          | [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/> [**Iadvisesink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                                                       |
| Nachrichtenfilterung<br/>           | [**Imessagefilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                                                     |
| Verknüpfen<br/>                     | Keine<br/>                                                                                                                                                         |
| Verknüpfen mit eingebetteten Objekten<br/> | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**Ipersistfile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/> [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>             |
| In-Place-Aktivierung<br/>         | [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/> [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/> [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> |
| Drag &amp; Drop<br/>               | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**Idroptarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                               |



 

In der folgenden Tabelle sind die erforderlichen und optionalen Verhaltensweisen für OLE-Server und deren zusammengesetzte Dokumentobjekte sowie die Schnittstellen aufgeführt, die Sie für jede implementieren müssen. Die Tabelle unterscheidet OLE-Server und ihre Objekte, um zu verdeutlichen, welche Komponente welche Schnittstellen implementiert. In der Tabelle sind auch die unterschiedlichen Anforderungen von Objekten aufgeführt, die von Out-of-Process- und In-Process-Servern bereitgestellt werden.



| Komponente                        | OLE Server                                                                                                                                | Object (Out-of-Process)                                                                                                                         | Object (In-Process)                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Erforderliches Verhalten             | [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>                                                                                         | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> | [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)<br/> [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2)<br/> |
| Nachrichtenfilterung<br/>   | [**Imessagefilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                       |                                                                                                                                                 |                                                                                                                                                                                                                                             |
| Verknüpfen<br/>             | [**IOleItemContainer**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**Ipersistfile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                 |                                                                                                                                                 | [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)<br/> [**IExternalConnection**](/windows/win32/api/objidlbase/nn-objidlbase-iexternalconnection)<br/>                                                                                                                                       |
| In-Place-Aktivierung<br/> |                                                                                                                                           | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                 | [**IOleInPlaceObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                                                                                                             |
| Drag &amp; Drop<br/>       | [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**Idroptarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> |                                                                                                                                                 |                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbunddokumente](compound-documents.md)
</dt> </dl>

 

