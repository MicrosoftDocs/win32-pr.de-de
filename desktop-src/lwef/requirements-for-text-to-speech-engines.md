---
title: Anforderungen für Text-zu-Sprache-Engines
description: Anforderungen für Text-zu-Sprache-Engines
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471341"
---
# <a name="requirements-for-text-to-speech-engines"></a><span data-ttu-id="f55b6-103">Anforderungen für Text-zu-Sprache-Engines</span><span class="sxs-lookup"><span data-stu-id="f55b6-103">Requirements for Text-To-Speech Engines</span></span>

<span data-ttu-id="f55b6-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="f55b6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f55b6-105">Die Engine muss vollständig SAPI 4,0-kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="f55b6-105">The engine must be fully SAPI 4.0-compliant.</span></span> <span data-ttu-id="f55b6-106">Außerdem muss die Engine die folgenden SAPI-Schnittstellen für markierte Text-und Lesezeichen Benachrichtigungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f55b6-106">In addition, the engine must also support the following SAPI interfaces for tagged text and bookmark notifications.</span></span> <span data-ttu-id="f55b6-107">Diese Schnittstellen ermöglichen es dem Microsoft-Agent, die Ausgabe von Text an die Wort Sprechblase eines Zeichens zu beschleunigen und den Mund (oder die Entsprechung) des Zeichens mit den gesprochenen Wörtern zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f55b6-107">These interfaces enable Microsoft Agent to pace the output of text to a character's word balloon and lip-sync the character's mouth (or equivalent) with the spoken words.</span></span>

-   [<span data-ttu-id="f55b6-108">Ittscentralw</span><span class="sxs-lookup"><span data-stu-id="f55b6-108">ITTSCentralW</span></span>](ittscentralw.md)
-   [<span data-ttu-id="f55b6-109">Ittsnotifysinkw</span><span class="sxs-lookup"><span data-stu-id="f55b6-109">ITTSNotifySinkW</span></span>](ittsnotifysinkw.md)
-   [<span data-ttu-id="f55b6-110">Ittsbusnotifysinkw</span><span class="sxs-lookup"><span data-stu-id="f55b6-110">ITTSBufNotifySinkW</span></span>](ittsbufnotifysinkw.md)
-   [<span data-ttu-id="f55b6-111">Ittsattributesw</span><span class="sxs-lookup"><span data-stu-id="f55b6-111">ITTSAttributesW</span></span>](ittsattributesw.md)

 

 




