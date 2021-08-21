---
title: Erforderliche Schnittstellen (COM)
description: Erfahren Sie mehr über die ActiveX Control Container-Schnittstellen, die von Steuerelementcontainern implementiert werden können oder müssen.
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf19cb8d0c72b365f6a8faa263fc76ddede1e5231fc34a9090c064f54d75b7f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309662"
---
# <a name="required-interfaces-com"></a>Erforderliche Schnittstellen (COM)

Die folgende Tabelle enthält die ActiveX Control Container-Schnittstellen und gibt an, welche Schnittstellen optional sind, welche obligatorisch sind und von Steuerelementcontainern implementiert werden müssen.



| Schnittstelle                                                                      | Erforderlich?      | Kommentare                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**Iadvisesink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | Nein<br/>  | Nur wenn der Container (a) Datenänderungsbenachrichtigungen (Steuerelemente mit [**IDataObject),**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)(b) Ansichtsänderungsbenachrichtigungen (Steuerelemente, die nicht aktiv sind und [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) oder [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)aufweisen) und (c) andere Benachrichtigungen von Steuerelementen wünscht, die als eingebettete Standardobjekte fungieren.<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Ja<br/> | Siehe Hinweis 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch** für Umgebungseigenschaften<br/>                                | Ja<br/> | Weitere Informationen finden Sie unter Hinweis 2 und [Umgebungseigenschaften für Steuerelemente.](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Steuern von Ereignissätzen<br/>                                                  | Ja<br/> | Siehe Hinweis 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | Nein<br/>  | [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) und Unterstützung für geschachtelte einfache Frames sind optional.<br/>                                                                                                                                                                                                                                                    |
| [Ipropertynotifysink](data-binding-through-ipropertynotifysink.md)<br/> | Nein<br/>  | Nur für Container erforderlich, die (a) über eine eigene Benutzeroberfläche zum Bearbeiten von Eigenschaften verfügen, die eine Aktualisierung erfordern würde, wenn ein Steuerelement eine Eigenschaft selbst geändert hat oder (b) \[ [](/windows/desktop/Midl/requestedit) \] requestedit-Eigenschaftsänderungen und andere solche Datenbindungsfunktionen steuern möchte.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Ja<br/> | Obligatorisch, wenn der Container duale Schnittstellen unterstützt. Siehe Hinweis 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | Nein<br/>  | Unterstützung wird dringend empfohlen.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) wird für das Dokument- oder Formularobjekt (oder das entsprechende analoge Objekt) implementiert, das die Containerstandorte enthält. Steuerelemente verwenden **IOleContainer,** um zu anderen Steuerelementen im gleichen Dokument oder Formular zu navigieren.
2.  Die Unterstützung für duale Schnittstellen ist nicht obligatorisch, wird jedoch dringend empfohlen. Das Schreiben ActiveX Steuercontainer, um duale Schnittstellen zu nutzen, bietet eine bessere Leistung mit Steuerelementen, die Dual Interface-Unterstützung bieten.

ActiveX-Steuerelementcontainer müssen OLE Automation-Ausnahmen unterstützen. Wenn ein Steuerelementcontainer duale Schnittstellen unterstützt, muss er Automatisierungsausnahmen über [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)erfassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

