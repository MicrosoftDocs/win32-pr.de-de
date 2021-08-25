---
title: Optionale Methoden in Steuerelementschnittstellen
description: Optionale Methoden in Steuerelementschnittstellen
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92303b9e4e6a5edd295d0895a9121eee70ea05ae2a8967a9346ea26b153e8b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859290"
---
# <a name="optional-methods-in-control-interfaces"></a>Optionale Methoden in Steuerelementschnittstellen

Das Implementieren einer Schnittstelle bedeutet nicht notwendigerweise, alle Methoden dieser Schnittstelle zu implementieren, um mehr zu tun, als E \_ NOTIMPL oder S \_ OK nach Bedarf zurückzugeben. In der folgenden Tabelle sind die Methoden der Schnittstellen aufgeführt, die im Thema [What Support for an Interface Means](what-support-for-an-interface-means.md) aufgeführt sind, die ein Steuerelement auf diese Weise implementieren kann. Jede methode, die hier nicht aufgeführt ist, muss vollständig implementiert werden, wenn die -Schnittstelle unterstützt wird.



| IOleControl                                                                                                   | Kommentare                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Obligatorisch für Steuerelemente mit Mnemonics.<br/>                              |
| [**IOleControl::OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Obligatorisch für Steuerelemente, die Umgebungseigenschaften verwenden.<br/>                 |
| [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | Weitere Informationen finden Sie unter [Ereignissperren.](event-freezing.md)<br/>                            |
| IOleObject                                                                                                    |                                                                                |
| [**SetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Obligatorisch, wenn das Steuerelement nicht mit OLEMISC \_ CANTLINKINSIDE markiert ist<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Obligatorisch, wenn das Steuerelement nicht mit OLEMISC \_ CANTLINKINSIDE markiert ist<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Optional<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Optional<br/>                                                            |
| [**SetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Nur für DVASPECT-INHALT obligatorisch \_<br/>                                |
| [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Nur für DVASPECT-INHALT obligatorisch \_<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Optional<br/>                                                            |
| [**DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | Siehe Hinweis 1<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Optional<br/>                                                            |
| [**ReactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Optional<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**ContextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Optional<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Freeze**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Optional<br/>                                                            |
| [**Auftauen**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Optional<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Optional<br/>                                                            |
| IPersistStream, IPersistStreamInit, IPersistMemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | Siehe Hinweis 2<br/>                                                          |



 

1.  Ein Steuerelement mit Eigenschaftenseiten muss [**IOleObject::D oVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) für die Verben OLEIVERB \_ PROPERTIES und OLEIVERB \_ PRIMARY unterstützen. Ein Steuerelement, das aktiv sein kann, muss **DoVerb** für das OLEIVERB \_ INPLACEACTIVATE-Verb unterstützen. Ein Steuerelement, das benutzeroberflächenaktiv sein kann, muss auch **DoVerb** für das OLEIVERB \_ UIACTIVATE-Verb unterstützen.
2.  Wenn ein Steuerelement [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) unterstützt und einen genauen Wert zurückgeben kann, sollte es dies tun.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

 





