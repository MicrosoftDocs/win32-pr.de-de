---
title: Eingabemedieneigenschaften-Objekt
description: Eingabemedieneigenschaften-Objekt
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Medienformat-SDK, Eingabemedieneigenschaftenobjekte
- Advanced Systems Format (ASF), Eingabemedieneigenschaftenobjekte
- ASF (Advanced Systems Format), Eingabemedieneigenschaftenobjekte
- Objekte, Eingabemedieneigenschaftenobjekte
- Eingabemedieneigenschaftenobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf5fac14de1c0fdc6619ab0dfe61feb9fcf577acb5c22dc2243a96d943921c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809030"
---
# <a name="input-media-properties-object"></a>Eingabemedieneigenschaften-Objekt

Ein vom Writer-Objekt erstelltes Eingabemedieneigenschaftenobjekt unterstützt die folgenden Schnittstellen. Auf diese Schnittstellen wird über einen Aufruf von **QueryInterface** auf einer der Schnittstellen des Writerobjekts zugegriffen.



| Schnittstelle                                        | BESCHREIBUNG                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Ruft die Eigenschaften eines Eingabestreams ab.                                                               |
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Wird als Basisschnittstelle für die anderen Medieneigenschaftenschnittstellen (Eingabe, Ausgabe und Video) verwendet.             |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Verwaltet die Eigenschaften eines Videostreams. Dies ist eine optionale Schnittstelle, die nur für Videostreams verfügbar ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Writer-Objekt**](writer-object.md)
</dt> </dl>

 

 




