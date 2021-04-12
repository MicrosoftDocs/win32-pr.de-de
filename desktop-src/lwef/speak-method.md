---
title: Sprech Methode
description: Sprech Methode
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88792a53fac80c68154f938e91fb9bfe63b2b8e3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472924"
---
# <a name="speak-method"></a><span data-ttu-id="acd82-103">Sprech Methode</span><span class="sxs-lookup"><span data-stu-id="acd82-103">Speak Method</span></span>

<span data-ttu-id="acd82-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="acd82-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="acd82-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="acd82-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="acd82-106">Gibt den angegebenen Text oder die Audiodatei für das angegebene Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="acd82-106">Speaks the specified text or sound file for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="acd82-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="acd82-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="acd82-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Sprach* \*  \[ *Text* \] , \[ *URL*\]</span><span class="sxs-lookup"><span data-stu-id="acd82-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speak*\* \[*Text*\], \[*Url*\]</span></span>



| <span data-ttu-id="acd82-109">Teil</span><span class="sxs-lookup"><span data-stu-id="acd82-109">Part</span></span>   | <span data-ttu-id="acd82-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="acd82-110">Description</span></span>                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acd82-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="acd82-111">*Text*</span></span> | <span data-ttu-id="acd82-112">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="acd82-112">Optional.</span></span> <span data-ttu-id="acd82-113">Eine Zeichenfolge, die angibt, was das Zeichen heißt.</span><span class="sxs-lookup"><span data-stu-id="acd82-113">A string that specifies what the character says.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="acd82-114">*Url*</span><span class="sxs-lookup"><span data-stu-id="acd82-114">*Url*</span></span>  | <span data-ttu-id="acd82-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="acd82-115">Optional.</span></span> <span data-ttu-id="acd82-116">Ein Zeichen folgen Ausdruck, der den Speicherort einer Audiodatei angibt (. WAV oder. Lwv-Format).</span><span class="sxs-lookup"><span data-stu-id="acd82-116">A string expression specifying the location of an audio file (.WAV or .LWV format).</span></span> <span data-ttu-id="acd82-117">Der Speicherort kann als Datei (einschließlich einer UNC-Pfadspezifikation) oder als URL angegeben werden (wenn auch Zeichen Animationsdaten über das HTTP-Protokoll abgerufen werden).</span><span class="sxs-lookup"><span data-stu-id="acd82-117">The location can be specified as a file (including a UNC path specification) or URL (when character animation data is also being retrieved via HTTP protocol).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acd82-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acd82-118">Remarks</span></span>

<span data-ttu-id="acd82-119">Obwohl die *Text* -und *URL* -Parameter optional sind, muss eine davon angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="acd82-119">Although the *Text* and *Url* parameters are optional, one of them must be supplied.</span></span> <span data-ttu-id="acd82-120">Um diese Methode mit einem Zeichen zu verwenden, das so konfiguriert ist, dass es nur in der Wort Sprechblase oder mithilfe einer TTS-Engine (Text-to-Speech) verwendet wird, geben Sie einfach den *Text* -Parameter</span><span class="sxs-lookup"><span data-stu-id="acd82-120">To use this method with a character configured to speak only in its word balloon or using a text-to-speech (TTS) engine, simply provide the *Text* parameter.</span></span> <span data-ttu-id="acd82-121">Fügen Sie ein Leerzeichen zwischen Wörtern ein, um entsprechende Wort Umbrüche in der Word-Sprechblase zu definieren, auch für Sprachen, die keine Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="acd82-121">Include a space between words to define appropriate word breaks in the word balloon, even for languages that do not traditionally include spaces.</span></span>

<span data-ttu-id="acd82-122">Sie können auch vertikale Balken Zeichen ( \| ) in den *Text* -Parameter einschließen, um alternative Zeichen folgen festzulegen, damit der Server bei jedem verarbeiten der Methode nach dem Zufallsprinzip eine andere Zeichenfolge auswählt.</span><span class="sxs-lookup"><span data-stu-id="acd82-122">You can also include vertical bar characters (\|) in the *Text* parameter to designate alternative strings, so that the server randomly chooses a different string each time it processes the method.</span></span>

<span data-ttu-id="acd82-123">Die Zeichen Unterstützung der TTS-Ausgabe wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="acd82-123">Character support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="acd82-124">Um die TTS-Ausgabe zu generieren, muss bereits eine kompatible TTS-Engine installiert sein, bevor diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="acd82-124">To generate TTS output, a compatible TTS engine must already be installed before calling this method.</span></span> <span data-ttu-id="acd82-125">Weitere Informationen finden Sie unter [zugreifen auf Sprachdienste](accessing-speech-services.md).</span><span class="sxs-lookup"><span data-stu-id="acd82-125">For further information, see [Accessing Speech Services](accessing-speech-services.md).</span></span>

