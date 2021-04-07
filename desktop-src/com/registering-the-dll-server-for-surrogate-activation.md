---
title: Registrieren des dll-Servers für die ersatzaktivierung
description: Registrieren des dll-Servers für die ersatzaktivierung
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730465"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a><span data-ttu-id="e0b93-103">Registrieren des dll-Servers für die ersatzaktivierung</span><span class="sxs-lookup"><span data-stu-id="e0b93-103">Registering the DLL Server for Surrogate Activation</span></span>

<span data-ttu-id="e0b93-104">Ein dll-Server wird unter den folgenden Bedingungen in einen Ersatzprozess geladen:</span><span class="sxs-lookup"><span data-stu-id="e0b93-104">A DLL server will be loaded into a surrogate process under the following conditions:</span></span>

-   <span data-ttu-id="e0b93-105">Es muss ein AppID-Wert angegeben werden, der unter dem CLSID-Schlüssel in der Registrierung angegeben ist, und ein entsprechender [AppID](appid-key.md) -Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="e0b93-105">There must be an AppID value specified under the CLSID key in the registry, and a corresponding [AppID](appid-key.md) key.</span></span>
-   <span data-ttu-id="e0b93-106">Bei einem Aktivierungsbefehl ist das [**lokale CLSCTX- \_ \_ Server**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) Bit festgelegt, und der CLSID-Schlüssel gibt [LocalServer32](localserver32.md), [LocalServer](localserver.md)oder [LocalService](localservice.md)nicht an.</span><span class="sxs-lookup"><span data-stu-id="e0b93-106">In an activation call, the [**CLSCTX\_LOCAL\_SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) bit is set and the CLSID key does not specify [LocalServer32](localserver32.md), [LocalServer](localserver.md), or [LocalService](localservice.md).</span></span> <span data-ttu-id="e0b93-107">Wenn andere **CLSCTX** -Bits festgelegt sind, wird der [**Verarbeitungs Algorithmus**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)für die in-Process-, local-oder remoteausführungsflags befolgt.</span><span class="sxs-lookup"><span data-stu-id="e0b93-107">If other **CLSCTX** bits are set, the [**processing algorithm**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)for the in-process, local, or remote execution flags is followed.</span></span>
-   <span data-ttu-id="e0b93-108">Der CLSID-Schlüssel enthält den [InProcServer32](inprocserver32.md) -Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e0b93-108">The CLSID key contains the [InprocServer32](inprocserver32.md) subkey.</span></span>
-   <span data-ttu-id="e0b93-109">Die im **InProcServer32** -Schlüssel angegebene Proxy-/Stub-dll ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e0b93-109">The proxy/stub DLL specified in the **InprocServer32** key exists.</span></span>
-   <span data-ttu-id="e0b93-110">Der Wert von " [dllersatz](dllsurrogate.md) " ist unter dem Schlüssel " **AppID** " vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e0b93-110">The [DllSurrogate](dllsurrogate.md) value exists under the **AppID** key.</span></span>

<span data-ttu-id="e0b93-111">Wenn ein **LocalServer**-, **LocalServer32**-oder **LocalService-Dienst** vorhanden ist, der angibt, dass eine exe-Datei vorhanden ist, wird der exe-Server oder-Dienst immer im Gegensatz zum Laden eines dll-Servers in einen Ersatzprozess gestartet.</span><span class="sxs-lookup"><span data-stu-id="e0b93-111">If there is a **LocalServer**, **LocalServer32**, or **LocalService**, indicating the existence of an EXE, the EXE server or service will always be launched in preference to loading a DLL server into a surrogate process.</span></span>

<span data-ttu-id="e0b93-112">Für den Ersatz der Ersatz Zeichen Aktivierung muss der benannte Wert von " **dllersatz** " angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0b93-112">The **DllSurrogate** named-value must be specified for surrogate activation to occur.</span></span> <span data-ttu-id="e0b93-113">Die Aktivierung bezieht sich auf Aufrufe einer der folgenden Aktivierungs Funktionen:</span><span class="sxs-lookup"><span data-stu-id="e0b93-113">Activation refers to calls to any of the following activation functions:</span></span>

