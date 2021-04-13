---
title: VCM-Architektur
description: VCM-Architektur
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video für Windows (Vfw), VCM-Architektur
- VFW (Video für Windows), VCM-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310568"
---
# <a name="vcm-architecture"></a><span data-ttu-id="da95b-105">VCM-Architektur</span><span class="sxs-lookup"><span data-stu-id="da95b-105">VCM Architecture</span></span>

<span data-ttu-id="da95b-106">VCM ist ein Vermittler zwischen einer Anwendung und Komprimierungs-und Komprimierungs Treibern.</span><span class="sxs-lookup"><span data-stu-id="da95b-106">VCM is an intermediary between an application and compression and decompression drivers.</span></span> <span data-ttu-id="da95b-107">Die Komprimierungs-und die Komprimierungs Treiber komprimieren und decokomprimieren einzelne Datenrahmen.</span><span class="sxs-lookup"><span data-stu-id="da95b-107">The compression and decompression drivers compress and decompress individual frames of data.</span></span>

<span data-ttu-id="da95b-108">Wenn eine Anwendung VCM aufruft, übersetzt VCM den-Rückruf in eine-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="da95b-108">When an application makes a call to VCM, VCM translates the call into a message.</span></span> <span data-ttu-id="da95b-109">Die Nachricht wird mithilfe der [**icsendmessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) -Funktion an den entsprechenden Kompressor oder Dekompressor gesendet, der die Daten komprimiert oder dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="da95b-109">The message is sent by using the [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) function to the appropriate compressor or decompressor, which compresses or decompresses the data.</span></span> <span data-ttu-id="da95b-110">VCM empfängt den Rückgabewert des Komprimierungs-oder Entkomprimierungs Treibers und gibt dann die Steuerung an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="da95b-110">VCM receives the return value from the compression or decompression driver and then returns control to the application.</span></span>

<span data-ttu-id="da95b-111">Wenn für eine Nachricht ein Makro definiert ist, wird das Makro zu einem **icsendmessage** -Funktions aufrufswert erweitert, der entsprechende Parameter für diese Nachricht bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="da95b-111">If a macro is defined for a message, the macro expands to an **ICSendMessage** function call supplying appropriate parameters for that message.</span></span> <span data-ttu-id="da95b-112">Wenn für eine Nachricht ein Makro definiert ist, sollte Sie von Ihrer Anwendung anstelle der Nachricht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da95b-112">If a macro is defined for a message, your application should use it rather than the message.</span></span> <span data-ttu-id="da95b-113">In dieser Übersicht folgen diese Makros Nachrichten in Klammern.</span><span class="sxs-lookup"><span data-stu-id="da95b-113">In this overview, these macros follow messages in parentheses.</span></span>

 

 




