---
title: Freigabe von Ersatz Zeichen
description: DLL-Server geben ein Ersatz Zeichen frei, wenn Sie über übereinstimmende Sicherheits Identitäten verfügen und denselben AppID-Wert aufweisen.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709425"
---
# <a name="surrogate-sharing"></a><span data-ttu-id="6413e-103">Freigabe von Ersatz Zeichen</span><span class="sxs-lookup"><span data-stu-id="6413e-103">Surrogate Sharing</span></span>

<span data-ttu-id="6413e-104">DLL-Server geben ein Ersatz Zeichen frei, wenn Sie über übereinstimmende Sicherheits Identitäten verfügen und denselben AppID-Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6413e-104">DLL servers will share a surrogate if they have matching security identities and share the same AppID value.</span></span>

<span data-ttu-id="6413e-105">DLL-Server werden standardmäßig in ihren eigenen Ersatzprozess geladen.</span><span class="sxs-lookup"><span data-stu-id="6413e-105">DLL servers are loaded, by default, into their own surrogate process.</span></span> <span data-ttu-id="6413e-106">Wenn Sie andere DLL-Server in ein vorhandenes Ersatz Zeichen laden möchten, sodass mehr als ein dll-Server unterstützt wird, gibt es zwei Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="6413e-106">To load other DLL servers into an existing surrogate so that it supports more than one DLL server, there are two requirements:</span></span>

-   <span data-ttu-id="6413e-107">Die DLL-Server müssen denselben AppID-Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6413e-107">The DLL servers must have the same AppID value.</span></span>
-   <span data-ttu-id="6413e-108">Der Sicherheitskontext der DLL-Server muss identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6413e-108">The security context of the DLL servers must be the same.</span></span>

<span data-ttu-id="6413e-109">Wenn zwei dll-Server unter verschiedenen Sicherheits Identitäten gestartet werden sollen, müssen Sie sich in unterschiedlichen Surrogates befinden, unabhängig davon, ob Ihre APPIDs einander entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6413e-109">If two DLL servers are to be launched under different security identities, they must be in different surrogates, whether their AppIDs match.</span></span>

<span data-ttu-id="6413e-110">Im folgenden finden Sie ein Beispiel für die Verwaltung der Freigabe von Ersatz Zeichen mit APPIDs:</span><span class="sxs-lookup"><span data-stu-id="6413e-110">Following is an example of administering surrogate sharing with AppIDs:</span></span>

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

<span data-ttu-id="6413e-111">Die beiden CLSIDs für die DLL-Komponenten comp1.dll und comp2.dll für die gemeinsame Verwendung einer AppID konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="6413e-111">The two CLSIDs for DLL components comp1.dll and comp2.dll have been configured to share an AppID.</span></span> <span data-ttu-id="6413e-112">Der [AppID](appid-key.md) -Schlüssel gibt an, dass der DLL-Server in ein Ersatz Zeichen geladen werden kann, indem der [dllersatz](dllsurrogate.md) -Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6413e-112">The [AppID](appid-key.md) key specifies that the DLL server can be loaded in a surrogate by specifying the [DllSurrogate](dllsurrogate.md) value.</span></span> <span data-ttu-id="6413e-113">In diesem Beispiel ist der **dllersatz** -Wert eine leere Zeichenfolge, die angibt, dass die standardmäßige System Implementierung des dll-Ersatz Zeichens verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6413e-113">In this example, the **DllSurrogate** value is an empty string, indicating that the default system implementation of the DLL surrogate should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6413e-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6413e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6413e-115">DLL-Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6413e-115">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="6413e-116">Registrieren des dll-Servers für die ersatzaktivierung</span><span class="sxs-lookup"><span data-stu-id="6413e-116">Registering the DLL Server for Surrogate Activation</span></span>](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




