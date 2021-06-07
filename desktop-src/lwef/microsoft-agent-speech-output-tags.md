---
title: Microsoft Agent Speech-Ausgabetags
description: Microsoft Agent Speech-Ausgabetags
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e712285b8160cf12817890ac42c4d49e95d72a2b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386799"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="e83c1-103">Microsoft Agent Speech-Ausgabetags</span><span class="sxs-lookup"><span data-stu-id="e83c1-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="e83c1-104">\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e83c1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e83c1-105">Die Microsoft Agent-Dienste unterstützen das Ändern der Sprachausgabe über spezielle Tags, die in die Sprachtextzeichenfolge eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e83c1-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="e83c1-106">Mit diesen Tags können Sie die Merkmale des Ausgabeausdrucks des Zeichens ändern.</span><span class="sxs-lookup"><span data-stu-id="e83c1-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="e83c1-107">Sprachausgabetags verwenden die folgenden Syntaxregeln:</span><span class="sxs-lookup"><span data-stu-id="e83c1-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="e83c1-108">Alle Tags beginnen und enden mit einem schrägen Schrägstrich ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="e83c1-108">All tags begin and end with a backslash character (\\).</span></span>
-   <span data-ttu-id="e83c1-109">Der einzelne schräge Schrägstrich ist innerhalb eines Tags nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e83c1-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="e83c1-110">Verwenden Sie einen doppelten schrägen Schrägstrich ( ), um einen schrägen Schrägstrich in einen Textparameter eines Tags ein-/aus. \\ \\</span><span class="sxs-lookup"><span data-stu-id="e83c1-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\\).</span></span>
-   <span data-ttu-id="e83c1-111">Bei Tags wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e83c1-111">Tags are case-insensitive.</span></span> <span data-ttu-id="e83c1-112">Pit ist \\ \\ z. B. identisch mit \\ PIT \\ .</span><span class="sxs-lookup"><span data-stu-id="e83c1-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="e83c1-113">Tags sind leerraumabhängig.</span><span class="sxs-lookup"><span data-stu-id="e83c1-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="e83c1-114">Beispielsweise ist \\ Rst \\ nicht mit \\ Rst \\ identisch.</span><span class="sxs-lookup"><span data-stu-id="e83c1-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="e83c1-115">Sofern nicht anders angegeben oder durch ein anderes Tag geändert, behält die Sprachausgabe das Merkmal bei, das durch das -Tag innerhalb des in einer einzelnen Speak-Methode angegebenen [**Texts festgelegt**](speak-method.md) wird.</span><span class="sxs-lookup"><span data-stu-id="e83c1-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="e83c1-116">Die Sprachausgabe wird automatisch über die benutzerdefinierten Parameter zurückgesetzt, nachdem eine **Speak-Methode** abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e83c1-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="e83c1-117">Einige Tags enthalten Zeichenfolgen in Anführungswörtern.</span><span class="sxs-lookup"><span data-stu-id="e83c1-117">Some tags include quoted strings.</span></span> <span data-ttu-id="e83c1-118">Für einige Programmiersprachen wie Visual Basic Scripting Edition (VBScript) und Visual Basic bedeutet dies, dass Sie möglicherweise zwei Anführungszeichen verwenden müssen, um den Parameter des Tags zu kennzeichnen oder ein doppeltes Anführungszeichen als Teil der Zeichenfolge zu verketten.</span><span class="sxs-lookup"><span data-stu-id="e83c1-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="e83c1-119">Letzteres wird in diesem Beispiel Visual Basic gezeigt:</span><span class="sxs-lookup"><span data-stu-id="e83c1-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="e83c1-120">Bei C-, C++- und Java™-Programmierung vor den zurücken Schrägstrichen und doppelten Anführungszeichen mit einem zurücken Schrägstrich.</span><span class="sxs-lookup"><span data-stu-id="e83c1-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="e83c1-121">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e83c1-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="e83c1-122">Für Sprachen, die Doppel-Byte-Zeichensatzzeichen (Double-Byte Character Set, DBCS) unterstützen, können Sie Doppel bytezeichen verwenden, um Zeichenfolgenparameter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e83c1-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="e83c1-123">Verwenden Sie jedoch Einzel bytezeichen für alle anderen Parameter und Zeichen, die zum Definieren des Tags verwendet werden, einschließlich des Tags selbst.</span><span class="sxs-lookup"><span data-stu-id="e83c1-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="e83c1-124">Die folgenden Tags werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e83c1-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="e83c1-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="e83c1-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="e83c1-126">**Ctx**</span><span class="sxs-lookup"><span data-stu-id="e83c1-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="e83c1-127">**Emp**</span><span class="sxs-lookup"><span data-stu-id="e83c1-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="e83c1-128">**Lst**</span><span class="sxs-lookup"><span data-stu-id="e83c1-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="e83c1-129">**Karte**</span><span class="sxs-lookup"><span data-stu-id="e83c1-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="e83c1-130">**Mrk**</span><span class="sxs-lookup"><span data-stu-id="e83c1-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="e83c1-131">**Pau**</span><span class="sxs-lookup"><span data-stu-id="e83c1-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="e83c1-132">**Grube**</span><span class="sxs-lookup"><span data-stu-id="e83c1-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="e83c1-133">**Ersten**</span><span class="sxs-lookup"><span data-stu-id="e83c1-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="e83c1-134">**Spd**</span><span class="sxs-lookup"><span data-stu-id="e83c1-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="e83c1-135">**Vol**</span><span class="sxs-lookup"><span data-stu-id="e83c1-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="e83c1-136">Die Tags sind in erster Linie für die Anpassung der von TTS (Text-to-Speech) generierten Ausgabe konzipiert.</span><span class="sxs-lookup"><span data-stu-id="e83c1-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="e83c1-137">Nur die [**Mrk-**](mrk-tag.md) und [**Map-Tags**](map-tag.md) können mit audiodateibasierter gesprochener Ausgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e83c1-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="e83c1-138">Microsoft Agent unterstützt nicht alle Tags, die im Microsoft Speech SDK dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="e83c1-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="e83c1-139">Die Parameter können auch abhängig von der ausgewählten TTS-Engine variieren.</span><span class="sxs-lookup"><span data-stu-id="e83c1-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="e83c1-140">Sie können eine bestimmte TTS-Engine mit [**TTSModeID festlegen.**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="e83c1-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




