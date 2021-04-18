---
description: Alle Erkennungs aktivierten Steuerelemente werden über ein Erkennungs Kontext-Objekt erkannt. Mit den Tablet PC-Technologie-APIs können Sie die Eigenschaft "Faktoid" für ein "erkennzercontext"-Objekt festlegen.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Festlegen des Kontexts für Ink-Enabled Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348628"
---
# <a name="setting-context-for-ink-enabled-controls"></a>Festlegen des Kontexts für Ink-Enabled Steuerelemente

Alle Erkennungs aktivierten Steuerelemente werden über ein [**Erkennungs Kontext**](inkrecognizercontext-class.md) -Objekt erkannt. Mit den Tablet PC-Technologie-APIs können Sie die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " für ein " **erkennzercontext** "-Objekt festlegen.

Wenn Sie eine frei Hand fähige Anwendung erstellen, verwenden Sie die Eigenschaften " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " und " [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) " des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts, um Kontexte festzulegen.

Sie können die Zeichen folgen Werte der Namen in den Eingabe Bereichen, die in der [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Enumeration definiert sind, an die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " übergeben, getrennt durch eine öffnende (! und eine schließende). Um z. b. den Kontext für ein [**erkennzercontext**](inkrecognizercontext-class.md) -Objekt für in einer URL verwendete Zeichen festzulegen, verwenden Sie die in den folgenden C-Beispielen gezeigte Syntax \# :


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> Die in der [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Enumeration definierten Eingabe Bereiche ersetzen die Faktoide, die in früheren Versionen des Windows XP Tablet PC Edition SDK verfügbar waren, obwohl diese Faktoide weiterhin funktionieren, um Abwärtskompatibilität zu gewährleisten.

 

Im folgenden C- \# Beispiel wird die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " für Postleitzahlen festgelegt:


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



Eingabe Bereiche können mithilfe der Handschrift Syntax regulärer Ausdrücke kombiniert werden. Weitere Informationen zur Verwendung der Syntax von regulären Ausdrücken finden Sie unter [benutzerdefinierte Eingabe Bereiche mit regulären Ausdrücken](custom-input-scopes-with-regular-expressions.md).

Sie können Erkennungs Flags für das [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt festlegen, um das Verhalten der Erkennung zu beeinflussen. Ein solches Flag ist das **coerce** -Flag in der [**inkrecognitionmodes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) -Enumeration des **erkenzercontext**. Das **coerce** -Flag zwingt die Erkennung, ein Ergebnis zurückzugeben, das der Definition des festgelegten Faktoid entspricht. Wenn Sie z. b. ein Formular haben, das erfordert, dass der Benutzer eine numerische Menge eingegeben hat, kann es hilfreich sein, das " **ist- \_ Nummer** "-Faktoid festzulegen und außerdem die " [**erkenntionflags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) "-Eigenschaft auf " **coerce**" In dieser Instanz garantiert das **coerce** -Flag, dass die Erkennung nur Zahlen zurückgibt.

Im folgenden C- \# Beispiel wird die [**erkenntionflags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) -Eigenschaft auf **coerce** festgelegt:


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



Verwenden Sie jedoch bei der Entscheidung, das **coerce** -Flag festzulegen, Vorsicht. Das Flag erzwingt, dass die Erkennung nur der Definition des Faktoid entspricht. Wenn Sie z. b. den \_ \_ Eingabebereich ist telefonfulltelefonienumber und das **coerce** -Flag festgelegt haben, gibt die Erkennung Ergebnisse zurück, die exakt mit der Definition des \_ nur- \_ telefoniefulltelefonienumber-Eingabe Bereichs übereinstimmen. Wenn ein Benutzer "911" mit dem "is \_ \_ telefonfulltelefonienumber"-Eingabebereich schreibt und das **coerce** -Flag festgelegt ist, kann die Erkennung entweder eine leere Zeichenfolge oder eine zufällige Zeichenfolge im Format (xxx) xxx-xxxx (wobei "X" eine Ziffer ist) zurückgeben. Das Format xxx stimmt nicht mit der Definition des \_ \_ Faktoid ist telefonfulltelefonienumber identisch, obwohl es sich um eine gültige Telefonnummer handelt.

Listen der unterstützten Formate für jeden Eingabebereich finden Sie in der [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Referenz.

Wenn Sie ein Feld zur Standardeinstellung für die Erkennung zurückgeben möchten, legen Sie den Wert für "Faktoid" auf "Default" fest \_ , wie im folgenden C- \# Beispiel gezeigt:


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



Legen Sie für Anwendungen, die das [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden, den Typ "Faktoid" für das Steuerelement fest


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



Dabei `IS_INPUTSCOPE` steht für den Namen des Eingabe Bereichs, den Sie anwenden möchten.

Das [InkEdit](inkedit-control-reference.md) -Steuerelement macht kein [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt verfügbar. Sie können weiterhin Kontext zuweisen, indem Sie die Eigenschaft " [**Faktoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) " des InkEdit-Steuer Elements verwenden, aber Sie können das **wordmode** -Flag nicht festlegen.

 

 
