---
title: Mischung
description: Blending kombiniert die R-, G-, B- und A-Werte eines Fragments mit den Werten, die im Framepuffer an der entsprechenden Position gespeichert sind.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- OpenGL-Verarbeitungspipeline, Mischen
- Mischen von OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b38786d2320a646bd6cac096e535e4e1441df98522ac86a146836b929c0986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361434"
---
# <a name="blending"></a>Mischung

Blending kombiniert die R-, G-, B- und A-Werte eines Fragments mit den Werten, die im Framepuffer an der entsprechenden Position gespeichert sind. Die Mischung, die nur im RGBA-Modus ausgeführt wird, hängt vom Alphawert des Fragments und dem des entsprechenden aktuell gespeicherten Pixels ab. sie kann auch von den RGB-Werten abhängen. Sie steuern das Mischen mit [**glBlendFunc,**](glblendfunc.md)mit dem Sie die Quell- und Zielmischungsfaktoren angeben.

 

 




