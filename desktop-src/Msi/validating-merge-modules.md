---
description: Autoren sollten die Validierung für jedes neue oder neu geänderte Mergemodul ausführen, bevor sie versuchen, das Modul zum ersten Mal in einer Installationsdatenbank zusammen zu führen.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Überprüfen von Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5a226f72e35ce4ee76599444e86ef80bd71a8866ca80eef2a5da04a87fb79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995799"
---
# <a name="validating-merge-modules"></a>Überprüfen von Mergemodulen

Autoren sollten die Validierung für jedes neue oder neu geänderte Mergemodul ausführen, bevor sie versuchen, das Modul zum ersten Mal in einer Installationsdatenbank zusammen zu führen. Die Überprüfung des Mergemoduls [](package-validation.md) funktioniert auf die gleiche Weise wie die Paketvalidierung, verwendet jedoch einen anderen Satz von internen Konsistenzauswertungen (Internal [Consistency Evaluators,](internal-consistency-evaluators-ices.md) ICEs), die für das Zusammenführen von Modulen spezifisch sind. Weitere Informationen zu diesen MERGE-Modul-ICEs finden Sie unter [Merge Module ICE Reference](merge-module-ice-reference.md).

Mergemodul-ICEs werden in der CUB-Datei des Mergemoduls "Mergemod.cub" gespeichert. Bei der Installation des Orca-Tools oder von ms merger2 werden auch die Dateien Logo.cub, Darice.cub und Mergemod.cub angezeigt.

Weitere Informationen finden Sie unter [Merge Module ICE Reference (ICE-Referenz zum Mergemodul).](merge-module-ice-reference.md)

 

 



