---
title: Anforderungen für Spracherkennungs-Engines
description: Anforderungen für Spracherkennungs-Engines
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947967"
---
# <a name="requirements-for-speech-recognition-engines"></a><span data-ttu-id="d58e1-103">Anforderungen für Spracherkennungs-Engines</span><span class="sxs-lookup"><span data-stu-id="d58e1-103">Requirements for Speech Recognition Engines</span></span>

<span data-ttu-id="d58e1-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="d58e1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d58e1-105">Eine Spracherkennungs-Engine muss auch ein vollständig kompatibles Befehls-und Steuerungs Modul (c&c) gemäß SAPI 4,0 sein.</span><span class="sxs-lookup"><span data-stu-id="d58e1-105">A speech recognition engine must also be a fully compliant Command and Control (C&C) engine according to SAPI 4.0.</span></span> <span data-ttu-id="d58e1-106">Es muss mehrere Grammatiken in dem Binärformat unterstützen, das in der Spezifikation beschrieben ist, und diese Grammatiken in Echtzeit aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d58e1-106">It must support multiple grammars in the binary format described in the specification and allow those grammars to be activated or deactivated in real time.</span></span>

<span data-ttu-id="d58e1-107">Beachten Sie, dass SAPI 4,0 erfordert, dass Spracherkennungs-Engines das breit Zeichen, Unicode-Schnittstellen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d58e1-107">Note that SAPI 4.0 requires that speech recognition engines support the wide character, Unicode interfaces.</span></span> <span data-ttu-id="d58e1-108">Bei der Unterstützung dieser Schnittstellen sollte die Engine jedoch nicht von der Umstellung von Unicode-Daten in ANSI abhängig sein, da die Engine auf einigen Systemen möglicherweise nicht ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d58e1-108">However, in supporting these interfaces, the engine should not depend on converting Unicode data to ANSI, as the engine may not function correctly on some systems.</span></span> <span data-ttu-id="d58e1-109">Beispielsweise funktioniert ein japanisches Modul, das Unicode in ANSI konvertiert, möglicherweise nicht auf einem englischsprachigen Microsoft Windows 95-System.</span><span class="sxs-lookup"><span data-stu-id="d58e1-109">For example, a Japanese engine that converts Unicode to ANSI may not work on an English-language Microsoft Windows 95 system.</span></span>

<span data-ttu-id="d58e1-110">Damit die Engine als Microsoft-Agent-kompatibel betrachtet wird, muss Sie Ergebnis Objekte zurückgeben, nachdem ein Ausdruck erfolgreich erkannt wurde (über isrgramnotifysinkwh::P hrasefinish).</span><span class="sxs-lookup"><span data-stu-id="d58e1-110">In addition, to be considered Microsoft Agent-compliant, the engine must return results objects upon the successful recognition of a phrase (through ISRGramNotifySinkW::PhraseFinish).</span></span> <span data-ttu-id="d58e1-111">Diese Ergebnis Objekte müssen isrresbasic unterstützen, da die Spezifikation erfordert.</span><span class="sxs-lookup"><span data-stu-id="d58e1-111">These results objects must support ISRResBasic, as the specification requires.</span></span> <span data-ttu-id="d58e1-112">Außerdem sollten Sie isrresscore unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d58e1-112">In addition, they should support ISRResScore.</span></span> <span data-ttu-id="d58e1-113">Obwohl der Microsoft-Agent mit einem Modul ausgeführt wird, das nur isrresbasic unterstützt, oder sogar mit einem Modul, das keine Ergebnis Objekte zurückgibt, ist die Leistung in der Regel mit diesen Engines erheblich ärmer.</span><span class="sxs-lookup"><span data-stu-id="d58e1-113">Although Microsoft Agent will run with an engine that supports only ISRResBasic, or even with an engine that returns no results objects whatsoever, performance will usually be significantly poorer with such engines.</span></span> <span data-ttu-id="d58e1-114">Viele Anwendungen verwenden die von der-Engine bereitgestellten Konfidenz Werte, um zu steuern, wie Sie auf verschiedene Befehle reagieren.</span><span class="sxs-lookup"><span data-stu-id="d58e1-114">Many applications use the confidence values provided by the engine to control how they respond to various commands.</span></span>

 

 




