---
title: Übersetzen in Visual Basic
description: Übersetzen in Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9aa8a163141c6361df464a22ce873770c8385607bdf8f84d333d204c55a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550614"
---
# <a name="translating-to-visual-basic"></a>Übersetzen in Visual Basic

Sie können ihrem Projekt ein COM-Objekt Visual Basic entweder als Verweis oder als Komponente hinzufügen. Sobald das Objekt ihrem Projekt hinzugefügt wurde, kann Ihre Anwendung auf ihre Klassen und Schnittstellen zugreifen. Anschließend können Sie den Visual Basic Objektbrowser verwenden, um die Typbibliotheksinformationen des Objekts in der Visual Basic anzeigen.

In der Regel werden Einem Projekt Steuerelemente als Komponenten und Nicht-Steuerelemente als Verweise hinzugefügt. Wenn ein COM-Objekt als Komponente hinzugefügt wird, wird es in der Toolbox Visual Basic angezeigt. Neue Instanzen dieses Objekts werden erstellt, indem das Objektsymbol aus der Toolbox auf Visual Basic formular oder einen anderen Containertyp gezogen wird. Neue Instanzen von COM-Objekten, die als Verweise hinzugefügt werden, werden mit dem **schlüsselwort new** erstellt.

Der Unterschied zwischen der Verwendung einer Klasse als Verweis und einer Komponente ist dezent, aber wichtig. Wenn Sie ein -Objekt als Verweis hinzufügen, können Sie nur die vom Steuerelement zur Verfügung stellt, oder die "rohe" Typbibliothek verwenden.

Wenn Sie ein Steuerelement als Komponente hinzufügen, führt Visual Basic die Extendereigenschaften und -methoden des Formulars, in das das Steuerelement eingebettet ist, mit der Typbibliothek des Steuerelements zusammen und stellt somit eine umschlossene, erweiterte Version der Typbibliothek zur Verfügung. Mit dieser Version der Typbibliothek können Sie Extendereigenschaften wie Top und Left verwenden, als ob sie Teil des Steuerelements und nicht des Containers des Steuerelements sind.

Visual Basic unterstützt derzeit nicht mehrere Typbibliotheken, die in eine einzelne .dll sind. Wenn Sie auf eine DLL mit mehreren Typbibliotheken laufen, sollten Sie eigenständige Kopien der Typbibliotheken aus der Quelle erhalten, die das Objekt bereitgestellt hat, um das -Objekt mit der Visual Basic.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Übersetzen in Visual Basic C++](translating-to-visual-basic-from-c--.md)
-   [Übersetzen in Visual Basic aus Java](translating-to-visual-basic-from-java.md)
-   [Hinzufügen einer Komponente zu Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
-   [Hinzufügen eines Verweises auf Visual Basic Project](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic Objektbrowser](visual-basic-object-browser.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in C++](translating-to-c--.md)
</dt> <dt>

[Übersetzen in Java](translating-to-java.md)
</dt> </dl>

 

 




