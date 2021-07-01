---
title: IAgentCharacter Prepare
description: IAgentCharacter Prepare
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119875"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter::P repare

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

Ruft Animationsdaten für ein Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgegeben wird, enthält *pdwReqID* die ID der Anforderung.

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

Ein -Wert, der den zu ladenden Animationsdatentyp angibt, der einer der folgenden Sein muss:



| Wert                                                           | Beschreibung                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| **const unsigned short** **PREPARE ANIMATION = \_ 0;**<br/> | Animationsdaten eines Zeichens.                              |
| **const unsigned short** **PREPARE STATE = \_ 1;**<br/>     | Zustandsdaten eines Zeichens.                                  |
| **const unsigned short** **PREPARE WAVE = \_ 2**<br/>       | Die Sounddatei eines Zeichens (. WAV oder . LWV) für die gesprochene Ausgabe. |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Der Name der Animation oder des Zustands.

Der Animationsname basiert auf dem Namen, der für das Zeichen definiert wurde, als es mit dem Microsoft-Agent-Zeichen-Editor gespeichert wurde.

Für Status kann der Wert einer der folgenden Sein:



|                      | Beschreibung                                     |
|----------------------|-------------------------------------------------|
| **"Gesturing"**      | So rufen Sie alle **Gesturingzustandsanimationen** ab. |
| **"GesturingDown"**  | So rufen Sie **GesturingDown-Animationen** ab.       |
| **"GesturingLeft"**  | So rufen Sie **GesturingLeft-Animationen** ab.       |
| **"GesturingRight"** | So rufen Sie **GesturingRight-Animationen** ab.      |
| **"GesturingUp"**    | So rufen Sie **GesturingUp-Animationen** ab.         |
| **"Ausblenden"**         | So rufen Sie die Animationen des **Ausblendenszustands** ab.    |
| **"Hörvermögen"**        | So rufen  Sie die Hörzustandsanimationen ab.   |
| **"Idling"**         | So rufen  Sie alle Idling-Zustandsanimationen ab.    |
| **"IdlingLevel1"**   | So rufen Sie alle **IdlingLevel1-Animationen** ab.    |
| **"IdlingLevel2"**   | So rufen Sie alle **IdlingLevel2-Animationen** ab.    |
| **"IdlingLevel3"**   | So rufen Sie alle **IdlingLevel3-Animationen** ab.    |
| **"Lauschen"**      | So rufen  Sie die Überwachungzustandsanimationen ab. |
| **"Moving" (Verschieben)**         | So rufen Sie alle **Animationen des Bewegungszustands** ab.    |
| **"MovingDown"**     | So rufen Sie alle **Moving-Animationen** ab.          |
| **"MovingLeft"**     | So rufen Sie alle **MovingLeft-Animationen** ab.      |
| **"MovingRight"**    | So rufen Sie alle **MovingRight-Animationen** ab.     |
| **"MovingUp"**       | So rufen Sie alle **MovingUp-Animationen** ab.        |
| **"Showing" (Wird angezeigt)**        | So rufen Sie die **Zustandsanimationen anzeigen** ab.   |
| **"Sprechen"**       | So rufen  Sie die Sprechzustandsanimationen ab.  |



 

Für. WAV-Dateien: Legen Sie *bszName* auf die URL oder Dateispezifikation für fest. WAV-Datei. Wenn die Spezifikation nicht vollständig ist, wird sie als relativ zur Spezifikation interpretiert, die in der [**Load-Methode**](https://www.bing.com/search?q=**Load**) verwendet wird.

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

Ein boolescher Wert, der angibt, ob der Server die [**Prepare-Anforderung**](/windows/desktop/lwef/iagentcharacter--prepare) in die Warteschlange stellt. **True** stellt die Anforderung in die Warteschlange und bewirkt, dass jede darauf folgende Animationsanforderung wartet, bis die von ihr angegebenen Animationsdaten geladen werden. **False** ruft die Animationsdaten asynchron ab.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die Anforderungs-ID [**vorbereiten**](/windows/desktop/lwef/iagentcharacter--prepare) empfängt.

</dd> </dl>

Wenn Sie ein Zeichen mithilfe des HTTP-Protokolls laden (ein . ACF-Datei), müssen Sie die [**Prepare-Methode**](/windows/desktop/lwef/iagentcharacter--prepare) verwenden, um Animationsdaten abzurufen, bevor Sie die Animation wiedergeben können. Sie können diese Methode nicht verwenden, wenn Sie das Zeichen mit dem UNC-Protokoll (einem ) geladen haben. ACS-Datei). Sie können mit **Prepare** auch keine HTTP-Daten für ein Zeichen abrufen, wenn Sie dieses Zeichen mithilfe des UNC-Protokolls geladen haben (. ACS-Zeichendatei).

Mit der [**Prepare-Methode**](/windows/desktop/lwef/iagentcharacter--prepare) abgerufene Animations- oder Sounddaten werden im Cache des Browsers gespeichert. Nachfolgende Aufrufe überprüfen den Cache, und wenn die Animationsdaten bereits vorhanden sind, lädt das Steuerelement die Daten direkt aus dem Cache. Nach dem Laden können die Animations- oder Sounddaten mit den [**Methoden Wiedergeben**](/windows/desktop/lwef/iagentcharacter--play) oder [**Sprechen**](/windows/desktop/lwef/iagentcharacter--speak) wiedergegeben werden.

Sie können mehrere Animationen und Zustände angeben, indem Sie sie durch Kommas trennen. Sie können Typen jedoch nicht in derselben [**Prepare-Anweisung**](/windows/desktop/lwef/iagentcharacter--prepare) mischen.

 

