---
description: Medienquellen-Objektmodell
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Medienquellen-Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351529"
---
# <a name="media-source-object-model"></a>Medienquellen-Objektmodell

In diesem Thema wird das Objektmodell für Medienquellen in Microsoft Media Foundation beschrieben. Eine Medienquelle muss zwei Objekte implementieren:

-   Ein Präsentations Deskriptor, der den Inhalt der Quelle beschreibt, einschließlich der Anzahl der Streams und des Formats der einzelnen Datenströme. Weitere Informationen zu Präsentations Deskriptoren finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).
-   Ein oder mehrere Mediendaten Ströme, die die Quelldaten generieren.

Die Quelle erstellt die Streams erst, wenn die Wiedergabe gestartet wird.

## <a name="media-source-interfaces"></a>Medienquellen Schnittstellen

Eine Medienquelle muss die folgenden Schnittstellen über **QueryInterface** verfügbar machen.



| Schnittstelle                                                | BESCHREIBUNG                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Für alle Medienquellen erforderlich.                                                                                 |
| [**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Für alle Medienquellen erforderlich. Die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle erbt diese Schnittstelle. |



 

Optional kann eine Medienquelle die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle implementieren und eine der folgenden Schnittstellen als Dienste implementieren:



| Dienst Schnittstelle                                  | BESCHREIBUNG                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | Steuert die Wiedergabe Rate.                                       |
| [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | Meldet den Bereich von Wiedergabe Raten, die unterstützt werden.           |
| [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | Ermöglicht es dem Quality Manager, die Audioqualität oder Videoqualität anzupassen. |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | Stellt Metadaten bereit.                                                |



 

Wenn die Medienquelle bei anderen raten als normaler Geschwindigkeit (1,0) wiedergegeben werden kann, sollte Sie den Raten Steuerungs Dienst ("[**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) " und " [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)") verfügbar machen. Andernfalls wird davon ausgegangen, dass die Quelle nur die Wiedergabe mit normaler Geschwindigkeit unterstützt. Weitere Informationen finden Sie unter [Implementieren der Raten Kontrolle](implementing-rate-control.md).

Weitere Informationen zu Dienst Schnittstellen und [**immagetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)finden Sie unter [Dienst Schnittstellen](service-interfaces.md).

## <a name="media-stream-interfaces"></a>Medienstrom Schnittstellen

Mediendaten Ströme müssen die folgenden Schnittstellen implementieren.



| Schnittstelle                                                | BESCHREIBUNG                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMF Media Stream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | Erforderlich für alle Mediendaten Ströme.                                                                                 |
| [**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Erforderlich für alle Mediendaten Ströme. Die [**IMF Media Stream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Schnittstelle erbt diese Schnittstelle. |



 

Zurzeit sind keine Dienst Schnittstellen für Mediendaten Ströme definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienquellen](media-sources.md)
</dt> </dl>

 

 



