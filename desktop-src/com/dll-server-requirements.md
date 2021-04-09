---
title: DLL-Server Anforderungen
description: Obwohl die meisten DLLs in einem Ersatz Zeichen ausgeführt werden können, können einige DLLs nicht.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037616"
---
# <a name="dll-server-requirements"></a><span data-ttu-id="51942-103">DLL-Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51942-103">DLL Server Requirements</span></span>

<span data-ttu-id="51942-104">Obwohl die meisten DLLs in einem Ersatz Zeichen ausgeführt werden können, können einige DLLs nicht.</span><span class="sxs-lookup"><span data-stu-id="51942-104">While most DLLs can run in a surrogate, some DLLs cannot.</span></span>

<span data-ttu-id="51942-105">Die dll muss sich gut Verhalten, wenn Sie das vom System bereitgestellte Ersatz Zeichen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="51942-105">The DLL must be well-behaved if you want to use the system-supplied surrogate.</span></span> <span data-ttu-id="51942-106">Beispielsweise würde eine DLL, die Methoden aufruft, die Rückrufe vom Client registrieren, versuchen, diese Rückrufe so aufzurufen, als ob die Funktionszeiger, die Sie erhalten hat, Anweisungen in ihrem Adressraum hätten, was nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="51942-106">For example, a DLL that calls methods that register callbacks from the client would try to invoke those callbacks as if the function pointers it received were for instructions in its address space, which is not the case.</span></span> <span data-ttu-id="51942-107">Ebenso funktioniert eine DLL, die eine globale Variable verwendet, auf die der Client zugreift, nicht.</span><span class="sxs-lookup"><span data-stu-id="51942-107">Similarly, a DLL that uses a global variable that it expects the client to access would not work.</span></span> <span data-ttu-id="51942-108">Im Allgemeinen verhindern Parameter, die nicht ordnungsgemäß gemarshallt werden können, dass der DLL-Server außerhalb des Client Prozesses ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51942-108">In general, parameters that cannot be properly marshaled will prevent the DLL server from running outside the client process.</span></span> <span data-ttu-id="51942-109">In vielen Fällen können Sie ein benutzerdefiniertes Ersatz Zeichen schreiben, das speziell so entworfen wurde, dass es das "schlechte" Verhalten kompensiert.</span><span class="sxs-lookup"><span data-stu-id="51942-109">In many cases, you can write a custom surrogate specifically designed to compensate for "bad" behavior.</span></span> <span data-ttu-id="51942-110">(Weitere Informationen finden Sie unter [Schreiben eines benutzerdefinierten Ersatz](writing-a-custom-surrogate.md)Zeichens.)</span><span class="sxs-lookup"><span data-stu-id="51942-110">(For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).)</span></span>

<span data-ttu-id="51942-111">Wenn der DLL-Server benutzerdefinierte Schnittstellen verwendet, müssen Sie sicherstellen, dass Marshalling-Code für diese Schnittstellen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="51942-111">If the DLL server uses custom interfaces, you would have to ensure that marshaling code is available for those interfaces.</span></span> <span data-ttu-id="51942-112">Beispielsweise können Sie eine Proxy-dll erstellen und registrieren oder eine Typbibliothek bereitstellen und registrieren, die es dem Server ermöglicht, bei Ausführung in einem Ersatz Zeichen ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="51942-112">For example, you could build and register a proxy DLL or provide and register a type library that would allow the server to function correctly while running in a surrogate.</span></span>

<span data-ttu-id="51942-113">DLL-Server werden nur in einen Ersatzprozess geladen, der im richtigen Sicherheitskontext ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51942-113">DLL servers will be loaded only into a surrogate process running in the proper security context.</span></span> <span data-ttu-id="51942-114">Der Sicherheitskontext für den DLL-Server Ersatz wird auf die gleiche Weise wie für exe-Server bestimmt.</span><span class="sxs-lookup"><span data-stu-id="51942-114">The security context for the DLL server surrogate is determined in the same way as for EXE servers.</span></span> <span data-ttu-id="51942-115">Das dll-Server-Ersatz Zeichen wird im gleichen Sicherheitskontext wie der Client ausgeführt, es sei denn, ein **runas** -Wert, der den Sicherheitskontext bestimmt, wird im [AppID](appid-clsid.md) -Registrierungs Abschnitt für den Server festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51942-115">The DLL server surrogate runs in the same security context as the client, unless a **RunAs** value, which determines the security context, is set in the [AppID](appid-clsid.md) registry section for the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51942-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51942-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51942-117">DLL-Surrogates</span><span class="sxs-lookup"><span data-stu-id="51942-117">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




