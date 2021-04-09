---
title: Sonstige RPC-Leistungs Tipps
description: In diesem Abschnitt werden verschiedene Leistungs Tipps zum Entwickeln von leistungsstarken RPC-Servern erläutert. Dieser Abschnitt enthält viele Tipps, die sich auf den RPC-Client beziehen. Wenn Sie einen RPC-Client ordnungsgemäß entwickeln, kann der RPC-Server weniger Arbeit ausführen.
ms.assetid: 82278f4b-1273-45e8-9078-ad919a4711f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b0b43f996cc0a165076f1d7aab1b69e6fb9b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036595"
---
# <a name="miscellaneous-rpc-performance-tips"></a><span data-ttu-id="05b9a-105">Sonstige RPC-Leistungs Tipps</span><span class="sxs-lookup"><span data-stu-id="05b9a-105">Miscellaneous RPC Performance Tips</span></span>

<span data-ttu-id="05b9a-106">In diesem Abschnitt werden verschiedene Leistungs Tipps zum Entwickeln von leistungsstarken RPC-Servern erläutert.</span><span class="sxs-lookup"><span data-stu-id="05b9a-106">This section discusses miscellaneous performance tips for developing high performance RPC servers.</span></span> <span data-ttu-id="05b9a-107">Dieser Abschnitt enthält viele Tipps, die sich auf den RPC-Client beziehen.</span><span class="sxs-lookup"><span data-stu-id="05b9a-107">This section provides many tips that refer to the RPC client.</span></span> <span data-ttu-id="05b9a-108">Wenn Sie einen RPC-Client ordnungsgemäß entwickeln, kann der RPC-Server weniger Arbeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="05b9a-108">Developing an RPC client properly enables the RPC server to perform less work.</span></span>

## <a name="use-kerberos"></a><span data-ttu-id="05b9a-109">Verwenden von Kerberos</span><span class="sxs-lookup"><span data-stu-id="05b9a-109">Use Kerberos</span></span>

<span data-ttu-id="05b9a-110">Wenn Sicherheit verwendet wird, verwenden Sie Kerberos.</span><span class="sxs-lookup"><span data-stu-id="05b9a-110">If security is used, use Kerberos.</span></span> <span data-ttu-id="05b9a-111">Auf der Serverseite ist für Kerberos kein Zugriff auf den KDC erforderlich.</span><span class="sxs-lookup"><span data-stu-id="05b9a-111">On the server side, Kerberos does not require access to the KDC.</span></span> <span data-ttu-id="05b9a-112">Dadurch wird die Arbeitsauslastung vom Server auf den Client verlagert, der Server mit besserer Leistung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="05b9a-112">This moves the workload from the server to the client, which provides better performing servers.</span></span>

## <a name="use-static-identity-tracking"></a><span data-ttu-id="05b9a-113">Statische Identitäts Überwachung verwenden</span><span class="sxs-lookup"><span data-stu-id="05b9a-113">Use Static Identity Tracking</span></span>

<span data-ttu-id="05b9a-114">Wenn Sicherheit verwendet wird, versuchen Sie, die statische Identitäts Überwachung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="05b9a-114">If security is used, try to use static identity tracking.</span></span> <span data-ttu-id="05b9a-115">Die statische Identitäts Verfolgung ist im Hinblick auf die Ressourcenverwendung günstiger als die dynamische Identitäts Überwachung.</span><span class="sxs-lookup"><span data-stu-id="05b9a-115">Static identity tracking is cheaper in terms of resource usage than dynamic identity tracking.</span></span> <span data-ttu-id="05b9a-116">Wenn sich die Client Identität ändert und der Server die Änderung nicht beachten sollte, verwenden Sie die dynamische Überwachung, anstatt ein anderes Bindungs Handle für jede Identität zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="05b9a-116">If the client identity changes, and the server should not be aware of the change, use dynamic tracking instead of creating a different binding handle for each identity.</span></span> <span data-ttu-id="05b9a-117">Wenn die Identität jedoch identisch ist, sollten Sie sicherstellen, dass RPC diese Tatsache kennt, um zu vermeiden, dass die RPC-Überprüfung auf geänderte Identitäten jedes Mal erfolgt.</span><span class="sxs-lookup"><span data-stu-id="05b9a-117">But if the identity is the same, ensure RPC is aware of that fact to avoid having RPC make checks for changed identity every time.</span></span>

## <a name="use-the-rpcgetauthorizationcontextforclient-function"></a><span data-ttu-id="05b9a-118">Verwenden der rpcgetauthorizationcontextforclient-Funktion</span><span class="sxs-lookup"><span data-stu-id="05b9a-118">Use the RpcGetAuthorizationContextForClient Function</span></span>

<span data-ttu-id="05b9a-119">Wenn Sie den Zugriff unter Windows XP überprüfen müssen, verwenden Sie die Funktion [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) .</span><span class="sxs-lookup"><span data-stu-id="05b9a-119">If you need to check access in Windows XP, use the [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) function.</span></span> <span data-ttu-id="05b9a-120">Die sich ergebenden Authz-Kontexte ermöglichen sehr schnelle Zugriffs Überprüfungen, die von der RPC-Laufzeit effizient zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="05b9a-120">The resulting Authz contexts enables very fast access checks, which are efficiently cached by the RPC run time.</span></span>

## <a name="do-not-modify-the-token-unless-necessary"></a><span data-ttu-id="05b9a-121">Ändern Sie das Token nur, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="05b9a-121">Do Not Modify the Token Unless Necessary</span></span>

<span data-ttu-id="05b9a-122">Wenn die dynamische Identitäts Verfolgung verwendet wird, sollten Sie das Thread-/Prozesstoken nur ändern, wenn dies unbedingt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="05b9a-122">If dynamic identity tracking is used, do not modify the thread/process token unless absolutely necessary.</span></span> <span data-ttu-id="05b9a-123">Auch wenn es in Einstellungen geändert wird, die es zuvor gab, unterscheidet sich das Token oft ausreichend vom Sicherheitssystem, um die Einrichtung eines neuen Sicherheits Kontexts zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="05b9a-123">Even if it is modified to settings it previously had, the token often is sufficiently different to the security system to trigger the establishment of a new security context.</span></span>

## <a name="consider-mixed-mode-serialization-for-context-handles"></a><span data-ttu-id="05b9a-124">Die Serialisierung im gemischten Modus für Kontext Handles wird berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="05b9a-124">Consider Mixed Mode Serialization for Context Handles</span></span>

<span data-ttu-id="05b9a-125">Der standardserialisierungsmodus für das Kontext Handle wird serialisiert (exklusiv).</span><span class="sxs-lookup"><span data-stu-id="05b9a-125">The default serialization mode for context handle is serialized (exclusive).</span></span> <span data-ttu-id="05b9a-126">Erstellen Sie ggf. alle Aufrufe, die den Zustand des Kontext Handles nicht ändern, im freigegebenen Serialisierungsmodus.</span><span class="sxs-lookup"><span data-stu-id="05b9a-126">Consider making all calls that do not modify the state of the context handle in shared serialization mode.</span></span> <span data-ttu-id="05b9a-127">Weitere Informationen finden Sie unter [**rpcsscontextlockexclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) .</span><span class="sxs-lookup"><span data-stu-id="05b9a-127">See [**RpcSsContextLockExclusive**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcsscontextlockexclusive) for more information.</span></span>

 

 




