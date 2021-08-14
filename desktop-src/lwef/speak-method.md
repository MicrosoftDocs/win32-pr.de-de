---
title: Speak-Methode
description: Speak-Methode
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8798809dc4cdfa38438bee2fa9449f879871e4018b0e6b046d95a73583b03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475342"
---
# <a name="speak-method"></a>Speak-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Spricht den angegebenen Text oder die angegebene Sounddatei für das angegebene Zeichen aus.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Text_ *  \[  \] sprechen, \[ *URL*\]



| Teil   | BESCHREIBUNG                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Text* | Optional. Eine Zeichenfolge, die angibt, was das Zeichen sagt.                                                                                                                                                                                                   |
| *Url*  | Optional. Ein Zeichenfolgenausdruck, der den Speicherort einer Audiodatei angibt (. WAV oder . LWV-Format). Der Speicherort kann als Datei (einschließlich UNC-Pfadspezifikation) oder URL (wenn Zeichenanimationsdaten auch über das HTTP-Protokoll abgerufen werden) angegeben werden. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Obwohl die *Parameter Text* und *URL* optional sind, muss einer von ihnen angegeben werden. Um diese Methode mit einem Zeichen zu verwenden, das so konfiguriert ist, dass es nur in seinem Wortsprechblasen oder mithilfe einer TTS-Engine (Text-to-Speech) spricht, geben Sie einfach den *Text-Parameter* an. Schließen Sie ein Leerzeichen zwischen Wörtern ein, um entsprechende Wortumbrüche im Wortsprechblasen zu definieren, auch für Sprachen, die normalerweise keine Leerzeichen enthalten.

Sie können auch vertikale Balkenzeichen \| () in den *Text-Parameter* einschließen, um alternative Zeichenfolgen festzulegen, sodass der Server bei jeder Verarbeitung der Methode nach dem Zufallsprinzip eine andere Zeichenfolge aus wählt.

Die Zeichenunterstützung der TTS-Ausgabe wird definiert, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor kompiliert wird. Um eine TTS-Ausgabe zu generieren, muss bereits eine kompatible TTS-Engine installiert sein, bevor diese Methode aufgerufen wird. Weitere Informationen finden Sie unter [Zugreifen auf Speech-Dienste.](accessing-speech-services.md)

Bei Verwendung der aufgezeichneten Sounddatei (. WAV oder . Nur LWV-Format) ausgabe für das Zeichen, geben Sie den Speicherort der Datei im *Url-Parameter* an. Diese Dateispezifikation kann einen lokalen (absoluten oder relativen) oder UNC-Pfad (Universal Naming Convention) enthalten. Der Dateiname darf keine Zeichen enthalten, die nicht in der US-Codepage 1252 enthalten sind. Wenn Sie jedoch das HTTP-Protokoll verwenden, um auf die Zeichenanimationsdaten zuzugreifen, verwenden [**Sie**](get-method.md) die Get-Methode, um die Animation zu laden, bevor Sie die **Speak-Methode** aufrufen. Informationen zu creative finden Sie unter [Using the Microsoft Linguistic Information Sound Editing Tool (Verwenden des Microsoft Linguistic Information Sound Editing Tools).](using-the-microsoft-linguistic-information-sound-editing-tool.md) LWV-Dateien.

Bei Verwendung der aufgezeichneten Audiodateiausgabe können Sie weiterhin den *Text-Parameter* verwenden, um die Wörter anzugeben, die im Wortsprechblasen des Zeichens angezeigt werden. Wenn Sie jedoch eine linguistisch erweiterte Sounddatei angeben (. LWV) für den *Url-Parameter* und geben keinen Text für die Wortsprechblase an. Der *Text-Parameter* verwendet den in der Datei gespeicherten Text.

Sie können auch Parameter der Sprachausgabe mit speziellen Tags variieren, die Sie in den *Text-Parameter* einschließen. Weitere Informationen finden Sie unter [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).

Wenn Sie einen Objektverweis deklarieren und auf diese Methode festlegen, wird ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurückgegeben. Sie können dies verwenden, um andere Teile des Codes mit der gesprochenen Ausgabe des Zeichens zu synchronisieren, wie im folgenden Beispiel zu sehen:


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



Sie können auch ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) verwenden, um bestimmte Fehlerbedingungen zu überprüfen. Wenn Sie beispielsweise die **Speak-Methode** verwenden, um zu sprechen, und keine kompatible TTS-Engine installiert ist, legt der Server die [**Status-Eigenschaft**](status-property.md) des **Request-Objekts** auf "failed" mit der [**Description-Eigenschaft**](description-property.md) auf "Class not registered" oder "Unknown or object returned error" fest. Verwenden Sie die [**TTSModeID-Eigenschaft,**](ttsmodeid-property.md) um zu ermitteln, ob eine TTS-Engine installiert ist.

Wenn Sie mit dem Zeichen versuchen, eine Sounddatei zu sprechen, und wenn die Datei nicht geladen wurde oder ein Problem mit dem Audiogerät vorliegt, legt der Server auch die [**Status-Eigenschaft**](status-property.md) des [**Request-Objekts**](/windows/desktop/lwef/the-request-object) auf "failed" mit einer entsprechenden Fehlercodenummer fest.

Sie können auch Lesezeichen-Sprachtags in Ihren Sprachtext einschließen, um Ihren Code zu synchronisieren:


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



Weitere Informationen zum Lesezeichen-Sprachtag finden Sie unter [Speech-Ausgabetags.](mrk-tag.md)

Die **Speak-Methode** verwendet die letzte wiedergegebene Aktion, um zu bestimmen, welche Sprechanimation wiedergegeben werden soll. Wenn Sie z. B. dem Befehl **Speak** einen **"GestureRight"** wiedergeben vorangestellt haben, gibt der Server **GestureRight** und dann die **GestureRight-Sprechanimation** wieder. [](play-method.md) Wenn die letzte wiedergegebene Animation über keine Sprechanimation verfügt, gibt der -Agent die Animation wieder, die dem **Sprechzustand** des Zeichens zugewiesen ist.

Wenn Sie **Speak** aufrufen und der Audiokanal ausgelastet ist, wird die Audioausgabe des Zeichens nicht gehört, aber der Text wird in der Wortsprechblase angezeigt.

Der automatische Wörterumbruch des Agents im Wortsprechblasen unterbricht Wörter mitHilfe von Leerzeichen (z. B. Leerzeichen oder Tabulatorzeichen). Wenn dies jedoch nicht der Lage ist, kann ein Wort an den Sprechblasen angepasst werden. Fügen Sie in Sprachen wie Japanisch, Chinesisch und Thailändisch, in denen Leerzeichen nicht zum Unterbrechen von Wörtern verwendet werden, ein Unicode-Leerzeichen mit einer Breite von null (0x200B) zwischen Zeichen ein, um logische Wortumbrüche zu definieren.

> [!Note]  
> Die [**Enabled-Eigenschaft**](enabled-property.md) des Sprechblasens muss auch **True** sein, damit Text angezeigt werden kann.

 

> [!Note]  
> Legen Sie die Sprach-ID des Zeichens fest (indem Sie die **LanguageID** des Zeichens festlegen, bevor Sie die **Speak-Methode** verwenden, um eine entsprechende Textanzeige innerhalb der Wortsprechblase sicherzustellen.

 

## <a name="see-also"></a>Weitere Informationen

[**Lesezeichenereignis,**](bookmark-event.md) [**RequestStart-Ereignis,**](requeststart-event.md) [**RequestComplete-Ereignis**](requestcomplete-event.md)


 

 