---
title: Unprämultiply-Effekt
description: Verwenden Sie diesen Effekt, um ein Bild von einem prämultipliierten Alpha in ein nicht multipliediertes Alpha zu konvertieren.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- Unpremultiply-Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a152803956b9839b881404be013c521dc0f5bfc764b2f07a8462275b523ba762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664878"
---
# <a name="unpremultiply-effect"></a>Unprämultiply-Effekt

Verwenden Sie diesen Effekt, um ein Bild von einem prämultipliierten Alpha in ein nicht multipliediertes Alpha zu konvertieren. Der Effekt ersetzt jedes Eingabepixel `P = {R, G, B, A}` `P' = {R/A, G/A, B/A, A}` durch in der Ausgabe.

Dieser Effekt hat keine Eigenschaften.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Unpremultiply.

## <a name="output-bitmap"></a>Ausgabebitmap

Die Größe der Ausgabebitmap ist mit der Größe der Eingabebitmap identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects.h                                                                      |
| Bibliothek                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
