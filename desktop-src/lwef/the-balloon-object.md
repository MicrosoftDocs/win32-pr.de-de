---
title: Das Balloon-Objekt
description: Das Balloon-Objekt
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc2ad1256b040588121dcb92fc8f66fea540b3051b92a6fe5273eb2f81107b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745972"
---
# <a name="the-balloon-object"></a>Das Balloon-Objekt

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Microsoft Agent unterstützt die Textbeschriftung der [**Speak-Methode**](speak-method.md) mithilfe eines Sprechblasenworts. Mit [**der Think-Methode**](think-method.md) können Sie Text ohne Audioausgabe in einem "Gedanken"-Wortsprechblasenformat anzeigen.

Die Standardeinstellungen eines Ersten Wortsprechblasenfensters eines Zeichens werden im Microsoft Agent-Zeichen-Editor definiert und kompiliert. Nach der Ausführung können die Eigenschaften [**Aktiviert und**](enabled-property.md) [**Schriftart**](https://www.bing.com/search?q=**Font**) des Balloons vom Benutzer überschrieben werden. Wenn ein Benutzer die Eigenschaften des Wortsprechblasens ändert, wirken sich diese auf alle Zeichen aus. Sowohl die [**Sprachsprechblasen**](speak-method.md) als auch die [**Think**](think-method.md) Word-Sprechblasen verwenden die gleichen Eigenschafteneinstellungen für die Größe. Sie können über das Balloon-Objekt, das [](/windows/desktop/lwef/the-balloon-object) ein untergeordnetes Objekt des Character-Objekts ist, auf die Eigenschaften für die Wortsprechblase [**eines Zeichens**](/windows/desktop/lwef/the-characters-object) zugreifen.

Das [**Balloon-Objekt**](/windows/desktop/lwef/the-balloon-object) unterstützt die folgenden Eigenschaften:

-   [**Backcolor**](backcolor-property.md)
-   [**BorderColor**](bordercolor-property.md)
-   [**CharsPerLine**](charsperline-property.md)
-   [**Aktiviert**](enabled-property.md)
-   [**FontCharSet**](fontcharset-property.md)
-   [**FontName**](fontname-property-bal.md)
-   [**SchriftFett**](fontbold-property.md)
-   [**FontItalic**](fontitalic-property.md)
-   [**Fontsize**](fontsize-property-bal.md)
-   [**FontStrikeThru**](fontstrikethru-property.md)
-   [**FontUnderline**](fontunderline-property.md)
-   [**ForeColor**](forecolor-property.md)
-   [**NumberOfLines**](numberoflines-property.md)
-   [**Stil**](style-property.md)
-   [**Sichtbar**](visible-property-bal.md)

 

 