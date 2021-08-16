---
description: DirectX-Medienobjekte
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: DirectX-Medienobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ef7dc17ab595748d9ccbfa16e33e7b4b8057d161c7f1e5d9f589e6768ec35f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821195"
---
# <a name="directx-media-objects"></a>DirectX-Medienobjekte

> [!Note]  
> DMOs wurden durch Media Foundation [Transforms](/windows/desktop/medfound/media-foundation-transforms) (MFTs) ersetzt. Die DMO Schnittstellen werden weiterhin unterstützt. Wenn Sie jedoch einen benutzerdefinierten Codec oder ein Plug-In für die Audio-/Videoverarbeitung schreiben, sollten Sie die Implementierung als MFT in Betracht ziehen.

 

DirectX Media Objects (DMOs) sind COM-basierte Datenstreamingkomponenten. In einigen Punkten ähneln DMOs Microsoft DirectShow-Filtern. Wie DirectShow-Filter verwenden DMOs Eingabedaten, um Ausgabedaten zu erzeugen. Die Anwendungsprogrammierschnittstellen (APPLICATION Programming Interfaces, APIs) für DMOs sind jedoch viel einfacher als die entsprechenden APIs für DirectShow. Daher sind DMOs einfacher zu erstellen, zu testen und zu verwenden. DMOs können in vielen Szenarien verwendet werden:

-   Anwendungen, die auf DirectShow basieren, können DMOs über einen DirectShow-Filter verwenden, der [als DMO Wrapperfilter](dmo-wrapper-filter.md) bezeichnet wird. Der Unterschied zwischen Filtern und DMOs ist für die Anwendung transparent. Die Anwendung ruft die DMO-APIs nicht direkt auf.
-   Anwendungen, die auf Microsoft DirectSound basieren, können DMOs mit Audioeffekt verwenden. Auch hier wird die Anwendung durch die DirectSound-APIs auf höherer Ebene vor den low-level DMO-APIs abgeschirmt.
-   Anwendungen können DMOs direkt verwenden.

Wenn Sie also eine DMO schreiben, erstellen Sie eine Komponente, die in einer Vielzahl von Anwendungen verwendet werden kann. Diese Dokumentation enthält die folgenden Abschnitte:

-   [Informationen zu DMOs](about-dmos.md)
-   [Verwenden von DMOs](using-dmos.md)
-   [Schreiben eines DMO](writing-a-dmo.md)
-   [Medienparameter](media-parameters.md)
-   [DMO Verweis](dmo-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directshow](directshow.md)
</dt> </dl>

 

 
