---
title: Server-Side Sicherheit
description: Server-Side Sicherheit
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949151"
---
# <a name="server-side-security"></a><span data-ttu-id="d3e3e-103">Server-Side Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d3e3e-103">Server-Side Security</span></span>

<span data-ttu-id="d3e3e-104">Der Server kann mithilfe der Methoden von [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity)Sicherheitsinformationen über einen Aufrufer abrufen oder die Identität des Aufrufers annehmen.</span><span class="sxs-lookup"><span data-stu-id="d3e3e-104">The server can retrieve security information about a caller or impersonate the caller by using the methods of [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span></span> <span data-ttu-id="d3e3e-105">Eine Implementierung von **IServerSecurity** wird von com für das Kontext Objekt für den aktuellen-Befehl bereitgestellt, wenn Standard-Marshalling verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3e3e-105">An implementation of **IServerSecurity** is supplied by COM on the context object for the current call when standard marshaling is used.</span></span> <span data-ttu-id="d3e3e-106">Diese Schnittstelle ist jedoch möglicherweise nicht für einige benutzerdefinierte gemarshallte Schnittstellen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d3e3e-106">However, this interface may be absent for some custom-marshaled interfaces.</span></span>

<span data-ttu-id="d3e3e-107">Wenn ein Anruf beim Server eingeht, kann der Server [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) aufrufen, um einen Zeiger auf die [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d3e3e-107">When a call arrives at the server, the server can call [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to the [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface.</span></span> <span data-ttu-id="d3e3e-108">Mit diesem Zeiger können die **IServerSecurity** -Methoden vom Server aufgerufen werden, um herauszufinden, was die Authentifizierungs Einstellungen des Clients sind, und um bei Bedarf die Identität des Clients anzunehmen.</span><span class="sxs-lookup"><span data-stu-id="d3e3e-108">With this pointer, **IServerSecurity** methods can be called by the server to find out what the client's authentication settings are and to impersonate the client, if needed.</span></span> <span data-ttu-id="d3e3e-109">Das **IServerSecurity** -Objekt ist in jedem Thread im Apartment gültig, bis der von **IServerSecurity** dargestellte Befehl abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d3e3e-109">The **IServerSecurity** object is valid on any thread in the apartment until the call represented by **IServerSecurity** completes.</span></span> <span data-ttu-id="d3e3e-110">Weitere Informationen zum Identitätswechsel finden Sie unter Identitätswechsel [und-Verschleierung](impersonation.md) [.](cloaking.md)</span><span class="sxs-lookup"><span data-stu-id="d3e3e-110">For more information about impersonation, see [Impersonation](impersonation.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="d3e3e-111">Die folgenden Hilfsfunktionen, die auf der [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) -Schnittstellen Implementierung des callkontextobjekts basieren, sind ebenfalls verfügbar:</span><span class="sxs-lookup"><span data-stu-id="d3e3e-111">The following helper functions that rely on the call context object's [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface implementation are also available:</span></span>

-   [<span data-ttu-id="d3e3e-112">**Coqueryclientblanket**</span><span class="sxs-lookup"><span data-stu-id="d3e3e-112">**CoQueryClientBlanket**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [<span data-ttu-id="d3e3e-113">**CoImpersonateClient**</span><span class="sxs-lookup"><span data-stu-id="d3e3e-113">**CoImpersonateClient**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [<span data-ttu-id="d3e3e-114">**Coreverttself**</span><span class="sxs-lookup"><span data-stu-id="d3e3e-114">**CoRevertToSelf**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a><span data-ttu-id="d3e3e-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3e3e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3e3e-116">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="d3e3e-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 