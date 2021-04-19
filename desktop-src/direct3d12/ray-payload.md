---
title: Ray-Nutz Last Struktur
description: Eine benutzerdefinierte Struktur, die als ein INOUT-Argument in einem traceray-Befehl bereitgestellt wird, und als INOUT-Parameter in den shadertypen, die möglicherweise auf die Ray-Nutzlast zugreifen.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106363830"
---
# <a name="ray-payload-structure"></a>Ray-Nutz Last Struktur 

Eine benutzerdefinierte Struktur, die als ein INOUT-Argument in einem [**traceray**](traceray-function.md) -Befehl bereitgestellt wird, und als INOUT-Parameter in den shadertypen, die möglicherweise auf die Ray-Nutzlast zugreifen, einschließlich [Treffer](any-hit-shader.md), [nächster Treffer](closest-hit-shader.md)und [fehlshader](miss-shader.md) . Alle Shader, die auf die Ray-Nutzlast zugreifen, müssen dieselbe Struktur wie die des ursprünglichen **traceray** -Aufrufes verwenden.  Auch wenn einer dieser Shader überhaupt nicht auf die Ray-Nutzlast verweist, muss er trotzdem die passende Nutzlast als ursprünglichen **traceray** -Aufrufwert angeben.

