---
title: Direct3D 12-Raytracing, HLSL-Interna
description: Die folgenden HLSL-Shader unterstützen die Direct3D 12-Raytracing-Pipeline.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2e7cc7053705bd66b37d91f3ee06a6a1f249a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339420"
---
# <a name="raytracing-hlsl-intrinsics"></a>Systeminterne Funktionen von Raytracing HLSL

Die folgenden HLSL-intrinisc-Funktionen unterstützen die Direct3D 12-Raytracing-Pipeline. 

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema | BESCHREIBUNG |
|-|-|
| [**AcceptHitAndEndSearch-Funktion**](accepthitandendsearch-function.md) | Wird in einem beliebigen Treffer-Shader verwendet, um einen Commit für den aktuellen Treffer durchzusetzen und dann nach weiteren Treffern für den Strahl zu suchen. |
| [**CallShader-Funktion**](callshader-function.md) | Ruft einen anderen Shader innerhalb eines Shaders auf. |
| [**IgnoreHit-Funktion**](ignorehit-function.md) | Wird von einem beliebigen Treffer-Shader aufgerufen, um den Treffer zu verwerfen und den Shader zu beenden. |
| [**Primitiveingedex-Funktion**](primitiveindex.md) | Ruft den automatisch generierten Index des primitiven innerhalb der Geometrie innerhalb der Beschleunigung der Beschleunigung-Struktur der untersten Ebene ab. |
| [**ReportHit-Funktion**](reporthit-function.md) | Wird von einem Schnittmengen-Shader aufgerufen, um eine Strahl Überschneidung zu melden. |
| [**TraceRay-Funktion**](traceray-function.md) | Sendet einen Strahl in eine Suche nach Treffern in einer Beschleunigungs Struktur. |

## <a name="related-topics"></a>Zugehörige Themen

* [Kern Referenz](direct3d-12-core-reference.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
