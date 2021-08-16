---
title: Klassensymbole
description: Das Symbol, das zum Darstellen eines Klassenobjekts verwendet wird, kann im IconPath-Attribut im DisplaySpecifiers-Container angegeben werden.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- Klassenanzeigenamen AD , Symbole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe3548daa223cdfa05dee8ec3df8f2f8bc800c5ba7449920744de1a67ac8745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022601"
---
# <a name="class-icons"></a>Klassensymbole

Das Symbol, das zum Darstellen eines Klassenobjekts verwendet wird, kann im **IconPath-Attribut** im DisplaySpecifiers-Container angegeben werden. Darüber hinaus kann jede Klasse mehrere Symbolzustände speichern. Eine Ordnerklasse kann z. B. Symbole für den geöffneten, geschlossenen und deaktivierten Zustände enthalten. Die aktuelle Implementierung akzeptiert maximal 16 verschiedene Symbolzustände pro Klasse.

Das **iconPath-Attribut** kann auf zwei Arten angegeben werden.


```C++
<state>,<icon file name>
```



oder


```C++
<state>,<module file name>,<resource ID>
```



In diesen Beispielen ist der Zustand &lt; &gt; "" eine ganze Zahl mit einem Wert zwischen 0 und 15. Der Wert 0 ist als Standard- oder Geschlossenzustand des Symbols definiert. Der Wert 1 ist als der Offene Zustand des Symbols definiert. Der Wert 2 ist der deaktivierte Zustand. Alle anderen Werte sind anwendungsdefiniert.

Der &lt; Symboldateiname ist der Pfad und Dateiname einer &gt; Symboldatei, die das Symbolbild enthält.

Der Moduldateiname ist der Pfad und Dateiname eines Moduls, z. B. einer EXE- oder DLL-Datei, das das &lt; &gt; Symbolbild in einer Ressource enthält. Die &lt; Ressourcen-ID &gt; ist eine ganze Zahl, die den Ressourcenbezeichner der Symbolressource innerhalb des Moduls angibt.

## <a name="adding-a-value-to-the-iconpath-attribute"></a>Hinzufügen eines Werts zum **iconPath-Attribut**

Um dem **iconPath-Attribut** einen Wert hinzuzufügen, führen Sie die folgenden Schritte aus.

1.  Bestimmen Sie, ob der Wert für das Attribut vorhanden ist. Wenn ein Wert ersetzt werden soll, löschen Sie zunächst den vorhandenen Wert mithilfe der [**IADs::P utEx-Methode,**](/windows/desktop/api/iads/nf-iads-iads-putex) bei der der *Parameter lnControlCode* auf **ADS PROPERTY \_ \_ DELETE** und der *vProp-Parameter* auf den zu entfernenden Wert festgelegt ist. Verwenden Sie **nicht ADS PROPERTY CLEAR \_ \_ oder** **ADS PROPERTY \_ \_ UPDATE** für *lnControlCode*.
2.  Erstellen Sie die Zeichenfolge, die die Attributsymboldaten darstellt. Ein Beispiel finden Sie im obigen Format.
3.  Verwenden Sie zum Hinzufügen des neuen Werts die [**IADs::P utEx-Methode,**](/windows/desktop/api/iads/nf-iads-iads-putex) und legen Sie den *Parameter lnControlCode* auf **ADS PROPERTY APPEND \_ \_ fest.**
4.  Rufen Sie zum Commit von Änderungen im Verzeichnis [**IADs::SetInfo auf.**](/windows/desktop/api/iads/nf-iads-iads-setinfo)

 

 