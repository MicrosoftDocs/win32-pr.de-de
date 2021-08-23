---
title: Raynutzlaststruktur
description: Eine benutzerdefinierte Struktur, die als inout-Argument in einem TraceRay-Aufruf und als Inout-Parameter in den Shadertypen bereitgestellt wird, die auf die Raynutzlast zugreifen können.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c1c6944bc66d33ebd134d6e2d0899c1992624cfb4db3b0fc0aaa80a1ef99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565630"
---
# <a name="ray-payload-structure"></a>Raynutzlaststruktur 

Eine benutzerdefinierte -Struktur, die als Inout-Argument in einem [**TraceRay-Aufruf**](traceray-function.md) und als Inout-Parameter in den Shadertypen bereitgestellt [](miss-shader.md) wird, die auf die Raynutzlast zugreifen können. Dazu gehören alle [Treffer,](any-hit-shader.md)der nächstgelegene Treffer und die Shader für Fehlschlage. [](closest-hit-shader.md) Alle Shader, die auf die Raynutzlast zugreifen, müssen die gleiche Struktur wie beim ursprünglichen **TraceRay-Aufruf** verwenden.  Auch wenn einer dieser Shader überhaupt nicht auf die Raynutzlast verweist, muss er dennoch die übereinstimmende Nutzlast als ursprünglichen **TraceRay-Aufruf** angeben.

