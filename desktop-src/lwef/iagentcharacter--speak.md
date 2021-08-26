---
title: IAgentCharacter Speak
description: IAgentCharacter Speak
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693b40a00b34173976410391249d3fac1a7f0684e34a6e2ae82afbd8b8169ce0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014210"
---
# <a name="iagentcharacterspeak"></a>IAgentCharacter::Speak

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Spricht den Text oder die Sounddatei.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*
</dt> <dd>

Der Text, den das Zeichen sprechen soll.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*
</dt> <dd>

Die URL (oder Dateispezifikation) einer Sounddatei, die für gesprochene Ausgaben verwendet werden soll. Dabei kann es sich um eine Standard-Sounddatei (. WAV) oder linguistisch erweiterte Sounddatei (. LWV).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die [**Speak-Anforderungs-ID**](/windows/desktop/lwef/iagentcharacter--speak) empfängt.

</dd> </dl>

Um diese Methode mit einem Zeichen zu verwenden, das für die Spracherkennung mithilfe einer TTS-Engine (Text-to-Speech) konfiguriert ist; geben Sie einfach den *bszText-Parameter* an. Sie können vertikale Balkenzeichen ( ) in den \| *bszText-Parameter* integrieren, um alternative Zeichenfolgen zu bestimmen, sodass bei jeder Serverprozessierung der Methode nach dem Zufallsprinzip eine andere Zeichenfolge ausgewählt wird. Die Unterstützung der TTS-Ausgabe wird definiert, wenn das Zeichen mit dem Microsoft Agent-Zeichen-Editor kompiliert wird.

Wenn Sie die Sounddateiausgabe für das Zeichen verwenden möchten, geben Sie den Speicherort für die Datei im *bszURL-Parameter* an. Wenn Sie das HTTP-Protokoll zum Herunterladen [](/windows/desktop/lwef/iagentcharacter--prepare) einer Sounddatei verwenden, verwenden Sie die Prepare-Methode, um die Verfügbarkeit der Datei sicherzustellen, bevor Sie diese Methode verwenden. Sie können den *bszText-Parameter* verwenden, um die Wörter anzugeben, die im Wortsprechblasen des Zeichens angezeigt werden. Wenn Sie eine linguistisch erweiterte Sounddatei angeben (. LWV) für den *bszURL-Parameter,* und geben Sie keinen Text an. Der *bszText-Parameter* verwendet den in der Datei gespeicherten Text.

Die [**Speak-Methode**](/windows/desktop/lwef/iagentcharacter--speak) verwendet die zuletzt abgespielte Animation, um zu bestimmen, welche Sprechanimation abgespielt werden soll. Wenn Sie beispielsweise dem **Speak-Befehl** eine [**IAgentCharacter::P lay**](iagentcharacter--play.md) "**GestureRight**" vorangehenden, gibt der Server **GestureRight** und dann die **GestureRight-Sprechanimation** wieder. Wenn die zuletzt gezeigte Animation keine Sprechanimation auf hat, gibt Microsoft Agent die Animation wieder, die dem Sprechzustand des **Zeichens zugewiesen** ist.

Wenn Sie [**Speak aufrufen**](/windows/desktop/lwef/iagentcharacter--speak) und der Audiokanal ausgelastet ist, wird die Audioausgabe des Zeichens nicht gehört, aber der Text wird im Wortsprechblasen angezeigt. Die Enabled-Eigenschaft [des](enabled-property.md) Wortsprechblasens muss auch **True sein,** damit der Text angezeigt wird.

Der automatische Wortumbruch von Microsoft Agent in der Wörtersprechblase unterbricht Wörter mitHilfe von Leerzeichen (z. B. Leerzeichen und Tabulator). Es kann jedoch auch ein Wort zum Einpassen in den Sprechblasen geben. Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Aufbrechen von Wörtern verwendet werden, ein Unicode-Leerzeichen mit einer Breite von null (0x200B) zwischen Zeichen ein, um logische Wörterumbrüche zu definieren.

> [!Note]  
> Legen Sie die Sprach-ID des Zeichens fest [**(mithilfe von IAgentCharacterEx::SetLanguageID,**](iagentcharacterex--setlanguageid.md) bevor Sie die [**Speak-Methode**](/windows/desktop/lwef/iagentcharacter--speak) verwenden, um eine entsprechende Textanzeige innerhalb des Wortsprechblasens sicherzustellen.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::P lay**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md)


 

 