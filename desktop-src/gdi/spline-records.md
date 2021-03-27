---
description: Spline-Datensätze stellen die quadratischen Kurven (d. h. Quadratische b-Splines) dar, die von TrueType verwendet werden.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Spline-Datensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755840"
---
# <a name="spline-records"></a>Spline-Datensätze

Spline-Datensätze stellen die quadratischen Kurven (d. h. Quadratische b-Splines) dar, die von TrueType verwendet werden. Ein Spline-Datensatz beginnt mit dem letzten Punkt im vorherigen Datensatz (oder für den ersten Datensatz in der Kontur mit dem Ausgangspunkt). Für den ersten Spline-Datensatz befinden sich der Anfangspunkt und der letzte Punkt im Datensatz in der Symbol Gliederung. Für alle anderen Spline-Datensätze befindet sich nur der letzte Punkt in der Symbol Gliederung. Alle anderen Punkte in den Spline-Datensätzen befinden sich außerhalb der Symbol Gliederung und müssen als Steuerpunkte der b-Splines gerendert werden.

Der letzte Spline-oder polyliniendatensatz in einer Kontur endet immer mit dem Anfangspunkt der Kontur. Durch diese Anordnung wird sichergestellt, dass jede Kontur geschlossen wird.

Da b-Splines drei Punkte benötigen (ein Punkt von der Symbol Gliederung zwischen zwei Punkten, die sich auf dem Umriss befinden), müssen Sie einige Berechnungen durchführen, wenn ein Spline-Datensatz mehr als einen Off-Kurven Punkt enthält.

Wenn ein Spline-Datensatz z. b. drei Punkte (a, B und C) enthält und es sich nicht um den ersten Datensatz handelt, werden die Punkte a und B außerhalb der Symbol Gliederung angezeigt. Um Punkt A zu interpretieren, verwenden Sie die aktuelle Position (die sich immer auf der Symbol Gliederung befindet) und den Punkt auf der Symbol Gliederung zwischen den Punkten A und B. Um den Mittelpunkt (M) zwischen A und B zu ermitteln, können Sie die folgende Berechnung ausführen.

M = A + (B A)/2

Der Mittelpunkt zwischen aufeinanderfolgenden offumriss-Punkten in einem Spline-Datensatz ist ein Punkt auf der Symbol Gliederung, gemäß der Definition des in TrueType-Schriftarten verwendeten Spline-Formats.

Wenn die aktuelle Position durch P festgelegt wird, sind die beiden quadratischen Splines, die von diesem Spline-Datensatz definiert werden, (P, A, M) und (M, B, C).

 

 



