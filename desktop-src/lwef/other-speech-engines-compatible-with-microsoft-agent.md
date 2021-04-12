---
title: Andere mit dem Microsoft-Agent kompatible Sprach-Engines
description: Andere mit dem Microsoft-Agent kompatible Sprach-Engines
ms.assetid: fa87c592-c819-4dea-a1d0-6ccb25cc0bcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9855a0f5374d35634d02f808b46449a053cada9a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389964"
---
# <a name="other-speech-engines-compatible-with-microsoft-agent"></a><span data-ttu-id="5be96-103">Andere mit dem Microsoft-Agent kompatible Sprach-Engines</span><span class="sxs-lookup"><span data-stu-id="5be96-103">Other Speech Engines Compatible with Microsoft Agent</span></span>

<span data-ttu-id="5be96-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="5be96-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="5be96-105">Zusätzlich zu den Microsoft Speech Engines, die mit und Support von Microsoft Agent bereitgestellt werden, bieten zahlreiche Unternehmen auch Sprachmodule mit Unterstützung für den Microsoft-Agent.</span><span class="sxs-lookup"><span data-stu-id="5be96-105">In addition to the Microsoft speech engines that are provided with and support Microsoft Agent, a number of companies also offer speech engines with support for Microsoft Agent.</span></span> <span data-ttu-id="5be96-106">Auf dieser Seite erhalten Sie einen kurzen Überblick über die Module, die in US-Englisch und in anderen Sprachen verfügbar sein können.</span><span class="sxs-lookup"><span data-stu-id="5be96-106">This page gives you a brief overview of such engines that may be available in U.S. English and other languages.</span></span> <span data-ttu-id="5be96-107">Informationen zum Installieren und Zugreifen auf die Module und zum erneuten Verteilen der Module finden Sie auf ihren Websites.</span><span class="sxs-lookup"><span data-stu-id="5be96-107">Information about how to install and access, as well as license and redistribute the engines can be found at their websites.</span></span>

<span data-ttu-id="5be96-108">Wenn Sie die Sprach-Engine von Drittanbietern verwenden, müssen Sie auch Microsoft SAPI 4.0 als Lauf Zeit Binärdateien installieren, damit die Engines ordnungsgemäß aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="5be96-108">When using any third-party speech engine, you also need to install Microsoft SAPI 4.0a runtime binaries so that the engines are enumerated properly.</span></span> <span data-ttu-id="5be96-109">Auf der Webseite können Sie das folgende Tag einschließen, um einen autodownload der Speech-API zu initiieren:</span><span class="sxs-lookup"><span data-stu-id="5be96-109">From your webpage you can include the following tag to trigger an autodownload of the Speech API:</span></span>

