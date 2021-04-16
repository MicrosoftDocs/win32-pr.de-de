---
description: In diesem Thema wird der Unterschied zwischen vollständigen Medientypen und partiellen Medientypen beschrieben.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Vollständige und partielle Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530524"
---
# <a name="complete-and-partial-media-types"></a>Vollständige und partielle Medientypen

In diesem Thema wird der Unterschied zwischen vollständigen Medientypen und partiellen Medientypen beschrieben.

## <a name="complete-media-types"></a>Vervollständigen von Medientypen

Ein *Vollständiger* Medientyp ist eine, die das Format des Mediendaten Stroms vollständig definiert. Bei einem kompletten Medientyp kann eine Pipeline Komponente die dem Medientyp zugeordneten Datenstrom Daten ohne Mehrdeutigkeit analysieren.

Für nicht komprimierte Formate definieren die folgenden Themen die Attribute, die für einen kompletten Medientyp erforderlich sind:

-   Audiodatei: [nicht komprimierte audiomedientypen](uncompressed-audio-media-types.md)
-   Video: [unkomprimierte Video Medientypen](uncompressed-video-media-types.md)

Bei komprimierten (oder *codierten*) Streams wird die Definition eines gesamten Medientyps durch den Codec definiert. Wenn jedoch unkomprimierte Typattribute für den komprimierten Datenstrom bekannt sind, sollten diese Werte in den Medientyp für den komprimierten Datenstrom eingeschlossen werden. Wenn z. b. die Frame Größe bekannt ist, legen Sie das Attribut " [**MF \_ MT \_ Frame \_ size**](mf-mt-frame-size-attribute.md) " auf den Medientyp fest, obwohl technisch gesehen ein komprimierter Stream nicht über eine Frame Größe verfügt.

## <a name="partial-media-types"></a>Partielle Medientypen

Bei einem *partiellen* Medientyp fehlt mindestens eines der für einen vollständigen Medientyp erforderlichen Attribute. Beim Auflisten möglicher Medientypen kann eine Microsoft Media Foundation Komponente einen Wert nicht festlegen, um anzugeben, dass jeder beliebige Wert verarbeitet werden kann. Beispielsweise kann ein Videoprozessor das Attribut " [**MF \_ MT \_ Frame \_ Rate**](mf-mt-frame-rate-attribute.md) " nicht festlegen, um anzugeben, dass es eine beliebige Framerate verarbeiten kann, und führt ggf. eine Frameraten Konvertierung durch.

Wenn Sie einen partiellen Medientyp erstellen, sollten Sie immer noch so viele Informationen wie Sie wissen einschließen. Ein Medientyp darf jedoch keine unsicheren Informationen enthalten. Es ist besser, Informationen zu fehlen als falsch.

Ein partieller Medientyp sollte mindestens zwei Attribute enthalten: " [**MF \_ MT \_ Major \_ Type**](mf-mt-major-type-attribute.md) " und " [**MF \_ MT"- \_ Untertyp**](mf-mt-subtype-attribute.md).

In manchen Fällen müssen Media Foundation Komponenten umfassende Medientypen bereitstellen:

-   Medienquellen müssen komplette Ausgabetypen bereitstellen.
-   Decoders müssen komplette Ausgabetypen bereitstellen, nachdem der Eingabetyp festgelegt wurde. Bevor der Eingabetyp festgelegt wird, kann ein Decoder einen partiellen Ausgabetyp bereitstellen.
-   Encoder müssen komplette Eingabetypen bereitstellen, nachdem der Ausgabetyp festgelegt wurde. Bevor der Ausgabetyp festgelegt wird, kann ein Encoder einen partiellen Eingabetyp bereitstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 