<span data-ttu-id="acd82-126">Wenn Sie die aufgezeichnete Sounddatei verwenden (. WAV oder. Nur lwv-Format) Ausgabe für das Zeichen geben Sie den Speicherort der Datei im *URL* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="acd82-126">If you use recorded sound-file (.WAV or .LWV format only) output for the character, specify the file's location in the *Url* parameter.</span></span> <span data-ttu-id="acd82-127">Diese Datei Spezifikation kann einen lokalen (absoluten oder relativen) oder UNC-Pfad (Universal Naming Convention) enthalten.</span><span class="sxs-lookup"><span data-stu-id="acd82-127">This file specification can include a local (absolute or relative) or universal naming convention (UNC) path.</span></span> <span data-ttu-id="acd82-128">Der Dateiname darf keine Zeichen enthalten, die nicht in der US-Codepage 1252 enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="acd82-128">The filename cannot include any characters not included in the US code page 1252.</span></span> <span data-ttu-id="acd82-129">Wenn Sie jedoch das HTTP-Protokoll verwenden, um auf die Daten der Zeichen Animation zuzugreifen, verwenden Sie die [**Get**](get-method.md) -Methode, um die Animation zu laden, bevor Sie die **Sprech** Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="acd82-129">However, if you are using the HTTP protocol to access the character animation data, use the [**Get**](get-method.md) method to load the animation before calling the **Speak** method.</span></span> <span data-ttu-id="acd82-130">Weitere Informationen zu Creative finden [Sie unter Verwenden des Microsoft-Tools zur sprach Sound Bearbeitung](using-the-microsoft-linguistic-information-sound-editing-tool.md) . Lwv-Dateien.</span><span class="sxs-lookup"><span data-stu-id="acd82-130">See [Using the Microsoft Linguistic Information Sound Editing Tool](using-the-microsoft-linguistic-information-sound-editing-tool.md) for information about creative .LWV files.</span></span>

