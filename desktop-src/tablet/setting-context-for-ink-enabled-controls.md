---
description: Die erkennung für ink-fähige Steuerelemente erfolgt über ein RecognizerContext-Objekt. Mit den Tablet PC-Technologie-APIs können Sie die Factoid-Eigenschaft für ein RecognizerContext-Objekt festlegen.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Festlegen des Kontexts für Ink-Enabled-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306ae4c76ce5187c930c24a10631ec703f684cc8a3e4b0a94f46414bddbd058f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091303"
---
# <a name="setting-context-for-ink-enabled-controls"></a>Festlegen des Kontexts für Ink-Enabled-Steuerelemente

Die erkennung für ink-fähige Steuerelemente erfolgt über ein [**RecognizerContext-Objekt.**](inkrecognizercontext-class.md) Mit den Tablet PC-Technologie-APIs können Sie die [**Factoid-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) für ein **RecognizerContext-Objekt** festlegen.

Wenn Sie eine Freifunktionsanwendung erstellen, verwenden Sie die [**Eigenschaften Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) und [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) des [**RecognizerContext-Objekts,**](inkrecognizercontext-class.md) um Kontexte zu setzen.

Sie können die Zeichenfolgenwerte der Namen in den Eingabebereich, die in der [**InputScope-Enumeration**](/windows/win32/api/inputscope/ne-inputscope-inputscope) definiert sind, an die [**Factoid-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) übergeben, getrennt durch eine öffnende (! und eine schließende ). Wenn Sie beispielsweise den Kontext für ein [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) so festlegen, dass er in Richtung der in einer URL verwendeten Zeichen voreingenommen wird, verwenden Sie die in den folgenden C-Beispielen gezeigte \# Syntax:


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> Die in der [**InputScope-Enumeration**](/windows/win32/api/inputscope/ne-inputscope-inputscope) definierten Eingabebereich haben die Fakten, die in früheren Versionen des Windows XP Tablet PC Edition SDK verfügbar waren, ersetzt, obwohl diese Fakten weiterhin funktionieren, um Abwärtskompatibilität zu gewährleisten.

 

Im folgenden \# C-Beispiel wird die [**Factoid-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) für Postleitzahlen definiert:


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



Sie können Eingabebereich kombinieren, indem Sie die Syntax für handschriftliche reguläre Ausdrücke verwenden. Weitere Informationen zur Verwendung der Syntax für reguläre Ausdrücke finden Sie unter [Benutzerdefinierte Eingabebereich mit regulären Ausdrücken.](custom-input-scopes-with-regular-expressions.md)

Sie können Erkennungsflags für das [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) festlegen, um das Verhalten der Erkennung zu beeinflussen. Ein solches Flag ist das **Coerce-Flag** in der [**InkRecognitionModes-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) des **RecognizerContext.** Das **Coerce-Flag** erzwingt die Rückgabe eines Ergebnisses, das der Definition des festgelegten Factoids entspricht. Wenn Sie beispielsweise über ein Formular verfügen, für das der Benutzer eine numerische Menge eingeben muss, kann es hilfreich sein, das **IS \_ NUMBER-Factoid** und auch die [**RecognitionFlags-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) auf **Coerce zu setzen.** In diesem Fall garantiert das **Coerce-Flag,** dass die Recognizer nur Zahlen zurückgibt.

Im folgenden \# C-Beispiel wird die [**RecognitionFlags-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) auf **Coerce legt:**


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



Seien Sie jedoch vorsichtig, wenn Sie sich für das Festlegen des **Coerce-Flags** entscheiden. Das Flag erzwingt, dass die Recognizer nur mit der Definition des Factoids übereinstimmen muss. Wenn Sie z. B. den Eingabebereich IS TELEPHONE FULLTELEPHONENUMBER und das Coerce-Flag festlegen, gibt die Recognizer Ergebnisse zurück, die genau mit der Definition des \_ \_ IS TELEPHONE  \_ \_ FULLTELEPHONENUMBER-Eingabebereichs übereinstimmen. Wenn ein Benutzer "911" mit dem Eingabebereich IS TELEPHONE FULLTELEPHONENUMBER und dem festgelegten Coerce-Flag schreibt, gibt die Recognizer möglicherweise entweder eine leere Zeichenfolge oder eine zufällige Zeichenfolge im Format \_ \_ (XXX) XXX-XXXX zurück (wobei X  eine Ziffer ist). Das Format von XXX passt nicht zur Definition des IS \_ TELEPHONE FULLTELEPHONENUMBER-Faktenoids, obwohl es sich um \_ eine gültige Telefonnummer handelt.

Listen der unterstützten Formate für jeden Eingabebereich finden Sie in der [**InputScope-Referenz.**](/windows/win32/api/inputscope/ne-inputscope-inputscope)

Um ein Feld an die Standardeinstellung für die Recognizer zurück zu geben, legen Sie das Factoid auf IS \_ DEFAULT fest, wie im folgenden C-Beispiel: \#


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



Legen Sie für Anwendungen, die das [InkEdit-Steuerelement](inkedit-control-reference.md) verwenden, den Factoidtyp für das Steuerelement fest, indem Sie Folgendes angeben:


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



Dabei `IS_INPUTSCOPE` ist der Name des Eingabebereichs, den Sie anwenden möchten.

Das [InkEdit-Steuerelement](inkedit-control-reference.md) macht kein [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) verfügbar. Sie können weiterhin Kontext zuweisen, indem Sie die [**Factoid-Eigenschaft**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) des InkEdit-Steuerelements verwenden, aber Sie können das **WORDMODE-Flag nicht** festlegen.

 

 
