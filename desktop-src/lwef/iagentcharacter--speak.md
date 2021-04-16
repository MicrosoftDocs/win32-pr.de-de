---
title: Iagentcharacter sprechen
description: Iagentcharacter sprechen
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e290ab9037ee6f261445d4dfd00a206213cd26
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516769"
---
# <a name="iagentcharacterspeak"></a>Iagentcharacter:: sprechen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

Spricht den Text oder die Audiodatei.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bsztext*
</dt> <dd>

Der Text, in dem das Zeichen gesprochen werden soll.

</dd> <dt>

<span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszurl*
</dt> <dd>

Die URL (oder Datei Spezifikation) einer Audiodatei, die für die gesprochene Ausgabe verwendet werden soll. Hierbei kann es sich um eine Standard Sounddatei () handeln. WAV) oder linguistisch erweiterte Audiodatei (. Lwv).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, die die [**Sprech**](/windows/desktop/lwef/iagentcharacter--speak) Anforderungs-ID empfängt.

</dd> </dl>

Um diese Methode mit einem Zeichen zu verwenden, das für die Verwendung einer TTS-Engine (Text-to-Speech) konfiguriert ist. Geben Sie einfach den *bsztext* -Parameter an. Sie können vertikale Balken Zeichen ( \| ) in den *bsztext* -Parameter einschließen, um alternative Zeichen folgen festzulegen, sodass jedes Mal, wenn der Server die Methode verarbeitet, nach dem Zufallsprinzip eine andere Zeichenfolge ausgewählt wird. Die Unterstützung der TTS-Ausgabe wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.

Wenn Sie die Ausgabe der Audiodatei für das Zeichen verwenden möchten, geben Sie den Speicherort für die Datei im Parameter *bszurl* an. Wenn Sie das HTTP-Protokoll verwenden, um eine Audiodatei herunterzuladen, verwenden Sie die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um die Verfügbarkeit der Datei vor der Verwendung dieser Methode sicherzustellen. Sie können den *bsztext* -Parameter verwenden, um die Wörter anzugeben, die in der Wort Sprechblase des Zeichens angezeigt werden. Wenn Sie eine linguistisch erweiterte Audiodatei () angeben. Lwv) für den *bszurl* -Parameter und keinen Text angeben, verwendet der *bsztext* -Parameter den in der Datei gespeicherten Text.

Die [**Sprech Methode verwendet die zuletzt**](/windows/desktop/lwef/iagentcharacter--speak) ausgespielte Animation, um zu bestimmen, welche sprechende Animation abgespielt werden soll. Wenn Sie dem " **sprechen** "-Befehl beispielsweise ein [**iagentcharacter**](iagentcharacter--play.md) -Element vorangestellt haben::P Lay "**gestureright**", wird der Server " **gestureright** " und dann die **gestureright** -Animation durch gesprochen. Wenn die letzte Animation keine sprach Animation enthält, gibt der Microsoft-Agent die Animation wieder, die dem **Sprech** Zustand des Zeichens zugewiesen ist.

Wenn Sie " [**sprechen**](/windows/desktop/lwef/iagentcharacter--speak) " aufrufen und der Audiokanal ausgelastet ist, wird die Audioausgabe des Zeichens nicht gehört, aber der Text wird in der Wort Sprechblase angezeigt. Die [aktivierte](enabled-property.md) -Eigenschaft der Word-Sprechblase muss auch **true** sein, damit der Text angezeigt wird.

Das automatische Wörter brechen des Microsoft-Agents in der Word-Sprechblase, unterbricht Wörter mit Leerzeichen (z. b. Leerzeichen und Registerkarten). Es kann jedoch sein, dass ein Wort auch an die Sprechblase angepasst wird. Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Abbrechen von Wörtern verwendet werden, ein Unicode-Zeichen mit 0 (null) Zeichen (0x200b) zwischen Zeichen ein, um logische Wort Umbrüche zu definieren.

> [!Note]  
> Legen Sie die Sprach-ID des Zeichens (mit [**iagentcharakteriex:: setlanguageid**](iagentcharacterex--setlanguageid.md) ) fest, bevor Sie die Sprech Methode verwenden, um die entsprechende Textanzeige innerhalb der Word- [**Sprech**](/windows/desktop/lwef/iagentcharacter--speak) Blase sicherzustellen.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter::P Lay**](iagentcharacter--play.md), [**iagentballoon:: GetEnabled**](iagentballoon--getenabled.md), [**iagentcharacter::P repare**](iagentcharacter--prepare.md)


 

 