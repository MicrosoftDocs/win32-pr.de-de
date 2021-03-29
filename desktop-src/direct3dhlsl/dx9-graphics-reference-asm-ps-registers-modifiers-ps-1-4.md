---
title: PS \_ 1 \_ 4-quellregistrierungs modifiziererer für texld, texcrd
description: Zwei Pixel-Shader Version 1 \_ 4 Textur Adress Anweisungen, texld-PS \_ 1 \_ 4 und texcrd-PS, haben eine benutzerdefinierte Syntax.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2019
ms.locfileid: "104101142"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a>PS \_ 1 \_ 4-quellregistrierungs modifiziererer für texld, texcrd

Zwei Pixel-Shader Version 1 \_ 4 Textur Adress Anweisungen, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) und [texcrd-PS](texcrd---ps.md), haben eine benutzerdefinierte Syntax. Diese Anweisungen unterstützen Ihren eigenen Satz von Quell Registrierungs Modifizierern, Quell Registrierungs-Selectors und Ziel-Register-Schreib Masken, wie hier gezeigt.

## <a name="source-register-modifiers-for-texld-and-texcrd"></a>Quellregistrierungs modifiziererer für texld und texcrd

Diese Modifizierer stellen eine Projective Teilungs Funktionalität bereit, indem die x-und y-Werte durch die z-oder w-Werte aufgeteilt werden.



| Quellregistrierungs modifiziererer | BESCHREIBUNG                | Syntax       |
|---------------------------|----------------------------|--------------|
| \_DZ                      | Dividieren von x, y-Komponenten durch z | Registrieren von \_ DZ |
| \_db                      | Dividieren von x, y-Komponenten durch z | Datenbank \_ registrieren |
| \_DW                      | Dividieren von x, y-Komponenten durch w | \_DW registrieren |
| \_da                      | Dividieren von x, y-Komponenten durch w | Registrieren von \_ da |



 

### <a name="remarks"></a>Bemerkungen

Der-Modifizierer für die-oder-Datenbank \_ \_ führt Folgendes aus:


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



Der \_ DW-oder \_ da-Modifizierer führt Folgendes aus:


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader-quellregistrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




