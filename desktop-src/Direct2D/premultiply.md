---
title: Premultiply-Effekt
description: Verwenden Sie diesen Effekt, um ein Bild von unpremultiplied alpha in premultiplied alpha zu konvertieren.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- premultiply-Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af158ab8f885c51d2dce15d5bfbc5c24f34f6a980ebc8e8f4631617d31a2a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075024"
---
# <a name="premultiply-effect"></a>Premultiply-Effekt

Verwenden Sie diesen Effekt, um ein Bild von unpremultiplied alpha in premultiplied alpha zu konvertieren. Der Effekt ersetzt jedes Eingabepixel `P = {R, G, B, A}` `P' = {R*A, G*A, B*A, A}` durch in der Ausgabe.

Dieser Effekt hat keine Eigenschaften.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Premultiply.

## <a name="output-bitmap"></a>Ausgabebitmap

Die Ausgabebitmapgröße entspricht der Größe der Eingabebitmap.

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

 

 
