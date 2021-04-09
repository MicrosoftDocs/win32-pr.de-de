---
title: Klassen Symbole
description: Das Symbol, das zum Darstellen eines Klassen Objekts verwendet wird, kann im IconPath-Attribut im displaySpecifier-Container angegeben werden.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- Klassen Anzeige Namen AD, Symbole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691d4ef22babeded12ec9b951f92247df99521b6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948588"
---
# <a name="class-icons"></a>Klassen Symbole

Das Symbol, das zum Darstellen eines Klassen Objekts verwendet wird, kann im **IconPath** -Attribut im displaySpecifier-Container angegeben werden. Darüber hinaus kann jede Klasse mehrere Symbol Zustände speichern. Beispielsweise kann eine Ordner Klasse Symbole für den Status "geöffnet", "geschlossen" und "deaktiviert" aufweisen. Die aktuelle Implementierung akzeptiert maximal sechzehn verschiedene Symbol Zustände pro Klasse.

Das **IconPath** -Attribut kann auf zwei Arten angegeben werden.


```C++
<state>,<icon file name>
```



oder


```C++
<state>,<module file name>,<resource ID>
```



In diesen Beispielen &lt; ist "State &gt; " eine ganze Zahl mit einem Wert zwischen 0 und 15. Der Wert 0 wird als Standard-oder Closed-Zustand des Symbols definiert. Der Wert 1 wird als offener Zustand des Symbols definiert. Der Wert 2 ist der deaktivierte Zustand. Alle anderen Werte sind Anwendungs definiert.

Der Name der Symbol &lt; Datei &gt; ist der Pfad und Dateiname einer Symbol Datei, die das Symbolbild enthält.

Der " &lt; Modul Dateiname &gt; " ist der Pfad und Dateiname eines Moduls, z. b. eine exe-oder DLL-Datei, die das Symbolbild in einer Ressource enthält. Die " &lt; Ressourcen-ID &gt; " ist eine ganze Zahl, die den Ressourcen Bezeichner der Symbol Ressource im Modul angibt.

## <a name="adding-a-value-to-the-iconpath-attribute"></a>Hinzufügen eines Werts zum **IconPath** -Attribut

Um dem **IconPath** -Attribut einen Wert hinzuzufügen, führen Sie die folgenden Schritte aus.

1.  Stellen Sie fest, ob der Wert für das Attribut vorhanden ist. Wenn ein Wert ersetzt werden soll, löschen Sie zuerst den vorhandenen Wert mithilfe der [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode, wobei der Parameter *lncontrolcode* auf **ADS \_ Property \_ Delete** und der *vprop* -Parameter auf den zu entfernenden Wert festgelegt ist. Verwenden Sie nicht die **ADS- \_ Eigenschaft \_ Clear** oder **ADS \_ Property \_ Update** für *lncontrolcode*.
2.  Erstellen Sie die Zeichenfolge, die die Attribut Symbol Daten darstellt. Ein Beispiel finden Sie im obigen Format.
3.  Wenn Sie den neuen Wert hinzufügen möchten, verwenden Sie die [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode, wobei der *lncontrolcode* -Parameter auf **ADS- \_ Eigenschaft \_ Append** festgelegt ist.
4.  Um die Änderungen im Verzeichnis zu übertragen, nennen Sie [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 