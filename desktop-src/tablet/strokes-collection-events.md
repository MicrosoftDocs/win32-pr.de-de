---
description: In der folgenden Tabelle wird beschrieben, in welchen Threads die Striche-Auflistungs Ereignisse auslösen können. Eventthreadsstrokesaddedfires im frei Hand Thread oder im Thread des Aufrufers. Ein von der Benutzerinteraktion mit dem InkCollector-Objekt, dem InkOverlay-Objekt oder dem InkPicture-Steuerelement generiertes Ereignis "StrokesAdded" wird auf dem frei Hand Thread ausgelöst. Strokesremovedfires im frei Hand Thread oder im Thread des Aufrufers. Ein von der Benutzerinteraktion mit dem InkCollector-Objekt, dem InkOverlay-Objekt oder dem InkPicture-Steuerelement generiertes Ereignis, das durch eine Benutzerinteraktion generiert wird, wird im frei Hand Thread ausgelöst.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Striche-Sammlungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04388179c53a4b85c5333ae6061cdd7612967174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351578"
---
# <a name="strokes-collection-events"></a>Striche-Sammlungs Ereignisse

In der folgenden Tabelle wird beschrieben, in welchen Threads die [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistungs Ereignisse auslösen können.



| Ereignis                                               | Threads                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | Wird im frei Hand Thread oder im Thread des Aufrufers ausgelöst.<br/> Ein von der Benutzerinteraktion mit dem [**InkCollector**](inkcollector-class.md) -Objekt, dem [**InkOverlay**](inkoverlay-class.md) -Objekt oder dem [InkPicture](inkpicture-control-reference.md) -Steuerelement generiertes Ereignis " [**StrokesAdded**](inkstrokes-strokesadded.md) " wird auf dem frei Hand Thread ausgelöst.<br/>     |
| [**Über strokesentfernt**](inkstrokes-strokesremoved.md) | Wird im frei Hand Thread oder im Thread des Aufrufers ausgelöst.<br/> Ein [**von**](inkstrokes-strokesremoved.md) der Benutzerinteraktion mit dem [**InkCollector**](inkcollector-class.md) -Objekt, dem [**InkOverlay**](inkoverlay-class.md) -Objekt oder dem [InkPicture](inkpicture-control-reference.md) -Steuerelement generiertes Ereignis, das durch eine Benutzerinteraktion generiert wird, wird im frei Hand Thread ausgelöst.<br/> |



 

 

 
