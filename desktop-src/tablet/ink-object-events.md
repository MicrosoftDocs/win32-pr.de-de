---
description: 'In der folgenden Tabelle wird beschrieben, in welchen Threads die frei Hand Objekt Ereignisse ausgelöst werden können. Eventthreadsinkaddedfires im frei Hand Thread oder im Thread des Aufrufers. Ein InkAdded-Ereignis, das von der Benutzerinteraktion mit dem InkCollector-Objekt, dem InkOverlay-Objekt oder dem InkPicture-Steuerelement generiert wurde, wird im frei Hand Thread ausgelöst. Inkdeletedauslöst im frei Hand Thread oder im Thread des Aufrufers. Ein InkDeleted-Ereignis, das von der Benutzerinteraktion mit dem InkCollector-Objekt, dem InkOverlay-Objekt oder dem InkPicture-Steuerelement generiert wird, wird im frei Hand Thread ausgelöst. '
ms.assetid: 410f7126-5c4c-4c0c-8aa6-c94f15c903fc
title: Frei Hand Objekt Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0375606b4f4a2f257aa00c360c764972f28c467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484795"
---
# <a name="ink-object-events"></a>Frei Hand Objekt Ereignisse

In der folgenden Tabelle wird beschrieben, in welchen Threads die frei [**Hand Objekt Ereignisse**](inkdisp-class.md) ausgelöst werden können.



| Ereignis                                    | Threads                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Wird im frei Hand Thread oder im Thread des Aufrufers ausgelöst.<br/> Ein [**InkAdded**](inkdisp-inkadded.md) -Ereignis, das von der Benutzerinteraktion mit dem [**InkCollector**](inkcollector-class.md) -Objekt, dem [**InkOverlay**](inkoverlay-class.md) -Objekt oder dem [InkPicture](inkpicture-control-reference.md) -Steuerelement generiert wurde, wird im frei Hand Thread ausgelöst.<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Wird im frei Hand Thread oder im Thread des Aufrufers ausgelöst.<br/> Ein [**InkDeleted**](inkdisp-inkdeleted.md) -Ereignis, das von der Benutzerinteraktion mit dem [**InkCollector**](inkcollector-class.md) -Objekt, dem [**InkOverlay**](inkoverlay-class.md) -Objekt oder dem [InkPicture](inkpicture-control-reference.md) -Steuerelement generiert wird, wird im frei Hand Thread ausgelöst.<br/> |



 

 

 




