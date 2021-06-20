---
title: Erforderliche Schnittstellen (COM)
description: Erfahren Sie mehr über die ActiveX-Steuerelementcontainerschnittstellen, die von Steuerelementcontainern implementiert werden können oder müssen.
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55015ee5837754c073d2590144687131c285bb80
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407643"
---
# <a name="required-interfaces-com"></a>Erforderliche Schnittstellen (COM)

In der folgenden Tabelle sind die ActiveX-Steuerelementcontainerschnittstellen aufgeführt, und es wird angegeben, welche Schnittstellen optional sind und welche erforderlich sind und von Steuerelementcontainern implementiert werden müssen.



| Schnittstelle                                                                      | Erforderlich?      | Kommentare                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**Iadvisesink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | Nein<br/>  | Nur wenn der Container (a) Datenänderungsbenachrichtigungen (Steuerelemente mit [**IDataObject)**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)wünscht, (b) Änderungsbenachrichtigungen anzeigen (Steuerelemente, die nicht aktiv sind und [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) oder [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)haben) und (c) andere Benachrichtigungen von Steuerelementen, die als standardmäßig eingebettete Objekte agieren.<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Ja<br/> | Siehe Hinweis 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch für** Umgebungseigenschaften<br/>                                | Ja<br/> | Siehe Hinweis 2 und [Umgebungseigenschaften für Steuerelemente](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Steuern von Ereignissätzen<br/>                                                  | Ja<br/> | Siehe Hinweis 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | Nein<br/>  | [**ISimpleFrameSite und**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) Unterstützung für geschachtelte einfache Frames sind optional.<br/>                                                                                                                                                                                                                                                    |
| [Ipropertynotifysink](data-binding-through-ipropertynotifysink.md)<br/> | Nein<br/>  | Wird nur für Container benötigt, die (a) über eine eigene Benutzeroberfläche zur Bearbeitung von Eigenschaften verfügen, die aktualisiert werden müsste, wenn ein Steuerelement eine Eigenschaft selbst geändert hat oder (b) änderungen an angeforderten Eigenschaften und andere solche Datenbindungsfeatures steuern \[ [](/windows/desktop/Midl/requestedit) \] möchten.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Ja<br/> | Obligatorisch, wenn der Container duale Schnittstellen unterstützt. Siehe Hinweis 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | Nein<br/>  | Die Unterstützung wird dringend empfohlen.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) wird für das Dokument oder Formularobjekt implementiert (oder entsprechend analog), das die Containerstandorte enthält. Steuerelemente verwenden **IOleContainer,** um zu anderen Steuerelementen im selben Dokument oder Formular zu navigieren.
2.  Die Unterstützung für duale Schnittstellen ist nicht obligatorisch, wird jedoch dringend empfohlen. Das Schreiben von ActiveX-Steuerelementcontainern zur Nutzung von dualen Schnittstellen bietet eine bessere Leistung mit Steuerelementen, die Unterstützung für duale Schnittstellen bieten.

ActiveX-Steuerelementcontainer müssen OLE-Automatisierungsausnahmen unterstützen. Wenn ein Steuerelementcontainer duale Schnittstellen unterstützt, muss er Automatisierungsausnahmen über [IErrorInfo erfassen.](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

