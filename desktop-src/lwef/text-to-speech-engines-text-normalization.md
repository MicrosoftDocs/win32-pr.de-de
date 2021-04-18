---
title: Text Normalisierung für Text-zu-Sprache-Engines
description: Text Normalisierung für Text-zu-Sprache-Engines
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337987"
---
# <a name="text-to-speech-engines-text-normalization"></a><span data-ttu-id="40b32-103">Text Normalisierung für Text-zu-Sprache-Engines</span><span class="sxs-lookup"><span data-stu-id="40b32-103">Text-to-Speech Engines Text Normalization</span></span>

<span data-ttu-id="40b32-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="40b32-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="40b32-105">Bei der Normalisierung werden Zahlen, Abkürzungen, Akronyme und idiomatiken identifiziert und nach Bedarf in voll Text transformiert. Dies ist in der Regel auf dem Kontext des Satzes begründet.</span><span class="sxs-lookup"><span data-stu-id="40b32-105">Normalization is the process of identifying numbers, abbreviations, acronyms and idiomatics and transforming them into full text as needed, usually based on the context of the sentence.</span></span>

<span data-ttu-id="40b32-106">Beispielsweise wird mit dem L&H truvoice American-TTS-Modul der Satz:</span><span class="sxs-lookup"><span data-stu-id="40b32-106">For example, using the L&H TruVoice American English TTS Engine, the sentence:</span></span>

<span data-ttu-id="40b32-107">King George VI von England ist am 6. Februar 1952.</span><span class="sxs-lookup"><span data-stu-id="40b32-107">King George VI of England died on Feb 6, 1952.</span></span>

<span data-ttu-id="40b32-108">wird im **normalen Kontext** wie folgt gelesen:</span><span class="sxs-lookup"><span data-stu-id="40b32-108">will be read under **normal context** as:</span></span>

   <span data-ttu-id="40b32-109">König George V I von England, starb am 6. Februar 19 52.</span><span class="sxs-lookup"><span data-stu-id="40b32-109">King George V I of England, died on February six, nineteen fifty-two.</span></span>

<span data-ttu-id="40b32-110">Unter dem **e-Mail-Kontext** wird Sie jedoch wie folgt gelesen:</span><span class="sxs-lookup"><span data-stu-id="40b32-110">But under **E-mail context**, it will be read as:</span></span>

   <span data-ttu-id="40b32-111">King George das sechste von England, verstarb am sechsten Februar 19 52.</span><span class="sxs-lookup"><span data-stu-id="40b32-111">King George the sixth of England, died on February sixth, nineteen fifty-two.</span></span>

<span data-ttu-id="40b32-112">Informationen zur Verwendung des kontexttags für den **Kontext** finden Sie in der Dokumentation zur agentprogrammierung [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="40b32-112">Information about using the **Context** speech tag can be found in the Agent programming documentation [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




