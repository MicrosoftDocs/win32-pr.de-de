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
# <a name="speak-method"></a>Sprech Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den angegebenen Text oder die Audiodatei für das angegebene Zeichen an.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Sprach* *  \[ *Text* \] , \[ *URL*\]



| Teil   | BESCHREIBUNG                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Text* | Dies ist optional. Eine Zeichenfolge, die angibt, was das Zeichen heißt.                                                                                                                                                                                                   |
| *Url*  | Dies ist optional. Ein Zeichen folgen Ausdruck, der den Speicherort einer Audiodatei angibt (. WAV oder. Lwv-Format). Der Speicherort kann als Datei (einschließlich einer UNC-Pfadspezifikation) oder als URL angegeben werden (wenn auch Zeichen Animationsdaten über das HTTP-Protokoll abgerufen werden). |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Obwohl die *Text* -und *URL* -Parameter optional sind, muss eine davon angegeben werden. Um diese Methode mit einem Zeichen zu verwenden, das so konfiguriert ist, dass es nur in der Wort Sprechblase oder mithilfe einer TTS-Engine (Text-to-Speech) verwendet wird, geben Sie einfach den *Text* -Parameter Fügen Sie ein Leerzeichen zwischen Wörtern ein, um entsprechende Wort Umbrüche in der Word-Sprechblase zu definieren, auch für Sprachen, die keine Leerzeichen enthalten.

Sie können auch vertikale Balken Zeichen ( \| ) in den *Text* -Parameter einschließen, um alternative Zeichen folgen festzulegen, damit der Server bei jedem verarbeiten der Methode nach dem Zufallsprinzip eine andere Zeichenfolge auswählt.

Die Zeichen Unterstützung der TTS-Ausgabe wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird. Um die TTS-Ausgabe zu generieren, muss bereits eine kompatible TTS-Engine installiert sein, bevor diese Methode aufgerufen wird. Weitere Informationen finden Sie unter [zugreifen auf Sprachdienste](accessing-speech-services.md).

Wenn Sie die aufgezeichnete Sounddatei verwenden (. WAV oder. Nur lwv-Format) Ausgabe für das Zeichen geben Sie den Speicherort der Datei im *URL* -Parameter an. Diese Datei Spezifikation kann einen lokalen (absoluten oder relativen) oder UNC-Pfad (Universal Naming Convention) enthalten. Der Dateiname darf keine Zeichen enthalten, die nicht in der US-Codepage 1252 enthalten sind. Wenn Sie jedoch das HTTP-Protokoll verwenden, um auf die Daten der Zeichen Animation zuzugreifen, verwenden Sie die [**Get**](get-method.md) -Methode, um die Animation zu laden, bevor Sie die **Sprech** Methode aufrufen. Weitere Informationen zu Creative finden [Sie unter Verwenden des Microsoft-Tools zur sprach Sound Bearbeitung](using-the-microsoft-linguistic-information-sound-editing-tool.md) . Lwv-Dateien.

Wenn Sie die aufgezeichnete Sounddatei Ausgabe verwenden, können Sie weiterhin den *Text* -Parameter verwenden, um die Wörter anzugeben, die in der Wort Sprechblase des Zeichens angezeigt werden. Wenn Sie jedoch eine linguistisch erweiterte Audiodatei () angeben. Lwv) für den *URL* -Parameter und keinen Text für die Word-Sprechblase angeben, wird *für den Text Parameter der* in der Datei gespeicherte Text verwendet.

Sie können auch die Parameter der Sprachausgabe mit speziellen Tags variieren, die Sie in den *Text* Parameter einschließen. Weitere Informationen finden Sie unter [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).

Wenn Sie einen Objekt Verweis deklarieren und diesen auf diese Methode festlegen, wird ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückgegeben. Damit können Sie andere Teile des Codes mit der gesprochenen Ausgabe des Zeichens synchronisieren, wie im folgenden Beispiel gezeigt:


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



Sie können auch ein [**Request**](/windows/desktop/lwef/the-request-object) -Objekt verwenden, um bestimmte Fehlerbedingungen zu überprüfen. Wenn Sie z. b. die **Sprech** Methode verwenden, um zu sprechen und keine kompatible TTS-Engine zu installieren, legt der Server die [**Status**](status-property.md) -Eigenschaft des **Anforderungs** Objekts auf "failed" (Fehler) fest, wobei die [**Description**](description-property.md) -Eigenschaft auf "Class Not Registered" oder "unknown or Object gab Error" festgelegt ist. Um zu ermitteln, ob Sie eine TTS-Engine installiert haben, verwenden Sie die [**ttsmodeid**](ttsmodeid-property.md) -Eigenschaft.

Wenn Sie den Zeichen Versuch haben, eine Audiodatei zu sprechen, und wenn die Datei nicht geladen wurde oder ein Problem mit dem Audiogerät vorliegt, legt der Server auch die [**Status**](status-property.md) -Eigenschaft des [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts auf "failed" (Fehler) mit einer entsprechenden Fehlercode Nummer fest.

Sie können auch Lesezeichen-Sprech Tags in ihren Sprechtext einschließen, um Ihren Code zu synchronisieren:


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



Weitere Informationen zum Lesetag für Lesezeichen finden Sie unter [Sprachausgabe Tags](mrk-tag.md).

Die **Sprech Methode verwendet die letzte** wiedergegebene Aktion, um zu bestimmen, welche sprechende Animation abgespielt werden soll. Wenn Sie z. b. den **"sprechen** "-Befehl mit der "**gestureright**"-wieder [**Gabe**](play-method.md) vorangestellt haben, spielt der Server " **gestureright** " und dann die **gestureright** -Animation. Wenn die letzte Animation keine sprach Animation enthält, gibt der-Agent die Animation wieder, die dem **Sprech** Zustand des Zeichens zugewiesen ist.

Wenn Sie " **sprechen** " aufrufen und der Audiokanal ausgelastet ist, wird die Audioausgabe des Zeichens nicht gehört, aber der Text wird in der Wort Sprechblase angezeigt.

Die automatische Wörter Trennung des Agents in der Wort Sprechblase unterbricht Wörter mit Leerzeichen (z. b. Leerzeichen oder Tabstopps). Wenn dies jedoch nicht möglich ist, kann es dazu kommen, dass ein Wort an die Sprechblase angepasst wird. Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Abbrechen von Wörtern verwendet werden, ein Unicode-Leerzeichen (0x200b) zwischen Zeichen ein, um logische Wort Umbrüche zu definieren.

> [!Note]  
> Die [**aktivierte**](enabled-property.md) Eigenschaft der Word-Sprechblase muss auch **true** sein, damit Text angezeigt wird.

 

> [!Note]  
> Legen Sie die Sprach-ID des Zeichens fest (indem Sie die **LanguageID** des Zeichens festlegen, bevor Sie die Sprech Methode verwenden, um die entsprechende Textanzeige innerhalb der Wort **Sprech** Blase sicherzustellen.

 

## <a name="see-also"></a>Weitere Informationen

[**Bookmark-Ereignis**](bookmark-event.md), [**requeststart-Ereignis**](requeststart-event.md), [**requestcomplete-Ereignis**](requestcomplete-event.md)


 

 