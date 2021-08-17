---
description: In der folgenden Tabelle wird beschrieben, für welche Threads die RecognizerContext-Objektereignisse ausgeführt werden können. EventThreadsRecognitionFires für den Hintergrunderkennungsthread oder für den Thread, der die Recognize-Methode des RecognizerContext-Objekts aufruft. RecognitionWithAlternatesFires im Hintergrunderkennungsthread.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: RecognizerContext-Objektereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c8fa7aad4e7c6ba0dde2b38db4b82437b0732dda565aed8cc42750a339b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091440"
---
# <a name="recognizercontext-object-events"></a>RecognizerContext-Objektereignisse

In der folgenden Tabelle wird beschrieben, für welche Threads [**die RecognizerContext-Objektereignisse**](inkrecognizercontext-class.md) ausgeführt werden können.



| Ereignis                                                                               | Threads                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Erkennung**](inkrecognizercontext-recognition.md)                             | Wird für den Hintergrunderkennungsthread oder für den Thread, der die Recognize-Methode des [**RecognizerContext-Objekts**](inkrecognizercontext-class.md) [**aufruft,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) ausgeführt.<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Wird im Hintergrunderkennungsthread ausgeführt.<br/>                                                                                                                                                               |



 

 

 