``` syntax
<OBJECT WIDTH=0 HEIGHT=0
  CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
  CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

<span data-ttu-id="5be96-110">Weitere Informationen zu den SAPI-Lauf Zeit Binärdateien finden Sie auf der [Website der Microsoft-Sprachgruppe](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="5be96-110">For more information about the SAPI runtime binaries, refer to the [Microsoft Speech group's website](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="5be96-111">Der Microsoft-Agent installiert auch die SAPI-Runtime-Binärdateien mit der Microsoft-Spracherkennungs-Engine, der Sprachsystem Steuerung und dem agentzeicheneditor.</span><span class="sxs-lookup"><span data-stu-id="5be96-111">Microsoft Agent also installs the SAPI runtime binaries with the Microsoft Speech Recognition Engine, the Speech Control Panel, and the Agent Character Editor.</span></span>

<span data-ttu-id="5be96-112">Beachten Sie, dass diese Verknüpfungen auf Server verweisen, die nicht von Microsoft gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="5be96-112">Please note that these links point to servers that are not under Microsoft control.</span></span> <span data-ttu-id="5be96-113">Lesen Sie die offizielle Microsoft- [Erklärung](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) zu anderen Servern.</span><span class="sxs-lookup"><span data-stu-id="5be96-113">Please read the Microsoft [official statement](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) regarding other servers.</span></span> <span data-ttu-id="5be96-114">Microsoft unterstützt den Inhalt und die auf diesen Websites bereitgestellte Software nicht.</span><span class="sxs-lookup"><span data-stu-id="5be96-114">Microsoft does not endorse the content nor the software provided at these websites.</span></span> <span data-ttu-id="5be96-115">Alle technischen Fragen und Supportfragen sollten auch an die Lieferanten der Engines und nicht an Microsoft oder das Microsoft-agentteam geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="5be96-115">All technical and support questions should also be directed to the suppliers of the engines and not to Microsoft or the Microsoft Agent team.</span></span>

<span data-ttu-id="5be96-116">**Digalo-Text-zu-Sprache-Engine**</span><span class="sxs-lookup"><span data-stu-id="5be96-116">**Digalo Text-To-Speech Engine**</span></span>

<span data-ttu-id="5be96-117">Digalo ist eine erschwingliche TTS-Engine, die für Endbenutzer und Entwickler konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="5be96-117">Digalo is an affordable TTS engine designed for end-users and developers.</span></span> <span data-ttu-id="5be96-118">Die-Engine wird in einer Reihe von Sprachen angeboten: Französisch, Deutsch, Portugiesisch (Brasilien), Spanisch, Russisch und UK und US-Englisch mit Italienisch, Polnisch und anderen Sprachen, die bald verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5be96-118">The engine is offered in a number of languages: French, German, Portuguese (Brazil), Spanish, Russian, and UK and U.S. English, with Italian, Polish, and other languages coming soon.</span></span> <span data-ttu-id="5be96-119">Entwicklerinformationen sowie Details zur Registrierung von Endbenutzern und Partnerprogrammen sind ebenfalls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5be96-119">Developer information, as well as details on end-user registration and affiliate programs, is also available.</span></span>

<span data-ttu-id="5be96-120">**Elan-Sprachmodul**</span><span class="sxs-lookup"><span data-stu-id="5be96-120">**Elan Speech Engine**</span></span>

<span data-ttu-id="5be96-121">Die Elan-Sprach-Engine verwendet die Text-to-Speech-Technologie von Elan und ist in sieben Sprachen verfügbar: Französisch, Deutsch, Portugiesisch (Brasilien), Spanisch, Russisch, UK und US-Englisch.</span><span class="sxs-lookup"><span data-stu-id="5be96-121">Elan Speech Engine uses Elan's Text To Speech technology and is available in seven languages: French, German, Portuguese (Brazil), Spanish, Russian, UK and U.S. English.</span></span>

<span data-ttu-id="5be96-122">**IBM ViaVoice Outloud**</span><span class="sxs-lookup"><span data-stu-id="5be96-122">**IBM ViaVoice Outloud**</span></span>

<span data-ttu-id="5be96-123">IBM hat mehrere Microsoft-agentzeichen für die Verwendung mit ViaVoice Outloud entwickelt.</span><span class="sxs-lookup"><span data-stu-id="5be96-123">IBM has developed several Microsoft Agent characters for use with ViaVoice Outloud.</span></span> <span data-ttu-id="5be96-124">IBM ViaVoice Outloud ist eine Technologie für Text-zu-Sprache (Sprachsynthese) und ist in Französisch, Deutsch, Italienisch, Spanisch, Englisch (Großbritannien) und Englisch (USA) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5be96-124">IBM ViaVoice Outloud is a text-to-speech (speech synthesis) technology and is available in French, German, Italian, Spanish, UK English and U.S. English.</span></span> <span data-ttu-id="5be96-125">In Kombination mit dem Microsoft-Agent können Sie in vielen Sprachen lebendige Anwendungen erstellen und Ihre Verkaufschancen auf neue weltweiten Märkten ausweiten.</span><span class="sxs-lookup"><span data-stu-id="5be96-125">When combined with Microsoft Agent, you can create vibrant applications in many languages and extend your sales opportunities to new worldwide markets.</span></span>

 

 




