---
title: Iagentcharacter-Vorbereitung
description: Iagentcharacter-Vorbereitung
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038956"
---
# <a name="iagentcharacterprepare"></a>Iagentcharacter::P repare

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

Ruft Animationsdaten für ein Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

Ein Wert, der den zu ladenden Animations Datentyp angibt, der eines der folgenden sein muss:



| Wert                                                           | BESCHREIBUNG                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| Animation für " **Ganzzahl ohne Vorzeichen Short** **Prepare" \_ = 0;**<br/> | Die Animationsdaten eines Zeichens.                              |
| **Ganzzahl ohne Vorzeichen Short** **Prepare \_ State = 1;**<br/>     | Die Zustandsdaten eines Zeichens.                                  |
| Konstante " **Ganzzahl ohne Vorzeichen Short** **Prepare \_ Wave = 2** "<br/>       | Die Audiodatei eines Zeichens (. WAV oder. Lwv) für die gesprochene Ausgabe. |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszname*
</dt> <dd>

Der Name der Animation oder des Zustands.

Der Animations Name basiert auf dem, der für das Zeichen definiert wurde, als es mit dem Microsoft-Agent-Zeichen-Editor gespeichert wurde.

Für Zustände kann der Wert eines der folgenden sein:



|                      |                                                 |
|----------------------|-------------------------------------------------|
| **"Gesturung"**      | Zum Abrufen aller **gestörenden** Zustands Animationen. |
| **"Gesturingdown"**  | Zum Abrufen von **gesturingdown** -Animationen.       |
| **"Gesturingleft"**  | Zum Abrufen von **gesturingleft** -Animationen.       |
| **"Gesturingright"** | Zum Abrufen von **gesturingright** -Animationen.      |
| **"Gesturingup"**    | Zum Abrufen von **gesturingup** -Animationen.         |
| **Zieher**         | Zum **Abrufen der Animationen zum Ausblenden** des Zustands.    |
| **Sinn**        | Zum Abrufen der **hörzustands** Animationen.   |
| **Leerlauf**         | , Um alle **idck** State-Animationen abzurufen.    |
| **"IdlingLevel1"**   | Zum Abrufen aller **IdlingLevel1** -Animationen.    |
| **"IdlingLevel2"**   | Zum Abrufen aller **IdlingLevel2** -Animationen.    |
| **"IdlingLevel3"**   | Zum Abrufen aller **IdlingLevel3** -Animationen.    |
| **Raum**      | **Zum Abrufen der Animation** des Empfangs Zustands. |
| **Verschieben**         | Zum Abrufen aller **beweglicher** Zustands Animationen.    |
| **""**     | , Um alle Verschieb **enden** Animationen abzurufen.          |
| **"Wvingleft"**     | Zum Abrufen aller Animationen von " **wvingleft** ".      |
| **"Wvingright"**    | , Um alle **wvingright** -Animationen abzurufen.     |
| **"Wvingup"**       | Zum Abrufen aller " **wvingup** "-Animationen.        |
| **Zeigten**        | Zum Abrufen der **Anzeige** Zustands Animationen.   |
| **Isch**       | Zum Abrufen der **sprach** Zustands Animationen.  |



 

Damit. WAV-Dateien, legen Sie *bszname* auf die URL oder die Datei Spezifikation für fest. WAV-Datei. Wenn die Spezifikation nicht fertig ist, wird Sie als relativ zu der in der [**Load**](https://www.bing.com/search?q=**Load**) -Methode verwendeten Spezifikation interpretiert.

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bqueue*
</dt> <dd>

Ein boolescher Wert, der angibt, ob der Server die [**Vorbereitungs**](/windows/desktop/lwef/iagentcharacter--prepare) Anforderung anfügt. **True** fügt die Anforderung in die Warteschlange ein und bewirkt, dass alle darauf folgenden Animations Anforderungen warten, bis die von ihr festgelegten Animationsdaten geladen sind. **False** Ruft die Animationsdaten asynchron ab.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, die die ID der [**Vorbereitungs**](/windows/desktop/lwef/iagentcharacter--prepare) Anforderung empfängt.

</dd> </dl>

Wenn Sie ein Zeichen mithilfe des HTTP-Protokolls (ein-Zeichen) laden. ACF-Datei). Sie müssen die [**Vorbereitungs**](/windows/desktop/lwef/iagentcharacter--prepare) Methode zum Abrufen von Animationsdaten verwenden, bevor Sie die Animation wiedergeben können. Diese Methode kann nicht verwendet werden, wenn Sie das Zeichen mithilfe des UNC-Protokolls (eines geladen haben. ACS-Datei). Sie können auch keine HTTP-Daten für ein Zeichen abrufen, indem Sie **vorbereiten** verwenden, wenn Sie dieses Zeichen mithilfe des UNC-Protokolls () geladen haben. ACS-Zeichen Datei).

Die mit der [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode abgerufenen Animations-oder Audiodaten werden im Cache des Browsers gespeichert. Bei nachfolgenden Aufrufen wird der Cache überprüft. wenn die Animationsdaten bereits vorhanden sind, lädt das-Steuerelement die Daten direkt aus dem Cache. Nach dem Laden können die Animations-oder Audiodaten mit den Methoden " [**abspielen**](/windows/desktop/lwef/iagentcharacter--play) " und " [**Sprache**](/windows/desktop/lwef/iagentcharacter--speak) " wiedergegeben werden.

Sie können mehrere Animationen und Zustände angeben, indem Sie Sie durch Kommas trennen. Es ist jedoch nicht möglich, Typen in derselben [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Anweisung zu mischen.

 

