---
title: Entwickeln eines Anbieters
description: Um die Ereignisse zu schreiben, die Sie im Manifest definieren, verwenden Sie die Funktionen der API für die Ereignis Ablauf Verfolgung (ETW). Ausführliche Informationen zum Schreiben eines Anbieters finden Sie unter Bereitstellen von Ereignissen.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102206"
---
# <a name="developing-a-provider"></a><span data-ttu-id="4870f-104">Entwickeln eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="4870f-104">Developing a Provider</span></span>

<span data-ttu-id="4870f-105">Um die Ereignisse zu schreiben, die Sie im Manifest definieren, verwenden Sie die Funktionen der API für die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="4870f-105">To write the events that you define in your manifest, you use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span> <span data-ttu-id="4870f-106">Ausführliche Informationen zum Schreiben eines Anbieters finden Sie unter [Bereitstellen von Ereignissen](/windows/desktop/ETW/providing-events).</span><span class="sxs-lookup"><span data-stu-id="4870f-106">For details on writing a provider, see [Providing Events](/windows/desktop/ETW/providing-events).</span></span>

<span data-ttu-id="4870f-107">Nachdem Sie den Anbieter geschrieben haben, können Sie den Anbieter und das Schema mit dem WevtUtil.exe Tool registrieren.</span><span class="sxs-lookup"><span data-stu-id="4870f-107">After writing the provider, use the WevtUtil.exe tool to register the provider and schema.</span></span> <span data-ttu-id="4870f-108">Weitere Informationen zur Verwendung von wevtutil finden Sie unter [Windows-Ereignisprotokoll Tools](windows-event-log-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4870f-108">For details on using WevtUtil, see [Windows Event Log Tools](windows-event-log-tools.md).</span></span> <span data-ttu-id="4870f-109">Im folgenden wird gezeigt, wie wevtutil verwendet wird, um einen Anbieter zu registrieren und die Registrierung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4870f-109">The following shows how to use WevtUtil to register a provider and to remove the registration.</span></span>


```cmd
wevtutil im provider.man

wevtutil um provider.man
```