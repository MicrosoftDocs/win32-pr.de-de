---
description: Erfahren Sie mehr über Medientypen in Microsoft Media Foundation. Ein Medientyp beschreibt das Format eines Medienstreams.
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: Informationen zu Medientypen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3abce5d86b931a472dc07e1b6daf244f1456cfd3220f85c2b0e311f243a122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975079"
---
# <a name="about-media-types-microsoft-media-foundation"></a>Informationen zu Medientypen (Microsoft Media Foundation)

Ein *Medientyp* beschreibt das Format eines Medienstreams. In Microsoft Media Foundation werden Medientypen durch die [**INTERFACESMediaType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) dargestellt. Diese Schnittstelle erbt die [**INTERFACESAttributes-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Die Details eines Medientyps werden als Attribute angegeben.

Um einen neuen Medientyp zu erstellen, rufen Sie die [**MFCreateMediaType-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) auf. Diese Funktion gibt einen Zeiger auf die [**INTERFACESMediaType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) zurück. Der Medientyp weist anfänglich keine Attribute auf. Legen Sie die relevanten Attribute fest, um die Details des Formats festzulegen.

Eine Liste der Medientypattribute finden Sie unter [Medientypattribute.](media-type-attributes.md)

## <a name="major-types-and-subtypes"></a>Haupttypen und Untertypen

Zwei wichtige Informationen für jeden Medientyp sind der Haupttyp und der Untertyp.

-   Der *Haupttyp* ist eine GUID, die die Gesamtkategorie der Daten in einem Medienstream definiert. Zu den Haupttypen gehören Video und Audio. Um den Haupttyp anzugeben, legen Sie das [MF \_ MT MAJOR \_ \_ TYPE-Attribut](mf-mt-major-type-attribute.md) fest. Die [**ATTRIBUTESMediaType::GetMajorType-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) gibt den Wert dieses Attributs zurück.
-   Der *Untertyp* definiert das Format weiter. Beispielsweise gibt es innerhalb des Haupttyps des Videos Untertypen für RGB-24, RGB-32, YUY2 usw. In audio gibt es PCM-Audio, IEEE-Gleitkommaaudio und andere. Der Untertyp stellt mehr Informationen als der Haupttyp bereit, definiert aber nicht alles über das Format. Videountertypen definieren beispielsweise nicht die Bildgröße oder die Bildfrequenz. Um den Untertyp anzugeben, legen Sie das [MF \_ MT \_ SUBTYPE-Attribut](mf-mt-subtype-attribute.md) fest.

Alle Medientypen sollten eine Haupttyp-GUID und eine Untertyp-GUID aufweisen. Eine Liste der Haupttyp- und Untertyp-GUIDs finden Sie unter [Medientyp-GUIDs.](media-type-guids.md)

## <a name="why-attributes"></a>Warum Attribute?

Attribute haben gegenüber den Formatstrukturen, die in früheren Technologien wie DirectShow und dem Windows Media Format SDK verwendet wurden, mehrere Vorteile.

-   Es ist einfacher, "don't know"- oder "don't care"-Werte darzustellen. Wenn Sie z. B. eine Videotransformation schreiben, wissen Sie möglicherweise im Voraus, welche RGB- und YUV-Formate die Transformation unterstützt, aber nicht die Abmessungen des Videoframes, bis Sie sie aus der Videoquelle erhalten. Auf ähnliche Weise sind ihnen möglicherweise bestimmte Details, z. B. die primären Videodateien, nicht wichtig. Bei einer Formatstruktur muss jeder Member mit *einem* Wert gefüllt werden. Daher ist es üblich, 0 (null) zu verwenden, um einen unbekannten oder Standardwert anzugeben. Diese Vorgehensweise kann Fehler verursachen, wenn eine andere Komponente 0 (null) als legitimen Wert behandelt. Bei Attributen lassen Sie einfach die Attribute aus, die für Ihre Komponente unbekannt oder nicht relevant sind.

-   Da sich die Anforderungen im Laufe der Zeit geändert haben, wurden Formatstrukturen erweitert, indem am Ende der Struktur zusätzliche Daten hinzugefügt wurden. Beispielsweise erweitert **WAVEFORMATEXTENSIBLE** die **WAVEFORMATEX-Struktur.** Diese Vorgehensweise ist fehleranfällig, da Komponenten Strukturzeiger auf andere Strukturtypen umformen müssen. Attribute können sicher erweitert werden.
-   Gegenseitig inkompatible Formatstrukturen wurden definiert. DirectShow definiert beispielsweise die Strukturen **VIDEOINFOHEADER** und **VIDEOINFOHEADER2.** Attribute werden unabhängig voneinander festgelegt, sodass dieses Problem nicht auftritt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 



