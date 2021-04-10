---
title: Attribute mit mehreren Werten (Windows Media Format 11 SDK)
description: Attribute mit mehreren Werten
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media-Format-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, mehrere Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039952"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Attribute mit mehreren Werten (Windows Media Format 11 SDK)

Einigen vordefinierten Attributen können mehrere Werte zugewiesen werden. Beispielsweise ist " **Artist** " ein Attribut, das mehrere Werte aufweisen kann. Sie können [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) mehrmals aufzurufen, um beliebig viele **Künstler** Werte hinzuzufügen. Wenn Sie mehrere Aufrufe von **AddAttribute** für Attribute durchführen, die mehrere Werte nicht unterstützen, gibt die Methode möglicherweise einen Fehlercode zurück, oder ignorieren Sie Ihre Anforderung einfach.

In der folgenden Tabelle werden die Attribute aufgelistet, die mehrere Werte unterstützen. Einige Attribute können mehrere Werte nur in ASF-Dateien aufweisen, während andere mehrere Werte in den Dateien "ASF" und "MP3" aufweisen können.



| Attribut                                                 | Unterstützung für mehrere Werte |
|-----------------------------------------------------------|-----------------------------|
| [**Autor**](author.md)                                  | ASF, MP3                    |
| [**WM/albumartist**](wm-albumartist.md)                  | ASF                         |
| [**WM/albumcoverurl**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/Kategorie**](wm-category.md)                        | ASF                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/Dirigent**](wm-conductor.md)                      | ASF                         |
| [**WM/Director**](wm-director.md)                        | ASF                         |
| [**WM/Genre**](wm-genre.md)                              | ASF                         |
| [**WM/GenreID**](wm-genreid.md)                          | ASF                         |
| [**WM/Sprache**](wm-language.md)                        | ASF, MP3                    |
| [**Synchronisierte WM/Liedtexte \_**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/Stimmung**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/Bild**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/Producer**](wm-producer.md)                        | ASF                         |
| [**WM/promotionurl**](wm-promotionurl.md)                | ASF                         |
| [**WM/userweburl**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/Writer**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> </dl>

 

 




