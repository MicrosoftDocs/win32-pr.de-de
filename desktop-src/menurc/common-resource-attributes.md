---
title: Allgemeine Ressourcen Attribute
description: Die für 16-Bit-Windows unterstützten Ressourcen Definitions Anweisungen enthalten eine Load-Load-Option, die das Lade-und Arbeitsspeicher Merkmal der Ressource angibt.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338597"
---
# <a name="common-resource-attributes"></a>Allgemeine Ressourcen Attribute

Die für 16-Bit-Windows unterstützten Ressourcen Definitions Anweisungen enthalten eine *Load-Load-* Option, die das Lade-und Arbeitsspeicher Merkmal der Ressource angibt. Diese Attribute sind aus Gründen der Abwärtskompatibilität in Ressourcen Skripts zulässig, werden jedoch ignoriert. Windows-Ressourcen werden geladen, wenn das entsprechende Modul geladen wird, und werden freigegeben, wenn das Modul entladen wird.

## <a name="load-attributes"></a>Attribute laden

Die Load-Attribute geben an, wann die Ressource geladen werden soll. Der Load-Parameter muss eines der folgenden Attribute sein.



| Attribut      | BESCHREIBUNG                                                                  |
|----------------|------------------------------------------------------------------------------|
| **Vorab laden**    | Ignoriert. In 16-Bit-Fenstern wird die Ressource mit der ausführbaren Datei geladen. |
| **LOADONCALL** | Ignoriert. In 16-Bit-Fenstern wird die Ressource geladen, wenn Sie aufgerufen wird.              |



 

## <a name="memory-attributes"></a>Speicher Attribute

Die Speicher Attribute geben an, ob die Ressource fest oder verschiebbar ist, ob Sie verworfen werden kann und ob Sie rein ist. Der Speicher Parameter kann eines oder mehrere der folgenden Attribute sein.



| Attribut       | BESCHREIBUNG                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | Ignoriert. In 16-Bit-Fenstern verbleibt die Ressource an einem Speicherort mit fester Größe.                                                              |
| **Moveable**    | Ignoriert. In 16-Bit-Fenstern kann die Ressource ggf. verschoben werden, um Arbeitsspeicher zu komprimieren.                                                     |
| **Entfernbare** | Ignoriert. In 16-Bit-Fenstern kann die Ressource verworfen werden, wenn Sie nicht mehr benötigt wird.                                                            |
| **Rein**        | Ignoriert. Wird für die Kompatibilität mit vorhandenen Ressourcen Skripts akzeptiert.                                                                       |
| **Unreinen**      | Ignoriert. Wird für die Kompatibilität mit vorhandenen Ressourcen Skripts akzeptiert.                                                                       |
| **Genu**      | Ignoriert. In 16-Bit-Fenstern wird Shared für reguläre Module ignoriert. Für eine Ressource aus einem Windows-Rom-Modul wird der Arbeitsspeicher freigegeben.        |
| **Nicht freigegebene**   | Ignoriert. In 16-Bit-Fenstern wird NonShared für reguläre Module ignoriert. Für eine Ressource aus einem Windows-Rom-Modul wird der Arbeitsspeicher nicht freigegeben. |



 

 

 




