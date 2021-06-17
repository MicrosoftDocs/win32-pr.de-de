---
title: Attribute mit mehreren Werten (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über Attribute mit mehreren Werten im Windows Media Format 11 SDK. Einige Medienelementattribute können mehrere Werte haben.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute,mehrere Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262692"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Attribute mit mehreren Werten (Windows Media Format 11 SDK)

Einigen vordefinierten Attributen können mehrere Werte zugewiesen werden. Beispielsweise ist **Interpret** ein Attribut, das mehrere Werte haben kann. Sie können [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) mehrmals aufrufen, um so viele **Interpretenwerte** wie erforderlich hinzuzufügen. Wenn Sie mehrere Aufrufe von **AddAttribute** für Attribute ausführen, die nicht mehrere Werte unterstützen, gibt die Methode möglicherweise einen Fehlercode zurück oder ignoriert einfach Ihre Anforderung.

In der folgenden Tabelle sind die Attribute aufgeführt, die mehrere Werte unterstützen. Einige Attribute können nur in ASF-Dateien mehrere Werte enthalten, während andere in ASF- und MP3-Dateien mehrere Werte enthalten können.



| attribute                                                 | Unterstützung für mehrere Werte |
|-----------------------------------------------------------|-----------------------------|
| [**Autor**](author.md)                                  | ASF, MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | ASF                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/Category**](wm-category.md)                        | ASF                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/2016**](wm-conductor.md)                      | ASF                         |
| [**WM/Director**](wm-director.md)                        | ASF                         |
| [**WM/Genre**](wm-genre.md)                              | ASF                         |
| [**WM/GenreID**](wm-genreid.md)                          | ASF                         |
| [**WM/Sprache**](wm-language.md)                        | ASF, MP3                    |
| [**WM/Synchronisierung \_**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/Stimmung**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/Picture**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/Producer**](wm-producer.md)                        | ASF                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | ASF                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/Writer**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> </dl>

 

 




