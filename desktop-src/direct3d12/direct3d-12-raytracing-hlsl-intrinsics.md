---
title: Direct3D 12-Raytracing, HLSL-Interna
description: Hier finden Sie Links zu Artikeln, in denen intrinsische Funktionen der high-level shader language (HLSL) beschrieben werden, die die Direct3D 12-Raytracingpipeline unterstützen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06687866354611f44f295ff4fe2cf171068e83c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396475"
---
# <a name="raytracing-hlsl-intrinsics"></a>Intrinsische Raytracing-HLSL-Eigenschaften

Die folgenden HLSL-Intriniskfunktionen unterstützen die Direct3D 12-Raytracingpipeline. 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema | Beschreibung |
|-|-|
| [**AcceptHitAndEndSearch-Funktion**](accepthitandendsearch-function.md) | Wird in einem beliebigen Treffer-Shader verwendet, um den aktuellen Treffer zu commiten und dann die Suche nach mehr Treffern für den Strahl zu beenden. |
| [**CallShader-Funktion**](callshader-function.md) | Ruft einen anderen Shader innerhalb eines Shaders auf. |
| [**IgnoreHit-Funktion**](ignorehit-function.md) | Wird von einem beliebigen Treffer-Shader aufgerufen, um den Treffer abzulehnen und den Shader zu beenden. |
| [**PrimitiveIndex-Funktion**](primitiveindex.md) | Ruft den automatisch generierten Index des Primitiven innerhalb der Geometrie innerhalb der Beschleunigungsstrukturinstanz der unteren Ebene ab. |
| [**ReportHit-Funktion**](reporthit-function.md) | Wird von einem Schnittpunkt-Shader aufgerufen, um eine Strahlschnittmenge zu melden. |
| [**TraceRay-Funktion**](traceray-function.md) | Sendet einen Strahl in eine Suche nach Treffern in einer Beschleunigungsstruktur. |

## <a name="related-topics"></a>Zugehörige Themen

* [Kernreferenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
