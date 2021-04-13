---
title: Unvorhersehunmultiplizieren
description: Verwenden Sie diesen Effekt zum Konvertieren eines Bilds von einem prämultiplizierten Alpha in ein unvorhersehvielfaches alpha.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- unvorhersehunmultiplizieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392113"
---
# <a name="unpremultiply-effect"></a>Unvorhersehunmultiplizieren

Verwenden Sie diesen Effekt zum Konvertieren eines Bilds von einem prämultiplizierten Alpha in ein unvorhersehvielfaches alpha. Der Effekt ersetzt jedes Eingabe Pixel `P = {R, G, B, A}` durch `P' = {R/A, G/A, B/A, A}` in der Ausgabe.

Dieser Effekt hat keine Eigenschaften.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Unpremultiply.

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
