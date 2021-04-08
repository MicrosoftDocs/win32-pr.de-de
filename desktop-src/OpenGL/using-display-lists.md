---
title: Verwenden von anzeigen Listen
description: Verwenden von anzeigen Listen
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, Anzeigen von Listen
- Anzeigelisten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855816"
---
# <a name="using-display-lists"></a>Verwenden von anzeigen Listen

Eine Anzeigeliste ist eine Gruppe von OpenGL-Funktionen, die für die nachfolgende Ausführung gespeichert wurden. Die Funktion " [**glnewlist**](glnewlist.md) " beginnt mit der Erstellung einer Anzeigeliste, und mit " [**glendlist**](glendlist.md) " wird Sie beendet. Mit wenigen Ausnahmen werden OpenGL-Funktionen, die zwischen **glnewlist** und **glendlist** aufgerufen werden, an die Anzeigeliste angehängt. (Eine Liste der Funktionen, die Sie in einer Anzeigeliste nicht speichern und ausführen können, finden Sie in der Liste mit den Funktionen von **glnewlist** .) Wenn Sie die Ausführung einer Liste oder einer Gruppe von Listen aufrufen möchten, verwenden Sie " [**glCallList**](glcalllist.md) " oder " [**glcalllists**](glcalllists.md) ", und geben Sie die identifizierende Anzahl einer bestimmten Liste oder Listen an. Sie verwalten die Indizes, die zum Identifizieren von anzeigen Listen mit " [**glgenlists**](glgenlists.md)", " [**gllistbase**](gllistbase.md)" und " [**glislist**](glislist.md)" verwendet werden. Verwenden Sie zum Löschen eines Satzes von Anzeigelisten " [**gldelta etelists**](gldeletelists.md)".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anzeigen von Listen verweisen](display-lists-reference.md)
</dt> </dl>

 

 




