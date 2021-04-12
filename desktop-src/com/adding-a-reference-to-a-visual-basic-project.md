---
title: Hinzufügen eines Verweises auf ein Visual Basic Projekt
description: Hinzufügen eines Verweises auf ein Visual Basic Projekt
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309732"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Hinzufügen eines Verweises auf ein Visual Basic Projekt

Im folgenden Verfahren wird beschrieben, wie einem Visual Basic Projekt ein Verweis auf ein COM-Objekt hinzugefügt wird. Die Anwendung kann dann die Klassen dieses Objekts verwenden.

Wenn Sie ein Objekt als Verweis hinzufügen, können Sie nur die Typbibliothek verwenden, die vom Steuerelement bereitgestellt wird, oder die Typbibliothek "RAW". Im Gegensatz dazu macht das Hinzufügen eines-Steuer Elements als Komponente auch die Visual Basic Extender-Eigenschaften und-Methoden verfügbar, als wären Sie Teil des-Steuer Elements.

**So erstellen Sie einen Visual Basic Verweis auf eine Komponente**

1.  Klicken Sie im Menü **Projekt** auf **Verweise**.
2.  Aktivieren Sie das Kontrollkästchen neben der Komponente, die Sie hinzufügen möchten. Wenn die Komponente nicht aufgelistet ist, suchen Sie die dll-oder OCX-Datei mithilfe von **Durchsuchen**.
3.  Klicken Sie auf **OK**.

Die Komponente ist nun Teil des Projekts. Die Anwendung kann mit dem **New** -Schlüsselwort Klassen Instanzen erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen einer Komponente zu einem Visual Basic Projekt](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Übersetzen in Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




