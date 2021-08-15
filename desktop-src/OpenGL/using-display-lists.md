---
title: Verwenden von Anzeigelisten
description: Verwenden von Anzeigelisten
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, Listen anzeigen
- Anzeigelisten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322721868f3bf994382a7604aa2cb76802f268aec7a1298aaa14e3066d5f6cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932800"
---
# <a name="using-display-lists"></a>Verwenden von Anzeigelisten

Eine Anzeigeliste ist eine Gruppe von OpenGL-Funktionen, die für die nachfolgende Ausführung gespeichert wurden. Die [**glNewList-Funktion**](glnewlist.md) beginnt mit der Erstellung einer Anzeigeliste, und [**glEndList**](glendlist.md) beendet sie. Bis auf wenige Ausnahmen werden OpenGL-Funktionen, die zwischen **glNewList** und **glEndList** aufgerufen werden, an die Anzeigeliste angefügt. (Eine Liste der Funktionen, die Sie nicht in einer Anzeigeliste speichern und ausführen können, finden Sie unter **glNewList.)** Um die Ausführung einer Liste oder einer Gruppe von Listen auszulösen, verwenden Sie [**glCallList**](glcalllist.md) oder [**glCallLists,**](glcalllists.md) und geben Sie die identifizierende Nummer einer bestimmten Liste oder Listen an. Sie verwalten die Indizes, die zum Identifizieren von Anzeigelisten verwendet werden, mit [**glGenLists,**](glgenlists.md) [**glListBase**](gllistbase.md)und [**glIsList.**](glislist.md) Verwenden Sie [**glDeleteLists,**](gldeletelists.md)um einen Satz von Anzeigelisten zu löschen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu Anzeigelisten](display-lists-reference.md)
</dt> </dl>

 

 




