---
title: Durchlässigkeitsmetadateneffekt
description: Sie können diesen Effekt verwenden, um einen Bereich eines Eingabebilds als nicht transparent zu markieren, sodass interne Renderingoptimierungen für das Diagramm möglich sind.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be14699214337dc3f8c6e9e525f128a382c14ee479af08b99ea1f9eadd00041d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665320"
---
# <a name="opacity-metadata-effect"></a>Durchlässigkeitsmetadateneffekt

Sie können diesen Effekt verwenden, um einen Bereich eines Eingabebilds als nicht transparent zu markieren, sodass interne Renderingoptimierungen für das Diagramm möglich sind.

> [!Note]  
> Dieser Effekt ändert nicht, dass das Bild selbst nicht transparent ist. Sie ändert die dem Bild zugeordneten Daten, sodass der Renderer davon ausgegangen wird, dass der angegebene Bereich nicht transparent ist.

 

Die CLSID für diesen Effekt ist CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                 | Typ und Standardwert                                                             | Beschreibung                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA \_ PROP \_ INPUT \_ OPAQUE \_ RECT <br/> | D2D1 \_ VECTOR \_ 4F<br/> (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX) <br/> | Der nicht transparente Teil des Quellbilds. Der Standardwert ist das gesamte Eingabebild.<br/> |



 

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

 

