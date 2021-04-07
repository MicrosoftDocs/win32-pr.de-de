---
title: Iagentcharakteriex-Ansicht
description: Iagentcharakteriex-Ansicht
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd1bedfc2665c80d522ccb38c7c3073580136db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038894"
---
# <a name="iagentcharacterexthink"></a>Iagentcharakteriex:: Think

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

Zeigt die gedachte Word-Sprechblase des Zeichens mit dem angegebenen Text an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bsztext*
</dt> <dd>

Der Text, der in der Gedanken Sprechblase des Zeichens angezeigt werden soll.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen **, die die Anforderungs Anforderungs** -ID empfängt.

</dd> </dl>

Wie die [**iagentcharacter:: Speak**](iagentcharacter--speak.md) -Methode ist die Methode " **Think** " eine Anforderung in der Warteschlange, die Text in einer Wort Sprechblase anzeigt, mit dem Unterschied, dass die Gedanken in einer speziellen Sprechblase angezeigt werden Die Sprechblase unterstützt nur das Lesezeichen-Steuerelement Tag (**\\ MRK**) und ignoriert alle anderen sprachkontrolltags. Anders als bei **iagentcharacter:: Speak** ändert die " **Think** "-Methode nicht den Animations Zustand des Zeichens.

Die [**iagentballoon**](/windows/desktop/lwef/iagentballoon) -Einstellungen gelten auch für den Darstellungsstil der Gedanken Sprechblase. Beispielsweise muss die [**aktivierte**](enabled-property.md) Eigenschaft der Sprechblase auch **true** sein, damit der Text angezeigt wird.

Das automatische Wörter brechen des Microsoft-Agents in der Word-Sprechblase unterbricht Wörter mit Leerzeichen (z. b. Leerzeichen und Tab). Es kann jedoch sein, dass ein Wort auch an die Sprechblase angepasst wird. Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Abbrechen von Wörtern verwendet werden, ein Unicode-Zeichen mit 0 (null) Zeichen (0x200b) zwischen Zeichen ein, um logische Wort Umbrüche zu definieren.

> [!Note]  
> Legen Sie die Sprach-ID des Zeichens (mit [**iagentcharakteriex:: setlanguageid**](iagentcharacterex--setlanguageid.md) ) fest, bevor Sie die [**iagentcharacter:: Speak**](iagentcharacter--speak.md) -Methode verwenden, um die entsprechende Textanzeige innerhalb der Word-Sprechblase sicherzustellen.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: GetEnabled**](iagentballoon--getenabled.md), [**iagentballoonex:: SetStyle**](iagentballoonex--setstyle.md), [**iagentcharacter:: Speak**](iagentcharacter--speak.md)


 

 