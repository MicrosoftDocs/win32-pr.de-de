---
title: Schnittstellen (Steuerelemente und Eigenschaften Seiten)
description: Die folgenden Schnittstellen werden verwendet, um com-Standardobjekte und-Eigenschaften Seiten zu erstellen.
ms.assetid: f0d655b3-fa92-4553-ba21-617649a922a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e143ab1793eaf0335bbcf04093707bdc359e868e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341347"
---
# <a name="interfaces-controls-and-property-pages"></a>Schnittstellen (Steuerelemente und Eigenschaften Seiten)

Die folgenden Schnittstellen werden verwendet, um com-Standardobjekte und-Eigenschaften Seiten zu erstellen.



| Schnittstelle                                             | BESCHREIBUNG                                                                                                                                                                                                  |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)                                | Stellt einen Wrapper um ein Windows-Schriftart Objekt bereit.                                                                                                                                                             |
| [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)                        | Macht die Eigenschaften eines Schriftart Objekts über Automation verfügbar. Sie stellt eine Teilmenge der [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) -Methoden bereit.                                                                                           |
| [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)                    | Stellt die Funktionen für die Unterstützung von Tastatur-mmamonics, Ambient-Eigenschaften und Ereignissen in Steuerelement Objekten bereit.                                                                                                  |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)            | Stellt die Methoden bereit, mit denen ein Standort Objekt jedes eingebettete Steuerelement in einem Container verwalten kann.                                                                                                           |
| [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)  | Ruft die Informationen auf den Eigenschaften Seiten ab, die von einem-Objekt angeboten werden.                                                                                                                                        |
| [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)                          | Verwaltet ein Bild Objekt und seine Eigenschaften. Bildobjekte stellen eine sprachneutrale Abstraktion für Bitmaps, Symbole und Metadateien bereit.                                                                       |
| [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)                  | Macht die Eigenschaften des Bildobjekts über Automation verfügbar. Es stellt eine Teilmenge der Funktionen bereit, die über [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) -Methoden verfügbar sind.                                                |
| [**IPointerInactive**](/windows/desktop/api/OCIdl/nn-ocidl-ipointerinactive)          | Ermöglicht, dass ein Objekt in den meisten Fällen inaktiv bleibt, aber trotzdem an der Interaktion mit der Maus beteiligt ist, einschließlich Drag & Drop.                                                                         |
| [**IPrint**](/windows/desktop/api/DocObj/nn-docobj-iprint)                              | Ermöglicht Verbund Dokumenten in allgemeinen und aktiven Dokumenten insbesondere, um programmgesteuerte Druckunterstützung zu unterstützen.                                                                                                   |
| [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)    | Wird von einem Sink-Objekt implementiert, um Benachrichtigungen über Eigenschafts Änderungen von einem Objekt zu empfangen, das [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) als ausgehende Schnittstelle unterstützt.                       |
| [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)                | Stellt die Hauptfunktionen eines Eigenschaften Seiten Objekts bereit, das eine bestimmte Seite in einem Eigenschaften Blatt verwaltet.                                                                                                 |
| [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)              | Eine Erweiterung von [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) zur Unterstützung der anfänglichen Auswahl einer Eigenschaft auf einer Seite.                                                                                                 |
| [**Ipropertypagesite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite)        | Stellt die wichtigsten Funktionen für ein Eigenschaften Seiten-Website Objekt bereit.                                                                                                                                                  |
| [**Iquickaktivierung**](/windows/desktop/api/OCIdl/nn-ocidl-iquickactivate)              | Ermöglicht es Steuerelementen und Containern, Leistungsengpässe beim Laden von Steuerelementen zu vermeiden. Es kombiniert die Lade Zeit-oder Initialisierungs Zeit zwischen dem Steuerelement und seinem Container in einem einzigen Aufruf. |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)          | Stellt einfache Frame Steuerelemente bereit, die als einfache Container für andere in der Form eingefügte Steuerelemente fungieren                                                                                                                      |
| [**Ispecifypropertypage**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages) | Gibt an, dass ein Objekteigenschaften Seiten unterstützt.                                                                                                                                                            |



 

 

 
