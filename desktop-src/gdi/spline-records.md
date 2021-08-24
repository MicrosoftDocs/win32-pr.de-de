---
description: Splinedatensätze stellen die quadratischen Kurven (d. h. quadratische B-Splines) dar, die von TrueType verwendet werden.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Spline-Datensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbaf3730f327501bd55b2e35b9410f03fd0559cbb5e36d87a3052901d26e5f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613650"
---
# <a name="spline-records"></a>Spline-Datensätze

Splinedatensätze stellen die quadratischen Kurven (d. h. quadratische B-Splines) dar, die von TrueType verwendet werden. Ein Splinedatensatz beginnt mit dem letzten Punkt im vorherigen Datensatz (oder für den ersten Datensatz in der Kontur mit dem Ausgangspunkt). Für den ersten Splinedatensatz befinden sich der Ausgangspunkt und der letzte Punkt im Datensatz auf der Glyphengliederung. Für alle anderen Splinedatensätze befindet sich nur der letzte Punkt auf der Glyphengliederung. Alle anderen Punkte in den Splinedatensätzen befinden sich nicht in der Glyphengliederung und müssen als Steuerungspunkte von B-Splines gerendert werden.

Der letzte Spline- oder Polyliniendatensatz in einer Kontur endet immer mit dem Ausgangspunkt der Kontur. Durch diese Anordnung wird sichergestellt, dass jede Kontur geschlossen wird.

Da B-Splines drei Punkte erfordern (einen Punkt von der Glyphengliederung zwischen zwei Punkten, die sich in der Kontur befinden), müssen Sie einige Berechnungen durchführen, wenn ein Splinedatensatz mehr als einen Offkurvenpunkt enthält.

Wenn z. B. ein Splinedatensatz drei Punkte (A, B und C) enthält und es sich nicht um den ersten Datensatz handelt, sind die Punkte A und B von der Glyphengliederung abgrenzt. Verwenden Sie zum Interpretieren von Punkt A die aktuelle Position (die sich immer auf der Glyphengliederung befindet) und den Punkt auf der Glyphengliederung zwischen den Punkten A und B. Um den Mittelpunkt (M) zwischen A und B zu finden, können Sie die folgende Berechnung ausführen.

M = A + (B A)/2

Der Mittelpunkt zwischen aufeinander folgenden Off-Outline-Punkten in einem Splinedatensatz ist ein Punkt in der Glyphengliederung gemäß der Definition des spline-Formats, das in TrueType-Schriftarten verwendet wird.

Wenn die aktuelle Position durch P festgelegt wird, sind die beiden quadratischen Splines, die durch diesen Splinedatensatz definiert werden, (P, A, M) und (M, B, C).

 

 