-   [<span data-ttu-id="e0b93-114">**CoGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="e0b93-114">**CoGetClassObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [<span data-ttu-id="e0b93-115">**Cokreateingestanceex**</span><span class="sxs-lookup"><span data-stu-id="e0b93-115">**CoCreateInstanceEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [<span data-ttu-id="e0b93-116">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="e0b93-116">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [<span data-ttu-id="e0b93-117">**Cogetinstancefromistorage**</span><span class="sxs-lookup"><span data-stu-id="e0b93-117">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [<span data-ttu-id="e0b93-118">**IMoniker:: bindtoken Object**</span><span class="sxs-lookup"><span data-stu-id="e0b93-118">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

<span data-ttu-id="e0b93-119">Um eine Instanz des vom System bereitgestellten Ersatz Zeichens zu starten, legen Sie den Wert von **dllersatz** entweder auf eine leere Zeichenfolge oder auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="e0b93-119">To launch an instance of the system-supplied surrogate, set the value of **DllSurrogate** either to an empty string or to **NULL**.</span></span> <span data-ttu-id="e0b93-120">Um den Start eines benutzerdefinierten Ersatz Zeichens anzugeben, legen Sie den Wert auf den Pfad des Ersatz Zeichens fest.</span><span class="sxs-lookup"><span data-stu-id="e0b93-120">To specify the launch of a custom surrogate, set the value to the path of the surrogate.</span></span>

<span data-ttu-id="e0b93-121">Wenn sowohl [Remoteservername](remoteservername.md) als auch **dllersatz** für dieselbe AppID angegeben werden, wird der **Remoteservername** -Wert ignoriert, und der Wert **dllersatz** bewirkt eine Aktivierung auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="e0b93-121">If both [RemoteServerName](remoteservername.md) and **DllSurrogate** are specified for the same AppID, the **RemoteServerName** value is ignored and the **DllSurrogate** value causes an activation on the local computer.</span></span> <span data-ttu-id="e0b93-122">Geben Sie für die Remote Ersatz Aktivierung den **Namen Remoteservername** , aber nicht **dllersatz** auf dem Client an, und geben Sie **dllersatz** auf dem Server an.</span><span class="sxs-lookup"><span data-stu-id="e0b93-122">For remote surrogate activation, specify **RemoteServerName** but not **DllSurrogate** on the client, and specify **DllSurrogate** on the server.</span></span>

<span data-ttu-id="e0b93-123">Ein dll-Server, der so konzipiert ist, dass er immer allein im eigenen Ersatzprozess ausgeführt wird, ist am besten mit einer AppID konfiguriert, die seiner CLSID entspricht.</span><span class="sxs-lookup"><span data-stu-id="e0b93-123">A DLL server that is designed to always run alone in its own surrogate process is best configured with an AppID equal its CLSID.</span></span> <span data-ttu-id="e0b93-124">Geben Sie unter " **AppID**" einfach einen **dllersatz** -Wert mit dem Namen "-Value" und einem leeren Zeichen folgen Wert</span><span class="sxs-lookup"><span data-stu-id="e0b93-124">Under **AppID**, simply specify a **DllSurrogate** named-value with an empty string value.</span></span>

<span data-ttu-id="e0b93-125">Es empfiehlt sich, einen dll-Server zu konfigurieren, der ausschließlich in einem eigenen Ersatzprozess ausgeführt werden soll, und mehrere Clients in einem Netzwerk mit einem [runas](runas.md) -Wert zu verarbeiten, der unter dem **AppID** -Registrierungsschlüssel angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e0b93-125">It is best to configure a DLL server that is designed to run alone in its own surrogate process and to service multiple clients across a network with a [RunAs](runas.md) value specified under the **AppID** registry key.</span></span> <span data-ttu-id="e0b93-126">Ob die **runas** "Interactive User" oder eine bestimmte Benutzeridentität angeben, hängt von der Benutzeroberfläche, der Sicherheit und anderen Serveranforderungen ab.</span><span class="sxs-lookup"><span data-stu-id="e0b93-126">Whether the **RunAs** specifies "Interactive User" or a specific user identity depends upon the user interface, security, and other server requirements.</span></span> <span data-ttu-id="e0b93-127">Wenn ein **runas** -Wert angegeben wird, wird nur eine Instanz des Servers geladen, um alle Clients zu bedienen, unabhängig von der Identität des Clients.</span><span class="sxs-lookup"><span data-stu-id="e0b93-127">When a **RunAs** value is specified, only one instance of the server is loaded to service all of the clients, regardless of the identity of the client.</span></span> <span data-ttu-id="e0b93-128">Konfigurieren Sie den Server auf der anderen Seite nicht mit **runas** , wenn die Absicht besteht, eine Instanz des dll-Servers als Ersatz für jede Remote Client Identität zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0b93-128">On the other hand, do not configure the server with **RunAs** if the intention is to have one instance of the DLL server running in surrogate to service each remote client identity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0b93-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0b93-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0b93-130">DLL-Server Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0b93-130">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="e0b93-131">Freigabe von Ersatz Zeichen</span><span class="sxs-lookup"><span data-stu-id="e0b93-131">Surrogate Sharing</span></span>](surrogate-sharing.md)
</dt> </dl>

 

 