---
title: Übersetzen in Visual Basic
description: Übersetzen in Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856400"
---
# <a name="translating-to-visual-basic"></a>Übersetzen in Visual Basic

Sie können Ihrem Visual Basic Projekt ein COM-Objekt als Verweis oder Komponente hinzufügen. Nachdem das Objekt dem Projekt hinzugefügt wurde, kann die Anwendung auf die Klassen und Schnittstellen zugreifen. Sie können dann die Visual Basic Objektkatalog verwenden, um die Typbibliotheks Informationen des Objekts in Visual Basic Syntax anzuzeigen.

Normalerweise werden Steuerelemente zu einem Projekt hinzugefügt, da eine Komponente und nicht-Steuerelemente als Verweise hinzugefügt werden. Wenn ein COM-Objekt als Komponente hinzugefügt wird, wird es in der Visual Basic Toolbox angezeigt. Neue Instanzen dieses Objekts werden erstellt, indem das Objekt Symbol aus der Toolbox auf ein Visual Basic Formular oder einen anderen Containertyp gezogen wird. Neue Instanzen von COM-Objekten, die als Verweise hinzugefügt werden, werden mithilfe des Schlüssel Worts **New** erstellt.

Der Unterschied zwischen der Verwendung einer Klasse als Verweis im Vergleich zu einer Komponente ist sehr gering, aber wichtig. Wenn Sie ein Objekt als Verweis hinzufügen, können Sie nur die Typbibliothek verwenden, die das Steuerelement bereitstellt, oder die Typbibliothek "RAW".

Wenn Sie ein-Steuerelement als Komponente hinzufügen Visual Basic werden die Extendereigenschaften und-Methoden der Form, in der das Steuerelement mit der Typbibliothek des Steuer Elements eingebettet ist, zusammengeführt und somit eine umschließende erweiterte Version der Typbibliothek bereitgestellt. Mit dieser Version der Typbibliothek können Sie Extender-Eigenschaften wie z. b. Top und Left verwenden, als wären Sie Teil des-Steuer Elements, anstatt den Container des Steuer Elements.

Visual Basic unterstützt derzeit nicht mehrere Typbibliotheken, die in eine einzelne DLL-Datei integriert sind. Wenn Sie eine DLL-Datei ausführen, die mehrere Typbibliotheken umfasst, sollten Sie eigenständige Kopien der Typbibliotheken von der Quelle erhalten, von der das Objekt bereitgestellt wurde, um das Objekt mit Visual Basic zu verwenden.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Übersetzen in Visual Basic von C++](translating-to-visual-basic-from-c--.md)
-   [Übersetzen in Visual Basic aus Java](translating-to-visual-basic-from-java.md)
-   [Hinzufügen einer Komponente zu einem Visual Basic Projekt](adding-a-component-to-a-visual-basic-project.md)
-   [Hinzufügen eines Verweises auf ein Visual Basic Projekt](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic Objektkatalog](visual-basic-object-browser.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersetzen in C++](translating-to-c--.md)
</dt> <dt>

[Übersetzen in Java](translating-to-java.md)
</dt> </dl>

 

 




