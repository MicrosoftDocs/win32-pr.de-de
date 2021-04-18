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
# <a name="setting-context-for-ink-enabled-controls"></a><span data-ttu-id="270ca-104">Festlegen des Kontexts für Ink-Enabled Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="270ca-104">Setting Context for Ink-Enabled Controls</span></span>

<span data-ttu-id="270ca-105">Alle Erkennungs aktivierten Steuerelemente werden über ein [**Erkennungs Kontext**](inkrecognizercontext-class.md) -Objekt erkannt.</span><span class="sxs-lookup"><span data-stu-id="270ca-105">All recognition for ink-enabled controls occurs through a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="270ca-106">Mit den Tablet PC-Technologie-APIs können Sie die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " für ein " **erkennzercontext** "-Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="270ca-106">The Tablet PC Technology APIs enable you to set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on a **RecognizerContext** object.</span></span>

<span data-ttu-id="270ca-107">Wenn Sie eine frei Hand fähige Anwendung erstellen, verwenden Sie die Eigenschaften " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " und " [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) " des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts, um Kontexte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="270ca-107">If you are creating an ink-enabled application, use the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) and [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) properties to set contexts.</span></span>

<span data-ttu-id="270ca-108">Sie können die Zeichen folgen Werte der Namen in den Eingabe Bereichen, die in der [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Enumeration definiert sind, an die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " übergeben, getrennt durch eine öffnende (!</span><span class="sxs-lookup"><span data-stu-id="270ca-108">You may pass in the string values of the names in the input scopes defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property, delimited with an opening (!</span></span> <span data-ttu-id="270ca-109">und eine schließende).</span><span class="sxs-lookup"><span data-stu-id="270ca-109">and a closing ).</span></span> <span data-ttu-id="270ca-110">Um z. b. den Kontext für ein [**erkennzercontext**](inkrecognizercontext-class.md) -Objekt für in einer URL verwendete Zeichen festzulegen, verwenden Sie die in den folgenden C-Beispielen gezeigte Syntax \# :</span><span class="sxs-lookup"><span data-stu-id="270ca-110">For example, to set the context for a [**RecognizerContext**](inkrecognizercontext-class.md) object to bias toward characters used in a URL, use the syntax shown in the following C\# examples:</span></span>


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> <span data-ttu-id="270ca-111">Die in der [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Enumeration definierten Eingabe Bereiche ersetzen die Faktoide, die in früheren Versionen des Windows XP Tablet PC Edition SDK verfügbar waren, obwohl diese Faktoide weiterhin funktionieren, um Abwärtskompatibilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="270ca-111">The input scopes as defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration supersede the factoids that were available in previous versions of the Windows XP Tablet PC Edition SDK, although these factoids will continue to work in order to provide backward compatibility.</span></span>

 

<span data-ttu-id="270ca-112">Im folgenden C- \# Beispiel wird die Eigenschaft " [**Faktoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) " für Postleitzahlen festgelegt:</span><span class="sxs-lookup"><span data-stu-id="270ca-112">The following C\# example sets the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property for postal codes:</span></span>


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



<span data-ttu-id="270ca-113">Eingabe Bereiche können mithilfe der Handschrift Syntax regulärer Ausdrücke kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="270ca-113">You can combine input scopes by using the handwriting regular expression syntax.</span></span> <span data-ttu-id="270ca-114">Weitere Informationen zur Verwendung der Syntax von regulären Ausdrücken finden Sie unter [benutzerdefinierte Eingabe Bereiche mit regulären Ausdrücken](custom-input-scopes-with-regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="270ca-114">For more details about using regular expression syntax, see [Custom Input Scopes with Regular Expressions](custom-input-scopes-with-regular-expressions.md).</span></span>

<span data-ttu-id="270ca-115">Sie können Erkennungs Flags für das [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt festlegen, um das Verhalten der Erkennung zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="270ca-115">You can set recognition flags on the [**RecognizerContext**](inkrecognizercontext-class.md) object to affect the behavior of the recognizer.</span></span> <span data-ttu-id="270ca-116">Ein solches Flag ist das **coerce** -Flag in der [**inkrecognitionmodes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) -Enumeration des **erkenzercontext**.</span><span class="sxs-lookup"><span data-stu-id="270ca-116">One such flag is the **Coerce** flag in the [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) enumeration of the **RecognizerContext**.</span></span> <span data-ttu-id="270ca-117">Das **coerce** -Flag zwingt die Erkennung, ein Ergebnis zurückzugeben, das der Definition des festgelegten Faktoid entspricht.</span><span class="sxs-lookup"><span data-stu-id="270ca-117">The **Coerce** flag forces the recognizer to return a result that matches the definition of the factoid that is set.</span></span> <span data-ttu-id="270ca-118">Wenn Sie z. b. ein Formular haben, das erfordert, dass der Benutzer eine numerische Menge eingegeben hat, kann es hilfreich sein, das " **ist- \_ Nummer** "-Faktoid festzulegen und außerdem die " [**erkenntionflags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) "-Eigenschaft auf " **coerce**"</span><span class="sxs-lookup"><span data-stu-id="270ca-118">For example, if you have a form that requires the user to enter a numerical quantity, it may be useful to set the **IS\_NUMBER** factoid and also set the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**.</span></span> <span data-ttu-id="270ca-119">In dieser Instanz garantiert das **coerce** -Flag, dass die Erkennung nur Zahlen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="270ca-119">In that instance, the **Coerce** flag guarantees that the recognizer returns only numbers.</span></span>

<span data-ttu-id="270ca-120">Im folgenden C- \# Beispiel wird die [**erkenntionflags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) -Eigenschaft auf **coerce** festgelegt:</span><span class="sxs-lookup"><span data-stu-id="270ca-120">The following C\# example sets the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**:</span></span>


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



<span data-ttu-id="270ca-121">Verwenden Sie jedoch bei der Entscheidung, das **coerce** -Flag festzulegen, Vorsicht.</span><span class="sxs-lookup"><span data-stu-id="270ca-121">However, use caution when deciding to set the **Coerce** flag.</span></span> <span data-ttu-id="270ca-122">Das Flag erzwingt, dass die Erkennung nur der Definition des Faktoid entspricht.</span><span class="sxs-lookup"><span data-stu-id="270ca-122">The flag forces the recognizer to match only the definition of the factoid.</span></span> <span data-ttu-id="270ca-123">Wenn Sie z. b. den \_ \_ Eingabebereich ist telefonfulltelefonienumber und das **coerce** -Flag festgelegt haben, gibt die Erkennung Ergebnisse zurück, die exakt mit der Definition des \_ nur- \_ telefoniefulltelefonienumber-Eingabe Bereichs übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="270ca-123">For example, if you set the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag, the recognizer returns results that exactly match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope only.</span></span> <span data-ttu-id="270ca-124">Wenn ein Benutzer "911" mit dem "is \_ \_ telefonfulltelefonienumber"-Eingabebereich schreibt und das **coerce** -Flag festgelegt ist, kann die Erkennung entweder eine leere Zeichenfolge oder eine zufällige Zeichenfolge im Format (xxx) xxx-xxxx (wobei "X" eine Ziffer ist) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="270ca-124">If a user writes "911" with the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag set, the recognizer may return either an empty string or a random string in the format of (XXX) XXX-XXXX (where X is a digit).</span></span> <span data-ttu-id="270ca-125">Das Format xxx stimmt nicht mit der Definition des \_ \_ Faktoid ist telefonfulltelefonienumber identisch, obwohl es sich um eine gültige Telefonnummer handelt.</span><span class="sxs-lookup"><span data-stu-id="270ca-125">The format of XXX does not match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER factoid, even though it is a valid phone number.</span></span>

<span data-ttu-id="270ca-126">Listen der unterstützten Formate für jeden Eingabebereich finden Sie in der [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) -Referenz.</span><span class="sxs-lookup"><span data-stu-id="270ca-126">For lists of the supported formats for each input scope, see the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reference.</span></span>

<span data-ttu-id="270ca-127">Wenn Sie ein Feld zur Standardeinstellung für die Erkennung zurückgeben möchten, legen Sie den Wert für "Faktoid" auf "Default" fest \_ , wie im folgenden C- \# Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="270ca-127">To return a field to the default setting for the recognizer, set the factoid to IS\_DEFAULT , as in the following C\# example:</span></span>


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



<span data-ttu-id="270ca-128">Legen Sie für Anwendungen, die das [InkEdit](inkedit-control-reference.md) -Steuerelement verwenden, den Typ "Faktoid" für das Steuerelement fest</span><span class="sxs-lookup"><span data-stu-id="270ca-128">For applications that use the [InkEdit](inkedit-control-reference.md) control, set the factoid type for the control by specifying:</span></span>


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



<span data-ttu-id="270ca-129">Dabei `IS_INPUTSCOPE` steht für den Namen des Eingabe Bereichs, den Sie anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="270ca-129">Where `IS_INPUTSCOPE` is the name of the input scope you want to apply.</span></span>

<span data-ttu-id="270ca-130">Das [InkEdit](inkedit-control-reference.md) -Steuerelement macht kein [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="270ca-130">The [InkEdit](inkedit-control-reference.md) control does not expose a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="270ca-131">Sie können weiterhin Kontext zuweisen, indem Sie die Eigenschaft " [**Faktoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) " des InkEdit-Steuer Elements verwenden, aber Sie können das **wordmode** -Flag nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="270ca-131">You can still assign context by using the [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) property of the InkEdit control, but you cannot set the **WORDMODE** flag.</span></span>

 

 
