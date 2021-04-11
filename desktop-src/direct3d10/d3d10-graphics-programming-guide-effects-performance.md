---
description: Überlegungen zur Leistung (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Überlegungen zur Leistung (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041379"
---
# <a name="performance-considerations-direct3d-10"></a>Überlegungen zur Leistung (Direct3D 10)

## <a name="using-effect-pools"></a>Verwenden von Effect-Pools

Das Rendern von Pipelines wird häufig verwendet, um viele Shader zum Rendern verschiedener Objekttypen und spezieller Effekte zu verwenden. Der Shader ist eine Mischung aus Zuständen, die für alle Shader (z. b. eine Weltmatrix oder eine helle Position) und für jeden Shader spezifisch sind, z. b. die diffuse Farbe eines Objekts oder eine Glanz Hervorhebungs Berechnung. Ein Effekt Pool ist eine Position im Speicher, in der der Zustand gespeichert wird, der über viele Shader hinweg verwendet wird, sowie allgemeine Geräte Objekte, wie z. b. Shader, gerenstatusobjekte und Konstantenpuffer. Die Leistungsverbesserung ergibt sich aus der Aktualisierung des allgemeinen Zustands für alle Shader, die diesen Zustand benötigen.

Ein Effekt Pool ist ein gemeinsam genutzter Speicherort für den Zustand des Effekts. Ein Pool wird ähnlich wie ein Effekt erstellt. Sie kann aus dem Arbeitsspeicher (oder einer Datei oder einer Ressource) erstellt werden. Dies führt zu zwei unterschiedlichen Arten von Effekten: einen globalen Effekt, der nicht von einem Zustand in anderen Effekten abhängig ist, und ein untergeordneter Effekt, der von einem anderen Effekt abhängig ist.

Beim Erstellen des Effekts geben Sie an, ob ein Effekt ein globaler Effekt (der Standardfall) oder ein untergeordneter Effekt ist (durch Bereitstellen des d3d10 Effect-Flag zum Kompilieren des untergeordneten [ \_ \_ \_ \_ Effekts](d3d10-effect.md) ). Ein globaler Effekt kann als Effekt Pool dienen. ein untergeordneter Effekt kann kein Effekt Pool sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Effekts](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[Effekte (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



