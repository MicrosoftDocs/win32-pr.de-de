---
description: Ein Tablet PC-Stift kann mehrere Enden haben, die mit dem Digitizer interagieren können.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Mehrere Funktionen mit einem Stift
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cbba4c95ef215b8ae1e0c94cbe1d43eaceb966fd775284c57a365bbba2f7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449671"
---
# <a name="multiple-functionality-with-one-pen"></a>Mehrere Funktionen mit einem Stift

Ein Tablet PC-Stift kann mehrere Enden haben, die mit dem Digitizer interagieren können. Wenn beide Enden des Stifts Ereignisse generieren können, kann ein Ende verwendet werden, um die Ink-, Select- und Point-Funktion zu erstellen, und das andere Ende kann für andere Funktionen wie das Löschen verwendet werden.

Um diese Funktionalität zu implementieren, muss Ihre Anwendung bestimmen können, welches Ende des Stifts verwendet wird und wann die Darstellung des Cursors geändert werden soll. Dies kann durch Suchen nach dem Zustand der [**Inverted-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) für das [**Cursor-Objekt der Fall**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) sein.

Spezifische Informationen zur Verwendung der Rückseite des Stifts zum Löschen finden Sie unter Löschen von [Ink mit dem Stift](erasing-ink-with-the-pen.md). Darüber hinaus wird im Beispiel zum Löschen von [Ink Erasing](ink-erasing-sample.md) veranschaulicht, wie die Rückseite des Stifts zum Löschen von Ink verwendet wird.

 

 



