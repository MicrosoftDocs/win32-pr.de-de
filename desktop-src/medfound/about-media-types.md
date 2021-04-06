---
description: Informationen zu Medientypen
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: Informationen zu Medientypen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1ee75979c5c382e7e4ea458655efb83435a22d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961095"
---
# <a name="about-media-types-microsoft-media-foundation"></a>Informationen zu Medientypen (Microsoft Media Foundation)

Ein *Medientyp* beschreibt das Format eines Mediendaten Stroms. In Microsoft Media Foundation werden Medientypen durch die [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle dargestellt. Diese Schnittstelle erbt die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle. Die Details eines Medientyps werden als Attribute angegeben.

Um einen neuen Medientyp zu erstellen, rufen Sie die [**mfkreatemediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) -Funktion auf. Diese Funktion gibt einen Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle zurück. Der Medientyp hat anfänglich keine Attribute. Um die Details des Formats festzulegen, legen Sie die relevanten Attribute fest.

Eine Liste der Medientyp Attribute finden Sie unter [Medientyp Attribute](media-type-attributes.md).

## <a name="major-types-and-subtypes"></a>Haupttypen und Untertypen

Zwei wichtige Informationen zu jedem Medientyp sind der Haupttyp und der Untertyp.

-   Der *Haupttyp* ist eine GUID, die die Gesamtkategorie der Daten in einem Mediendaten Strom definiert. Zu den Haupttypen zählen Video und Audiodaten. Legen Sie zum Angeben des Haupt Datentyps das [MF \_ MT- \_ \_ Haupttyp](mf-mt-major-type-attribute.md) Attribut fest. Die [**IMF MediaType:: getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) -Methode gibt den Wert dieses Attributs zurück.
-   Der *Untertyp* definiert das Format weiter. Im Video Haupttyp gibt es z. b. Untertypen für RGB-24, RGB-32, im YUY2 usw. In Audiodaten sind PCM-Audiodaten, IEEE-Gleit Komma-Audiodaten und andere. Der Untertyp bietet mehr Informationen als der Haupttyp, aber er definiert nicht alles über das Format. Beispielsweise definieren Video Untertypen nicht die Bildgröße oder die Framerate. Um den Untertyp anzugeben, legen Sie das Attribut " [MF \_ MT \_ SubType](mf-mt-subtype-attribute.md) " fest.

Alle Medientypen sollten eine GUID des Haupt Typs und eine Untertyp-GUID aufweisen. Eine Liste der Haupttyp-und Untertyp-GUIDs finden Sie unter [Medientyp-GUIDs](media-type-guids.md).

## <a name="why-attributes"></a>Warum Attribute?

Attribute haben mehrere Vorteile gegenüber den Format Strukturen, die in früheren Technologien wie DirectShow und Windows Media Format SDK verwendet wurden.

-   Es ist einfacher, die Werte "nicht bekannt" oder "keine Sorgfalt" darzustellen. Wenn Sie z. b. eine Video Transformation schreiben, wissen Sie möglicherweise im voraus, welche RGB-und YUV-Formate die Transformation unterstützt, aber nicht die Abmessungen des Video Rahmens, bis Sie Sie aus der Videoquelle erhalten. Ebenso ist es möglicherweise nicht wichtig, dass bestimmte Details, wie z. b. die Video-primär-, Bei einer Format Struktur muss jeder Member mit *einem Wert aufgefüllt* werden. Folglich ist es üblich, dass NULL verwendet wird, um einen unbekannten oder Standardwert anzugeben. Diese Vorgehensweise kann zu Fehlern führen, wenn eine andere Komponente NULL als berechtigten Wert behandelt. Mit Attributen lassen Sie einfach die Attribute aus, die für Ihre Komponente unbekannt oder nicht relevant sind.

-   Wenn sich die Anforderungen im Laufe der Zeit geändert haben, wurden die Format Strukturen durch Hinzufügen zusätzlicher Daten am Ende der Struktur erweitert. **WAVEFORMATEXTENSIBLE** erweitert z. b. die **WaveFormatEx** -Struktur. Diese Vorgehensweise ist anfällig für Fehler, da Komponenten Struktur Zeiger auf andere Strukturtypen umwandeln müssen. Attribute können sicher erweitert werden.
-   Es wurden inkompatible Formatierungs Strukturen definiert. Beispielsweise definiert DirectShow die **videoinfoheader** -und **VIDEOINFOHEADER2** -Strukturen. Attribute werden unabhängig voneinander festgelegt, sodass dieses Problem nicht auftritt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 