<span data-ttu-id="acd82-131">Wenn Sie die aufgezeichnete Sounddatei Ausgabe verwenden, können Sie weiterhin den *Text* -Parameter verwenden, um die Wörter anzugeben, die in der Wort Sprechblase des Zeichens angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="acd82-131">When using recorded sound-file output, you can still use the *Text* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="acd82-132">Wenn Sie jedoch eine linguistisch erweiterte Audiodatei () angeben. Lwv) für den *URL* -Parameter und keinen Text für die Word-Sprechblase angeben, wird *für den Text Parameter der* in der Datei gespeicherte Text verwendet.</span><span class="sxs-lookup"><span data-stu-id="acd82-132">However, if you specify a linguistically enhanced sound file (.LWV) for the *Url* parameter and do not specify text for the word balloon, the *Text* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="acd82-133">Sie können auch die Parameter der Sprachausgabe mit speziellen Tags variieren, die Sie in den *Text* Parameter einschließen.</span><span class="sxs-lookup"><span data-stu-id="acd82-133">You can also vary parameters of the speech output with special tags that you include in the *Text* parameter.</span></span> <span data-ttu-id="acd82-134">Weitere Informationen finden Sie unter [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="acd82-134">For more information, see [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

<span data-ttu-id="acd82-135">Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="acd82-135">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="acd82-136">Damit können Sie andere Teile des Codes mit der gesprochenen Ausgabe des Zeichens synchronisieren, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="acd82-136">You can use this to synchronize other parts of your code with the character's spoken output, as in the following example:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



<span data-ttu-id="acd82-137">Sie können auch ein [**Request**](/windows/desktop/lwef/the-request-object) -Objekt verwenden, um bestimmte Fehlerbedingungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="acd82-137">You can also use a [**Request**](/windows/desktop/lwef/the-request-object) object to check for certain error conditions.</span></span> <span data-ttu-id="acd82-138">Wenn Sie z. b. die **Sprech** Methode verwenden, um zu sprechen und keine kompatible TTS-Engine zu installieren, legt der Server die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) fest, wobei die [**Description**](description-property.md) -Eigenschaft auf "Class Not Registered" oder "unknown or Object gab Error" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="acd82-138">For example, if you use the **Speak** method to speak and do not have a compatible TTS engine installed, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with its [**Description**](description-property.md) property to "Class not registered" or "Unknown or object returned error".</span></span> <span data-ttu-id="acd82-139">Um zu ermitteln, ob Sie eine TTS-Engine installiert haben, verwenden Sie die [**ttsmodeid**](ttsmodeid-property.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="acd82-139">To determine if you have a TTS engine installed, use the [**TTSModeID**](ttsmodeid-property.md) property.</span></span>

<span data-ttu-id="acd82-140">Wenn Sie den Zeichen Versuch haben, eine Audiodatei zu sprechen, und wenn die Datei nicht geladen wurde oder ein Problem mit dem Audiogerät vorliegt, legt der Server auch die [**Status**](status-property.md) -Eigenschaft des [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlercode Nummer fest.</span><span class="sxs-lookup"><span data-stu-id="acd82-140">Similarly, if you have the character attempt to speak a sound file, and if the file has not been loaded or there is a problem with the audio device, the server also sets the [**Request**](/windows/desktop/lwef/the-request-object) object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="acd82-141">Sie können auch Lesezeichen-Sprech Tags in ihren Sprechtext einschließen, um Ihren Code zu synchronisieren:</span><span class="sxs-lookup"><span data-stu-id="acd82-141">You can also include bookmark speech tags in your Speak text to synchronize your code:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



<span data-ttu-id="acd82-142">Weitere Informationen zum Lesetag für Lesezeichen finden Sie unter [Sprachausgabe Tags](mrk-tag.md).</span><span class="sxs-lookup"><span data-stu-id="acd82-142">For more information on the bookmark speech tag, see [Speech Output Tags](mrk-tag.md).</span></span>

<span data-ttu-id="acd82-143">Die **Sprech Methode verwendet die letzte** wiedergegebene Aktion, um zu bestimmen, welche sprechende Animation abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="acd82-143">The **Speak** method uses the last action played to determine which speaking animation to play.</span></span> <span data-ttu-id="acd82-144">Wenn Sie z. b. den **"sprechen** "-Befehl mit der "**gestureright**"-wieder [**Gabe**](play-method.md) vorangestellt haben, spielt der Server " **gestureright** " und dann die **gestureright** -Animation.</span><span class="sxs-lookup"><span data-stu-id="acd82-144">For example, if you preceded the **Speak** command with a [**Play**](play-method.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="acd82-145">Wenn die letzte Animation keine sprach Animation enthält, gibt der-Agent die Animation wieder, die dem **Sprech** Zustand des Zeichens zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="acd82-145">If the last animation played has no speaking animation, Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="acd82-146">Wenn Sie " **sprechen** " aufrufen und der Audiokanal ausgelastet ist, wird die Audioausgabe des Zeichens nicht gehört, aber der Text wird in der Wort Sprechblase angezeigt.</span><span class="sxs-lookup"><span data-stu-id="acd82-146">If you call **Speak** and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span>

<span data-ttu-id="acd82-147">Die automatische Wörter Trennung des Agents in der Wort Sprechblase unterbricht Wörter mit Leerzeichen (z. b. Leerzeichen oder Tabstopps).</span><span class="sxs-lookup"><span data-stu-id="acd82-147">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="acd82-148">Wenn dies jedoch nicht möglich ist, kann es dazu kommen, dass ein Wort an die Sprechblase angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="acd82-148">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="acd82-149">Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Abbrechen von Wörtern verwendet werden, ein Unicode-Leerzeichen (0x200b) zwischen Zeichen ein, um logische Wort Umbrüche zu definieren.</span><span class="sxs-lookup"><span data-stu-id="acd82-149">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="acd82-150">Die [**aktivierte**](enabled-property.md) Eigenschaft der Word-Sprechblase muss auch **true** sein, damit Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="acd82-150">The word balloon's [**Enabled**](enabled-property.md) property must also be **True** for text to display.</span></span>

 

> [!Note]  
> <span data-ttu-id="acd82-151">Legen Sie die Sprach-ID des Zeichens fest (indem Sie die **LanguageID** des Zeichens festlegen, bevor Sie die Sprech Methode verwenden, um die entsprechende Textanzeige innerhalb der Wort **Sprech** Blase sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="acd82-151">Set the character's language ID (by setting the character's **LanguageID** before using the **Speak** method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="acd82-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="acd82-152">See Also</span></span>

<span data-ttu-id="acd82-153">[**Bookmark-Ereignis**](bookmark-event.md), [**requeststart-Ereignis**](requeststart-event.md), [**requestcomplete-Ereignis**](requestcomplete-event.md)</span><span class="sxs-lookup"><span data-stu-id="acd82-153">[**Bookmark event**](bookmark-event.md), [**RequestStart event**](requeststart-event.md), [**RequestComplete event**](requestcomplete-event.md)</span></span>


 

 