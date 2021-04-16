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
# <a name="iagentcharacterspeak"></a><span data-ttu-id="449cb-103">Iagentcharacter:: sprechen</span><span class="sxs-lookup"><span data-stu-id="449cb-103">IAgentCharacter::Speak</span></span>

<span data-ttu-id="449cb-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="449cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="449cb-105">Spricht den Text oder die Audiodatei.</span><span class="sxs-lookup"><span data-stu-id="449cb-105">Speaks the text or sound file.</span></span>

-   <span data-ttu-id="449cb-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="449cb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="449cb-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bsztext*</span><span class="sxs-lookup"><span data-stu-id="449cb-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="449cb-108">Der Text, in dem das Zeichen gesprochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="449cb-108">The text the character is to speak.</span></span>

</dd> <dt>

<span data-ttu-id="449cb-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszurl*</span><span class="sxs-lookup"><span data-stu-id="449cb-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span></span>
</dt> <dd>

<span data-ttu-id="449cb-110">Die URL (oder Datei Spezifikation) einer Audiodatei, die für die gesprochene Ausgabe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="449cb-110">The URL (or file specification) of a sound file to use for spoken output.</span></span> <span data-ttu-id="449cb-111">Hierbei kann es sich um eine Standard Sounddatei () handeln. WAV) oder linguistisch erweiterte Audiodatei (. Lwv).</span><span class="sxs-lookup"><span data-stu-id="449cb-111">This can be a standard sound file (.WAV) or linguistically enhanced sound file (.LWV).</span></span>

</dd> <dt>

<span data-ttu-id="449cb-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="449cb-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="449cb-113">Adresse einer Variablen, die die [**Sprech**](/windows/desktop/lwef/iagentcharacter--speak) Anforderungs-ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="449cb-113">Address of a variable that receives the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="449cb-114">Um diese Methode mit einem Zeichen zu verwenden, das für die Verwendung einer TTS-Engine (Text-to-Speech) konfiguriert ist. Geben Sie einfach den *bsztext* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="449cb-114">To use this method with a character configured to speak using a text-to-speech (TTS) engine; simply provide the *bszText* parameter.</span></span> <span data-ttu-id="449cb-115">Sie können vertikale Balken Zeichen ( \| ) in den *bsztext* -Parameter einschließen, um alternative Zeichen folgen festzulegen, sodass jedes Mal, wenn der Server die Methode verarbeitet, nach dem Zufallsprinzip eine andere Zeichenfolge ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="449cb-115">You can include vertical bar characters (\|) in the *bszText* parameter to designate alternative strings, so that each time the server processes the method, it randomly choose a different string.</span></span> <span data-ttu-id="449cb-116">Die Unterstützung der TTS-Ausgabe wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="449cb-116">Support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="449cb-117">Wenn Sie die Ausgabe der Audiodatei für das Zeichen verwenden möchten, geben Sie den Speicherort für die Datei im Parameter *bszurl* an.</span><span class="sxs-lookup"><span data-stu-id="449cb-117">If you want to use sound file output for the character, specify the location for the file in the *bszURL* parameter.</span></span> <span data-ttu-id="449cb-118">Wenn Sie das HTTP-Protokoll verwenden, um eine Audiodatei herunterzuladen, verwenden Sie die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um die Verfügbarkeit der Datei vor der Verwendung dieser Methode sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="449cb-118">When using the HTTP protocol to download a sound file, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the file before using this method.</span></span> <span data-ttu-id="449cb-119">Sie können den *bsztext* -Parameter verwenden, um die Wörter anzugeben, die in der Wort Sprechblase des Zeichens angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="449cb-119">You can use the *bszText* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="449cb-120">Wenn Sie eine linguistisch erweiterte Audiodatei () angeben. Lwv) für den *bszurl* -Parameter und keinen Text angeben, verwendet der *bsztext* -Parameter den in der Datei gespeicherten Text.</span><span class="sxs-lookup"><span data-stu-id="449cb-120">If you specify a linguistically enhanced sound file (.LWV) for the *bszURL* parameter and do not specify text, the *bszText* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="449cb-121">Die [**Sprech Methode verwendet die zuletzt**](/windows/desktop/lwef/iagentcharacter--speak) ausgespielte Animation, um zu bestimmen, welche sprechende Animation abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="449cb-121">The [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method uses the last animation played to determine which speaking animation to play.</span></span> <span data-ttu-id="449cb-122">Wenn Sie dem " **sprechen** "-Befehl beispielsweise ein [**iagentcharacter**](iagentcharacter--play.md) -Element vorangestellt haben::P Lay "**gestureright**", wird der Server " **gestureright** " und dann die **gestureright** -Animation durch gesprochen.</span><span class="sxs-lookup"><span data-stu-id="449cb-122">For example, if you precede the **Speak** command with an [**IAgentCharacter::Play**](iagentcharacter--play.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="449cb-123">Wenn die letzte Animation keine sprach Animation enthält, gibt der Microsoft-Agent die Animation wieder, die dem **Sprech** Zustand des Zeichens zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="449cb-123">If the last animation played has no speaking animation, then Microsoft Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="449cb-124">Wenn Sie " [**sprechen**](/windows/desktop/lwef/iagentcharacter--speak) " aufrufen und der Audiokanal ausgelastet ist, wird die Audioausgabe des Zeichens nicht gehört, aber der Text wird in der Wort Sprechblase angezeigt.</span><span class="sxs-lookup"><span data-stu-id="449cb-124">If you call [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span> <span data-ttu-id="449cb-125">Die [aktivierte](enabled-property.md) -Eigenschaft der Word-Sprechblase muss auch **true** sein, damit der Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="449cb-125">The word balloon's [Enabled](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="449cb-126">Das automatische Wörter brechen des Microsoft-Agents in der Word-Sprechblase, unterbricht Wörter mit Leerzeichen (z. b. Leerzeichen und Registerkarten).</span><span class="sxs-lookup"><span data-stu-id="449cb-126">Microsoft Agent's automatic word breaking in the word balloon, breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="449cb-127">Es kann jedoch sein, dass ein Wort auch an die Sprechblase angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="449cb-127">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="449cb-128">Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Abbrechen von Wörtern verwendet werden, ein Unicode-Zeichen mit 0 (null) Zeichen (0x200b) zwischen Zeichen ein, um logische Wort Umbrüche zu definieren.</span><span class="sxs-lookup"><span data-stu-id="449cb-128">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="449cb-129">Legen Sie die Sprach-ID des Zeichens (mit [**iagentcharakteriex:: setlanguageid**](iagentcharacterex--setlanguageid.md) ) fest, bevor Sie die Sprech Methode verwenden, um die entsprechende Textanzeige innerhalb der Word- [**Sprech**](/windows/desktop/lwef/iagentcharacter--speak) Blase sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="449cb-129">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="449cb-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="449cb-130">See Also</span></span>

<span data-ttu-id="449cb-131">[**Iagentcharacter::P Lay**](iagentcharacter--play.md), [**iagentballoon:: GetEnabled**](iagentballoon--getenabled.md), [**iagentcharacter::P repare**](iagentcharacter--prepare.md)</span><span class="sxs-lookup"><span data-stu-id="449cb-131">[**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md)</span></span>


 

 