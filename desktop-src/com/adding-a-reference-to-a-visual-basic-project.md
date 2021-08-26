---
title: Hinzufügen eines Verweises zu einem Visual Basic Project
description: Hinzufügen eines Verweises zu einem Visual Basic Project
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deba6030e57839e0f436239790aaa6f02e2fb29981ce021b0de2d09af2acdff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097070"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Hinzufügen eines Verweises zu einem Visual Basic Project

Im folgenden Verfahren wird beschrieben, wie sie einem Visual Basic Projekt einen Verweis auf ein COM-Objekt hinzufügen. Ihre Anwendung kann dann die Klassen dieses Objekts verwenden.

Wenn Sie ein Objekt als Verweis hinzufügen, können Sie nur die vom Steuerelement bereitgestellte Typbibliothek oder die "unformatierte" Typbibliothek verwenden. Im Gegensatz dazu macht das Hinzufügen eines Steuerelements als Komponente auch die Visual Basic Extendereigenschaften und -methoden verfügbar, als wären sie Teil des Steuerelements.

**So erstellen Sie einen Visual Basic Verweis auf eine Komponente**

1.  Klicken Sie im Menü **Projekt** auf **Verweise**.
2.  Klicken Sie auf diese Option, um das Kontrollkästchen neben der Komponente zu aktivieren, die Sie hinzufügen möchten. Wenn die Komponente nicht aufgeführt ist, suchen Sie die .dll- oder OCX-Datei mit **durchsuchen.**
3.  Klicken Sie auf **OK**.

Die Komponente ist jetzt Teil des Projekts. Ihre Anwendung kann Klasseninstanzen mithilfe des **Schlüsselworts New** erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen einer Komponente zu einem Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Übersetzen in Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




