---
description: 'In der folgenden Tabelle wird beschrieben, für welche Threads die Ink-Objektereignisse ausgeführt werden können. EventThreadsInkAddedFires im Ink-Thread oder im Thread des Aufrufers. Ein InkAdded-Ereignis, das durch Benutzerinteraktion mit dem InkCollector-Objekt, dem InkOverlay-Objekt oder dem InkPicture-Steuerelement generiert wird, wird im Ink-Thread ausgeführt. InkDeletedFires für den Ink-Thread oder den Thread des Aufrufers. Ein InkDeleted-Ereignis, das durch Benutzerinteraktion mit dem InkCollector-Objekt, dem InkOverlay-Objekt oder dem InkPicture-Steuerelement generiert wird, wird im Ink-Thread ausgeführt. '
ms.assetid: 410f7126-5c4c-4c0c-8aa6-c94f15c903fc
title: Ink-Objektereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63217f603b06703b7824c19d3a709fdb97f31c9890e3148a6eeefd1e681d63b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451937"
---
# <a name="ink-object-events"></a>Ink-Objektereignisse

In der folgenden Tabelle wird beschrieben, für welche Threads die [**Ink-Objektereignisse**](inkdisp-class.md) ausgeführt werden können.



| Ereignis                                    | Threads                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | Wird im Ink-Thread oder im Thread des Aufrufers ausgeführt.<br/> Ein [**InkAdded-Ereignis,**](inkdisp-inkadded.md) das durch Benutzerinteraktion mit dem [**InkCollector-Objekt,**](inkcollector-class.md) dem [**InkOverlay-Objekt**](inkoverlay-class.md) oder dem [InkPicture-Steuerelement](inkpicture-control-reference.md) generiert wird, wird im Ink-Thread ausgeführt.<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | Wird im Ink-Thread oder im Thread des Aufrufers ausgeführt.<br/> Ein [**InkDeleted-Ereignis,**](inkdisp-inkdeleted.md) das durch Benutzerinteraktion mit dem [**InkCollector-Objekt,**](inkcollector-class.md) dem [**InkOverlay-Objekt**](inkoverlay-class.md) oder dem [InkPicture-Steuerelement](inkpicture-control-reference.md) generiert wird, wird im Ink-Thread ausgeführt.<br/> |



 

 

 




