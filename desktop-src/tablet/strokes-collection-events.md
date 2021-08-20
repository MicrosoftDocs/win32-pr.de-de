---
description: In der folgenden Tabelle wird beschrieben, für welche Threads die Strokes-Auflistungsereignisse ausgeführt werden können. EventThreadsStrokesAddedFires im Ink-Thread oder im Thread des Aufrufers. Ein StrokesAdded-Ereignis, das durch Benutzerinteraktion mit dem InkCollector-Objekt, dem InkOverlay-Objekt oder dem InkPicture-Steuerelement generiert wird, wird im Ink-Thread ausgeführt. StrokesRemovedFires im Ink-Thread oder im Thread des Aufrufers. Ein StrokesRemoved-Ereignis, das durch Benutzerinteraktion mit dem InkCollector-Objekt, dem InkOverlay-Objekt oder dem InkPicture-Steuerelement generiert wird, wird im Ink-Thread ausgeführt.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Strichsammlungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24be819f63fa29cd0d650ce27f760984ca6d917886fe5f45e1ec72cf4c9fe2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589780"
---
# <a name="strokes-collection-events"></a>Strichsammlungsereignisse

In der folgenden Tabelle wird beschrieben, für welche Threads die [**Strokes-Auflistungsereignisse**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ausgeführt werden können.



| Ereignis                                               | Threads                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StricheAdded**](inkstrokes-strokesadded.md)     | Wird im Ink-Thread oder im Thread des Aufrufers ausgeführt.<br/> Ein [**StrokesAdded-Ereignis,**](inkstrokes-strokesadded.md) das durch Benutzerinteraktion mit dem [**InkCollector-Objekt,**](inkcollector-class.md) dem [**InkOverlay-Objekt**](inkoverlay-class.md) oder dem [InkPicture-Steuerelement](inkpicture-control-reference.md) generiert wird, wird im Ink-Thread ausgeführt.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Wird im Ink-Thread oder im Thread des Aufrufers ausgeführt.<br/> Ein [**StrokesRemoved-Ereignis,**](inkstrokes-strokesremoved.md) das durch Benutzerinteraktion mit dem [**InkCollector-Objekt,**](inkcollector-class.md) dem [**InkOverlay-Objekt**](inkoverlay-class.md) oder dem [InkPicture-Steuerelement](inkpicture-control-reference.md) generiert wird, wird im Ink-Thread ausgeführt.<br/> |



 

 

 
