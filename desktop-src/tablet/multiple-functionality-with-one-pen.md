---
description: Ein Tablet PC-Stift hat möglicherweise mehr als ein Ende, das mit dem Digitalisierer interagieren kann.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Mehrere Funktionen mit einem Stift
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349879"
---
# <a name="multiple-functionality-with-one-pen"></a>Mehrere Funktionen mit einem Stift

Ein Tablet PC-Stift hat möglicherweise mehr als ein Ende, das mit dem Digitalisierer interagieren kann. Wenn beide Enden des Stifts Ereignisse generieren können, kann ein Ende verwendet werden, um frei Hand Eingaben, SELECT-und Point-Funktionen zu verwenden, und das andere Ende kann für andere Funktionen wie z. b. das Löschen verwendet werden.

Um diese Funktionalität zu implementieren, muss Ihre Anwendung in der Lage sein, zu bestimmen, welches Ende des Stifts verwendet wird, und damit, wann die Darstellung des Cursors geändert werden soll. Dies ist möglich, indem Sie den Status der [**invertierten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) Eigenschaft für das [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt suchen.

Ausführliche Informationen zur Verwendung der Rückseite des Stifts zum Löschen finden Sie unter Löschen von frei Hand Eingaben [mit dem Stift](erasing-ink-with-the-pen.md). Außerdem wird im [Beispiel](ink-erasing-sample.md) frei Hand Löschung veranschaulicht, wie die Rückseite des Stifts verwendet wird, um frei Hand Eingaben zu löschen.

 

 



