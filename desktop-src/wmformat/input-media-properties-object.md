---
title: Eigenschaften Objekt für Eingabemedien
description: Eigenschaften Objekt für Eingabemedien
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media-Format-SDK, Eingabemedien Eigenschaften Objekte
- Advanced Systems Format (ASF), Eingabemedien Eigenschaften Objekte
- ASF (Advanced Systems Format), Eingabemedien Eigenschaften Objekte
- Objekte, Eigenschaften von Eingabemedien Eigenschaften
- Eigenschaften der Eingabemedien Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103857995"
---
# <a name="input-media-properties-object"></a>Eigenschaften Objekt für Eingabemedien

Ein vom Writer-Objekt erstelltes Eigenschaften Objekt für Eingabemedien unterstützt die folgenden Schnittstellen. Auf diese Schnittstellen wird durch Aufrufen von **QueryInterface** für eine der Schnittstellen des Writer-Objekts zugegriffen.



| Schnittstelle                                        | BESCHREIBUNG                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Iwminputmedia-Eigenschaften**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Ruft die Eigenschaften eines Eingabestreams ab.                                                               |
| [**Iwmmedia-Eigenschaften**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Wird als Basisschnittstelle für die anderen Schnittstellen der Medien Eigenschaft verwendet (Eingabe, Ausgabe und Video).             |
| [**Iwmvideomedia-Eigenschaften**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Verwaltet die Eigenschaften eines Videostreams. Dies ist eine optionale Schnittstelle, die nur für Videostreams verfügbar ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Writer-Objekt**](writer-object.md)
</dt> </dl>

 

 




