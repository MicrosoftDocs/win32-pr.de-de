---
description: In der folgenden Tabelle wird beschrieben, in welchen Threads die erkenzercontext-Objekt Ereignisse ausgelöst werden können. Eventthreadserkentionauslöst für den Hintergrund Erkennungs Thread oder für den Thread, der die Erkennungsmethode des erkenzercontext-Objekts aufruft. "Erkentionwithalternativen" im Hintergrund Erkennungs Thread.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Erkenzercontext-Objekt Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960284"
---
# <a name="recognizercontext-object-events"></a>Erkenzercontext-Objekt Ereignisse

In der folgenden Tabelle wird beschrieben, in welchen Threads die [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt Ereignisse ausgelöst werden können.



| Ereignis                                                                               | Threads                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erkennung**](inkrecognizercontext-recognition.md)                             | Wird im Hintergrund Erkennungs Thread oder im Thread ausgelöst, der die Erkennungs [**Methode des**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts aufruft.<br/> |
| [**Erkentionwithalternativen**](inkrecognizercontext-recognitionwithalternates.md) | Wird im Hintergrund Erkennungs Thread ausgelöst.<br/>                                                                                                                                                               |



 

 

 




