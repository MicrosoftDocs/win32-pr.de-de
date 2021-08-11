---
title: Allgemeine Ressourcenattribute
description: Die ressourcendefinitionsbasierten Anweisungen, die auf 16-Bit-Windows enthalten eine load-mem-Option, die die Lade- und Arbeitsspeichermerkmale der Ressource angibt.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b7bf01f95c700f12d130490673ef4f0df61cb84ae8077ca759655a2c4a1577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235577"
---
# <a name="common-resource-attributes"></a>Allgemeine Ressourcenattribute

Die ressourcendefinitionsbasierten Anweisungen, die auf 16-Bit-Windows enthalten eine *load-mem-Option,* die die Lade- und Arbeitsspeichermerkmale der Ressource angibt. Diese Attribute sind aus Gründen der Abwärtskompatibilität in Ressourcenskripts zulässig, werden jedoch ignoriert. Windows werden beim Laden des entsprechenden Moduls geladen und beim Entladen des Moduls wieder frei.

## <a name="load-attributes"></a>Laden von Attributen

Die Load-Attribute geben an, wann die Ressource geladen werden soll. Der load-Parameter muss eines der folgenden Attribute sein.



| attribute      | BESCHREIBUNG                                                                  |
|----------------|------------------------------------------------------------------------------|
| **Vorspannung**    | Ignoriert. In 16-Bit-Windows wird die Ressource mit der ausführbaren Datei geladen. |
| **Loadoncall** | Ignoriert. In 16-Bit-Windows wird die Ressource geladen, wenn sie aufgerufen wird.              |



 

## <a name="memory-attributes"></a>Speicherattribute

Die Speicherattribute geben an, ob die Ressource fest oder verschiebbar ist, ob sie verworfen werden kann und ob sie rein ist. Der Memory-Parameter kann eines oder mehrere der folgenden Attribute sein.



| attribute       | BESCHREIBUNG                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **FIXED**       | Ignoriert. In 16-Bit-Windows bleibt die Ressource an einem festen Speicherort.                                                              |
| **Bewegliche**    | Ignoriert. In 16-Bit-Windows kann die Ressource bei Bedarf verschoben werden, um Arbeitsspeicher zu komprimen.                                                     |
| **Discardable** | Ignoriert. In 16-Bit-Windows kann die Ressource verworfen werden, wenn sie nicht mehr benötigt wird.                                                            |
| **Reine**        | Ignoriert. Wird aus Kompatibilitäts- mit vorhandenen Ressourcenskripts akzeptiert.                                                                       |
| **Unreine**      | Ignoriert. Wird aus Kompatibilitäts- mit vorhandenen Ressourcenskripts akzeptiert.                                                                       |
| **geteilt**      | Ignoriert. In 16-Bit-Windows wird SHARED für reguläre Module ignoriert. Für eine Ressource aus einem ROM-Windows wird der Arbeitsspeicher gemeinsam genutzt.        |
| **NICHTFREIGABE**   | Ignoriert. In 16-Bit-Windows wird NONSHARED für reguläre Module ignoriert. Für eine Ressource aus einem ROM-Windows wird der Arbeitsspeicher nicht gemeinsam genutzt. |



 

 

 




