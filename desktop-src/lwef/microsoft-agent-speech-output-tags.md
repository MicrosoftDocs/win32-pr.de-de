---
title: Microsoft-Agent-Sprachausgabe Tags
description: Microsoft-Agent-Sprachausgabe Tags
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856212"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="087d9-103">Microsoft-Agent-Sprachausgabe Tags</span><span class="sxs-lookup"><span data-stu-id="087d9-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="087d9-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="087d9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="087d9-105">Die Microsoft-Agent-Dienste unterstützen das Ändern der Sprachausgabe über spezielle Tags, die in die Zeichenfolge für die sprach</span><span class="sxs-lookup"><span data-stu-id="087d9-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="087d9-106">Diese Tags helfen Ihnen, die Eigenschaften des Ausgabe Ausdrucks des Zeichens zu ändern.</span><span class="sxs-lookup"><span data-stu-id="087d9-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="087d9-107">Für Sprachausgabe Tags werden die folgenden Syntax Regeln verwendet:</span><span class="sxs-lookup"><span data-stu-id="087d9-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="087d9-108">Alle Tags beginnen und enden mit einem umgekehrten Schrägstrich ( \) .</span><span class="sxs-lookup"><span data-stu-id="087d9-108">All tags begin and end with a backslash character (\).</span></span>
-   <span data-ttu-id="087d9-109">Der einzelne umgekehrte Schrägstrich ist innerhalb eines Tags nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="087d9-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="087d9-110">Wenn Sie einen umgekehrten Schrägstrich in einen Text Parameter eines Tags einschließen möchten, verwenden Sie einen doppelten umgekehrten Schrägstrich ( \\ \) .</span><span class="sxs-lookup"><span data-stu-id="087d9-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\).</span></span>
-   <span data-ttu-id="087d9-111">Tags Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="087d9-111">Tags are case-insensitive.</span></span> <span data-ttu-id="087d9-112">Beispielsweise \\ ist Pit \\ das gleiche wie \\ Pit \\ .</span><span class="sxs-lookup"><span data-stu-id="087d9-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="087d9-113">Tags sind Leerzeichen abhängig.</span><span class="sxs-lookup"><span data-stu-id="087d9-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="087d9-114">Beispielsweise \\ ist RST \\ nicht mit \\ RST identisch \\ .</span><span class="sxs-lookup"><span data-stu-id="087d9-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="087d9-115">Sofern nicht anders angegeben oder von einem anderen Tag geändert, behält die Sprachausgabe das von dem-Tag festgelegte Merkmal in dem Text bei, der in einer einzelnen [**Sprech**](speak-method.md) Methode angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="087d9-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="087d9-116">Die Sprachausgabe wird automatisch durch die benutzerdefinierten Parameter zurückgesetzt, **nachdem eine Sprech** Methode abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="087d9-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="087d9-117">Einige Tags enthalten Zeichen folgen in Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="087d9-117">Some tags include quoted strings.</span></span> <span data-ttu-id="087d9-118">Für einige Programmiersprachen, wie z. b. Visual Basic Scripting Edition (VBScript) und Visual Basic, bedeutet dies, dass Sie möglicherweise zwei Anführungszeichen verwenden müssen, um den Parameter des Tags anzugeben oder ein doppeltes Anführungszeichen als Teil der Zeichenfolge zu verketten.</span><span class="sxs-lookup"><span data-stu-id="087d9-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="087d9-119">Letzteres wird in diesem Visual Basic Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="087d9-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="087d9-120">Stellen Sie für C-, C++-und Java-™ Programmierung vor umgekehrten Schrägstrichen und doppelten Anführungszeichen mit einem umgekehrten Schrägstrich voran.</span><span class="sxs-lookup"><span data-stu-id="087d9-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="087d9-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="087d9-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="087d9-122">Für Fremdsprachen, die Zeichen mit Doppelbyte-Zeichensatz (Double-Byte Character Set, DBCS) unterstützen, können Sie Zeichen folgen Parameter mithilfe von Doppelbyte Zeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="087d9-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="087d9-123">Verwenden Sie jedoch Einzel Byte Zeichen für alle anderen Parameter und Zeichen, die zum Definieren des Tags verwendet werden, einschließlich des Tags selbst.</span><span class="sxs-lookup"><span data-stu-id="087d9-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="087d9-124">Die folgenden Tags werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="087d9-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="087d9-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="087d9-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="087d9-126">**CTX**</span><span class="sxs-lookup"><span data-stu-id="087d9-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="087d9-127">**EMP**</span><span class="sxs-lookup"><span data-stu-id="087d9-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="087d9-128">**LST**</span><span class="sxs-lookup"><span data-stu-id="087d9-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="087d9-129">**Bilden**</span><span class="sxs-lookup"><span data-stu-id="087d9-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="087d9-130">**MRK**</span><span class="sxs-lookup"><span data-stu-id="087d9-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="087d9-131">**Referi**</span><span class="sxs-lookup"><span data-stu-id="087d9-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="087d9-132">**Baum**</span><span class="sxs-lookup"><span data-stu-id="087d9-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="087d9-133">**RST**</span><span class="sxs-lookup"><span data-stu-id="087d9-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="087d9-134">**SPD**</span><span class="sxs-lookup"><span data-stu-id="087d9-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="087d9-135">**Volumen**</span><span class="sxs-lookup"><span data-stu-id="087d9-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="087d9-136">Die Tags sind hauptsächlich für die Anpassung von von der Text-zu-Sprache (TTS) generierten Ausgaben konzipiert.</span><span class="sxs-lookup"><span data-stu-id="087d9-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="087d9-137">Nur die [**MRK**](mrk-tag.md) -und [**map**](map-tag.md) -Tags können mit Audiodatei-basierter, gesprochener Ausgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="087d9-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="087d9-138">Der Microsoft-Agent unterstützt nicht alle Tags, die im Microsoft Speech SDK dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="087d9-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="087d9-139">Parameter können auch abhängig von der ausgewählten TTS-Engine variieren.</span><span class="sxs-lookup"><span data-stu-id="087d9-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="087d9-140">Sie können eine bestimmte TTS-Engine mit [**ttsmodeid**](ttsmodeid-property.md)festlegen.</span><span class="sxs-lookup"><span data-stu-id="087d9-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




