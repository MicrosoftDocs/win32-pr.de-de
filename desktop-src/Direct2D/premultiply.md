---
title: Prämultiplizieren von Effekten
description: Verwenden Sie diesen Effekt, um ein Bild von einem nicht multiplizierten Alpha in ein prämultipliziertes Alpha zu konvertieren.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- prämultiplizieren von Effekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956784"
---
# <a name="premultiply-effect"></a>Prämultiplizieren von Effekten

Verwenden Sie diesen Effekt, um ein Bild von einem nicht multiplizierten Alpha in ein prämultipliziertes Alpha zu konvertieren. Der Effekt ersetzt jedes Eingabe Pixel `P = {R, G, B, A}` durch `P' = {R*A, G*A, B*A, A}` in der Ausgabe.

Dieser Effekt hat keine Eigenschaften.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Premultiply.

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

 

 
