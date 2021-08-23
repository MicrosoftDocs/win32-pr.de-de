---
title: IAgentCharacterEx Think
description: IAgentCharacterEx Think
ms.assetid: 64bfa388-0db7-423c-a4af-64a9f7351e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a513a070104605df0cf3e0e722852a2b68d5845f4bcdb1ef6073954b3f9a18c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105438"
---
# <a name="iagentcharacterexthink"></a>IAgentCharacterEx::Think

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Think(
   BSTR bszText,    // text to think
   long * pdwReqID  // address of a request ID
);
```

Zeigt den Sprechblasen des Gedankenworts des Zeichens mit dem angegebenen Text an.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Der Text, der im Gedankensprechblasen des Zeichens angezeigt werden soll.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die Anforderungs-ID von **Think** empfängt.

</dd> </dl>

Wie die [**IAgentCharacter::Speak-Methode**](iagentcharacter--speak.md) ist die **Think-Methode** eine Anforderung in der Warteschlange, die Text in einem Wortsprechblasen anzeigt, mit der Ausnahme, dass Gedanken in einem speziellen Sprechblasen angezeigt werden. Der Thought Balloon unterstützt nur das Lesezeichen-Sprachsteuerelementtag (**\\ Mrk**) und ignoriert alle anderen Sprachsteuerungstags. Im Gegensatz zu **IAgentCharacter::Speak** ändert die **Think-Methode** den Animationszustand des Zeichens nicht.

Die [**IAgentBalloon-Einstellungen**](/windows/desktop/lwef/iagentballoon) gelten auch für die Darstellungsart des Gedankensprechblasens. Beispielsweise muss die [**Enabled-Eigenschaft**](enabled-property.md) der Sprechblase auch **True** sein, damit der Text angezeigt wird.

Der automatische Wörterumbruch des Microsoft-Agents im Wortsprechblasen unterbricht Wörter mitHilfe von Leerzeichen (z. B. Leerzeichen und Tabstopps). Es kann jedoch auch ein Wort unterbrechen, das an den Sprechblasen passt. Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Unterbrechen von Wörtern verwendet werden, ein Unicode-Leerzeichen mit einer Breite von 0 (0x200B) zwischen Zeichen ein, um logische Wortumbrüche zu definieren.

> [!Note]  
> Legen Sie die Sprach-ID des Zeichens fest (mithilfe von [**IAgentCharacterEx::SetLanguageID,**](iagentcharacterex--setlanguageid.md) bevor Sie die [**IAgentCharacter::Speak-Methode**](iagentcharacter--speak.md) verwenden, um die entsprechende Textanzeige innerhalb der Wortsprechblase sicherzustellen.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md)


 

 