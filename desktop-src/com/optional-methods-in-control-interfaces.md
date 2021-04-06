---
title: Optionale Methoden in Steuerungs Schnittstellen
description: Optionale Methoden in Steuerungs Schnittstellen
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1409b1c8d22f85a48829c07155e03379fc79103c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947496"
---
# <a name="optional-methods-in-control-interfaces"></a>Optionale Methoden in Steuerungs Schnittstellen

Das Implementieren einer Schnittstelle bedeutet nicht notwendigerweise, dass alle Methoden dieser Schnittstelle implementiert werden müssen, um etwas mehr zu tun, als "E \_ notimpl" oder "S \_ OK". In der folgenden Tabelle sind die Methoden der Schnittstellen aufgeführt, die im Thema [Unterstützung für eine Schnittstelle](what-support-for-an-interface-means.md) aufgeführt sind, das von einem Steuerelement auf diese Weise implementiert werden kann. Jede hier nicht aufgelistete Methode muss vollständig implementiert werden, wenn die Schnittstelle unterstützt wird.



| IOleControl                                                                                                   | Kommentare                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **onmnetmonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obligatorisch für Steuerelemente mit mnetmonics.<br/>                              |
| [**IOleControl:: OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obligatorisch für Steuerelemente, die Umgebungs Eigenschaften verwenden.<br/>                 |
| [**IOleControl:: frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Siehe [Ereignis Einfrieren](event-freezing.md)<br/>                            |
| IOleObject                                                                                                    |                                                                                |
| [**Setmoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obligatorisch, wenn das Steuerelement nicht mit OLEMISC \_ cantlinkinside markiert ist.<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obligatorisch, wenn das Steuerelement nicht mit OLEMISC \_ cantlinkinside markiert ist.<br/> |
| [**Initfromdata**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Optional<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Optional<br/>                                                            |
| [**Abtextent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Nur für DVASPECT- \_ Inhalt obligatorisch<br/>                                |
| [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Nur für DVASPECT- \_ Inhalt obligatorisch<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Optional<br/>                                                            |
| [**DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Siehe Hinweis 1<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Optional<br/>                                                            |
| [**Reactivateandundo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Optional<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Optional<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Einfrieren**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Optional<br/>                                                            |
| [**Fixierung aufheben**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Optional<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Optional<br/>                                                            |
| IPersistStream, IPersistStreamInit, ipersistmemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Siehe Hinweis 2<br/>                                                          |



 

1.  Ein Steuerelement mit Eigenschaften Seiten muss [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) für die oleiverb \_ -Eigenschaften und primäre oleiverb- \_ Verben unterstützen. Ein Steuerelement, das aktiv sein kann, muss **DoVerb** für das oleiverb \_ inplaceaktivierungs-Verb unterstützen. Ein Steuerelement, das UI-aktiv sein kann, muss auch **DoVerb** für das oleiverb- \_ uiaktivierungs-Verb unterstützen.
2.  Wenn ein Steuerelement [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) unterstützt und einen exakten Wert zurückgeben kann, sollten Sie dies tun.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

 





