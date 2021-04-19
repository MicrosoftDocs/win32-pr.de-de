---
description: DirectX-Medienobjekte
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: DirectX-Medienobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106367267"
---
# <a name="directx-media-objects"></a>DirectX-Medienobjekte

> [!Note]  
> DMOS wurden durch [Media Foundation Transformationen](/windows/desktop/medfound/media-foundation-transforms) (MFTs) abgelöst. Die DMO-Schnittstellen werden weiterhin unterstützt. Wenn Sie jedoch einen benutzerdefinierten Codec oder ein Plug-in für die Audio-/Videoverarbeitung schreiben, sollten Sie es als MFT implementieren.

 

Bei DirectX Media Objects (DMOs) handelt es sich um COM-basierte datenstreamingkomponenten. In gewisser Hinsicht ähneln DMOS Microsoft DirectShow-filtern. Wie DirectShow-Filter übernehmen DMOS Eingabedaten und verwenden Sie, um Ausgabedaten zu erstellen. Die Anwendungs Programmierschnittstellen (Application Programming Interfaces, APIs) für DMOS sind jedoch viel einfacher als die entsprechenden APIs für DirectShow. Demzufolge sind DMOS einfacher zu erstellen, zu testen und zu verwenden. DMOS können in vielen Szenarien verwendet werden:

-   Anwendungen, die auf DirectShow basieren, können DMOS über einen DirectShow-Filter verwenden, der als [DMO-Wrapper](dmo-wrapper-filter.md) Filter bezeichnet wird. Der Unterschied zwischen Filtern und DMOS ist für die Anwendung transparent. Die Anwendung ruft die DMO-APIs nicht direkt auf.
-   Anwendungen, die auf Microsoft DirectSound basieren, können Audioeffekt-DMOS verwenden. Die Anwendung wird erneut von den DMO-APIs auf niedriger Ebene durch die DirectSound-APIs auf höherer Ebene geschützt.
-   Anwendungen können DMOS direkt verwenden.

Wenn Sie also ein DMO schreiben, erstellen Sie eine-Komponente, die in einer Vielzahl von Anwendungen verwendet werden kann. Diese Dokumentation enthält die folgenden Abschnitte:

-   [Informationen zu DMOS](about-dmos.md)
-   [Verwenden von dmos](using-dmos.md)
-   [Schreiben eines DMO](writing-a-dmo.md)
-   [Medien Parameter](media-parameters.md)
-   [DMO-Referenz](dmo-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
