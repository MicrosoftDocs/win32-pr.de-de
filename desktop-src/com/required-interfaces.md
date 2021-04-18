---
title: Erforderliche Schnittstellen (com)
description: Erforderliche Schnittstellen
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df483f8c8aa5eb5ecb6799b834fccab42f42ca1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340957"
---
# <a name="required-interfaces-com"></a>Erforderliche Schnittstellen (com)

In der folgenden Tabelle sind die ActiveX-Steuerelement Container-Schnittstellen aufgeführt, und es wird angegeben, welche Schnittstellen optional sind und welche obligatorisch sind und von Steuerelement Containern implementiert werden müssen.



| Schnittstelle                                                                      | Erforderlich?      | Kommentare                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | Nein<br/>  | Nur, wenn der Container (a) Daten Änderungs Benachrichtigungen (Steuerelemente mit [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)) wünscht, (b) Änderungs Benachrichtigungen anzeigen (Steuerelemente, die nicht aktiv sind und [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) oder [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)), und (c) andere Benachrichtigungen von Steuerelementen, die als eingebettete Standardobjekte fungieren.<br/> |
| [**Ioleingeplacesite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Ja<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Ja<br/> | Siehe Hinweis 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch** für Ambient-Eigenschaften<br/>                                | Ja<br/> | Siehe Hinweis 2 und [Ambient-Eigenschaften für Steuerelemente](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Steuern von Ereignis Sätzen<br/>                                                  | Ja<br/> | Siehe Hinweis 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | Nein<br/>  | [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) und Unterstützung für geduckte einfache Frames ist optional.<br/>                                                                                                                                                                                                                                                    |
| [IPropertyNotifySink](data-binding-through-ipropertynotifysink.md)<br/> | Nein<br/>  | Nur erforderlich für Container, die (a) über eine eigene Benutzeroberfläche zum Bearbeiten von Eigenschaften verfügen, die aktualisiert werden muss, wenn ein Steuerelement eine Eigenschaft selbst geändert hat oder (b) die Änderungen an \[ [**requestedit**](/windows/desktop/Midl/requestedit) \] -Eigenschaften und andere Daten Bindungs Features steuern möchten.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Ja<br/> | Obligatorisch, wenn der Container duale Schnittstellen unterstützt. Siehe Hinweis 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | Nein<br/>  | Der Support wird dringend empfohlen.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) wird auf dem Dokument-oder Formular Objekt (oder dem entsprechenden analog) implementiert, das die Container Websites enthält. Steuerelemente verwenden **IOleContainer** , um zu anderen Steuerelementen im gleichen Dokument oder Formular zu navigieren.
2.  Die Unterstützung für duale Schnittstellen ist nicht obligatorisch, wird jedoch dringend empfohlen. Wenn Sie ActiveX-Steuerelement Container schreiben, um duale Schnittstellen zu nutzen, wird eine bessere Leistung mit Steuerelementen erzielt, die Dual Schnittstellen Unterstützung bieten

ActiveX-Steuerelement Container müssen OLE-Automatisierungs Ausnahmen unterstützen. Wenn ein Steuerelement Container duale Schnittstellen unterstützt, muss er Automatisierungs Ausnahmen über [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)erfassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

