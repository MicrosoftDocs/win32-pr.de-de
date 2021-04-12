---
title: Ausschalten der Rückruf Sicherheit
description: Die Sicherheitseinstellungen für Anrufe bestimmen, ob ein Client über die Berechtigung verfügt, die Methoden eines Servers aufzurufen. Es gibt zwei Möglichkeiten, die Aufruf Sicherheit zu deaktivieren. dazu gehört das Verwenden von Dcomcnfg.exe, um die Registrierung zu ändern, und das andere erfordert Aufrufe von CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388082"
---
# <a name="turning-off-call-security"></a><span data-ttu-id="86395-104">Ausschalten der Rückruf Sicherheit</span><span class="sxs-lookup"><span data-stu-id="86395-104">Turning Off Call Security</span></span>

<span data-ttu-id="86395-105">Die Sicherheitseinstellungen für Anrufe bestimmen, ob ein Client über die Berechtigung verfügt, die Methoden eines Servers aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="86395-105">Call security determines whether a client has permission to call a server's methods.</span></span> <span data-ttu-id="86395-106">Es gibt zwei Möglichkeiten, die Aufruf Sicherheit zu deaktivieren: eine erfordert die Verwendung von Dcomcnfg.exe, um die Registrierung zu ändern, und die andere erfordert Aufrufe von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="86395-106">There are two ways to disable call security: One involves using Dcomcnfg.exe to modify the registry, and the other requires calls to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

-   [<span data-ttu-id="86395-107">Ausschalten der Rückruf Sicherheit mithilfe von DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="86395-107">Turning Off Call Security Using DCOMCNFG</span></span>](#turning-off-call-security-using-dcomcnfg)
-   [<span data-ttu-id="86395-108">Programm gesteuertes Ausschalten der Rückruf Sicherheit</span><span class="sxs-lookup"><span data-stu-id="86395-108">Turning Off Call Security Programmatically</span></span>](#turning-off-call-security-programmatically)
-   [<span data-ttu-id="86395-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86395-109">Related topics</span></span>](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a><span data-ttu-id="86395-110">Ausschalten der Rückruf Sicherheit mithilfe von DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="86395-110">Turning Off Call Security Using DCOMCNFG</span></span>

<span data-ttu-id="86395-111">Die aufrufssicherheit kann am einfachsten mithilfe Dcomcnfg.exe deaktiviert werden, um die Registrierung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="86395-111">Call security can most easily be turned off by using Dcomcnfg.exe to modify the registry.</span></span> <span data-ttu-id="86395-112">Die Verwendung Dcomcnfg.exe zum Ausschalten der Sicherheit funktioniert jedoch nur, wenn sowohl der Client als auch der Server [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufruft.</span><span class="sxs-lookup"><span data-stu-id="86395-112">However, using Dcomcnfg.exe to turn security off will work only if both the client and the server do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="86395-113">Dies liegt daran, dass beim Aufrufen von **CoInitializeSecurity** die Registrierungs Einstellungen von DCOM ignoriert werden und stattdessen die für **CoInitializeSecurity** bereitgestellten Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86395-113">This is because when **CoInitializeSecurity** is called, DCOM ignores the registry settings and uses the values supplied to **CoInitializeSecurity** instead.</span></span>

<span data-ttu-id="86395-114">Zum Deaktivieren der Sicherheit mit Dcomcnfg.exe müssen sowohl der Client als auch der Server die Authentifizierungs Ebenen auf keine festlegen.</span><span class="sxs-lookup"><span data-stu-id="86395-114">To turn off security with Dcomcnfg.exe, both the client and the server must set their Authentication Levels to None.</span></span> <span data-ttu-id="86395-115">Die folgenden Schritte müssen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="86395-115">The following steps must be completed:</span></span>

1.  <span data-ttu-id="86395-116">Führen Sie "Dcomcnfg.exe" aus.</span><span class="sxs-lookup"><span data-stu-id="86395-116">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="86395-117">Wählen Sie auf der Seite **Anwendungen** die Anwendung aus, die den Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="86395-117">On the **Applications** page, select the application that represents the server.</span></span> <span data-ttu-id="86395-118">Klicken Sie auf die Schaltfläche **Eigenschaften** (oder Doppelklicken Sie auf die ausgewählte Anwendung).</span><span class="sxs-lookup"><span data-stu-id="86395-118">Click the **Properties** button (or double-click the selected application).</span></span>
3.  <span data-ttu-id="86395-119">Klicken Sie auf die Registerkarte **Allgemein**.</span><span class="sxs-lookup"><span data-stu-id="86395-119">Click the **General** tab.</span></span>
4.  <span data-ttu-id="86395-120">Wählen Sie im Listenfeld **Standard Authentifizierungs Ebene** die Option **(keine)** aus.</span><span class="sxs-lookup"><span data-stu-id="86395-120">From the **Default Authentication Level** list box, select **(None)**.</span></span>
5.  <span data-ttu-id="86395-121">Klicken Sie auf die Schaltfläche **anwenden** , um die Änderungen anzuwenden Änderungen werden jedoch nicht auf alle laufenden Instanzen der Anwendung angewendet.</span><span class="sxs-lookup"><span data-stu-id="86395-121">Click the **Apply** button to apply changes; however, changes are not applied to any running instances of the application.</span></span>
6.  <span data-ttu-id="86395-122">Wenn der Client in der Liste auf der Seite *Anwendungen* angezeigt wird, wiederholen Sie die Schritte 2 bis 5, und wählen Sie den Client anstelle des Servers für Schritt 2 aus.</span><span class="sxs-lookup"><span data-stu-id="86395-122">If the client appears on the list on the *Applications* page, repeat steps 2 through 5, choosing the client instead of the server for step 2.</span></span> <span data-ttu-id="86395-123">Klicken Sie dann auf die Schaltfläche **OK**.</span><span class="sxs-lookup"><span data-stu-id="86395-123">Then click the **OK** button.</span></span> <span data-ttu-id="86395-124">Wenn der Client nicht in der Liste enthalten ist, können Sie eine der folgenden drei Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="86395-124">If the client is not on the list, you can do one of the following three things:</span></span>
    -   <span data-ttu-id="86395-125">Mithilfe von Dcomcnfg.exe können Sie die Authentifizierungs Ebene des Clients auf Computer Ebene auf keine festlegen.</span><span class="sxs-lookup"><span data-stu-id="86395-125">You can set the client's Authentication Level to None on a computer-wide basis by using Dcomcnfg.exe.</span></span> <span data-ttu-id="86395-126">(Siehe die Warnung und das Verfahren weiter unten.)</span><span class="sxs-lookup"><span data-stu-id="86395-126">(See the warning and the procedure below.)</span></span>
    -   <span data-ttu-id="86395-127">Sie können die Authentifizierungs Ebene des Clients Programm gesteuert auf "None" festlegen.</span><span class="sxs-lookup"><span data-stu-id="86395-127">You can set the client's authentication level to None programmatically.</span></span>
    -   <span data-ttu-id="86395-128">Sie können einen [AppID](appid-key.md) -Schlüssel für den Client erstellen, um die Authentifizierungs Ebene "None" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="86395-128">You can create an [AppID](appid-key.md) key for the client to indicate an authentication level of None.</span></span> <span data-ttu-id="86395-129">(Siehe [festlegen Process-Wide Sicherheit über die Registrierung](setting-processwide-security-through-the-registry.md).)</span><span class="sxs-lookup"><span data-stu-id="86395-129">(See [Setting Process-Wide Security Through the Registry](setting-processwide-security-through-the-registry.md).)</span></span>

<span data-ttu-id="86395-130">So legen Sie die Authentifizierungs Ebene auf der Computer weiten Basis auf "None" fest:</span><span class="sxs-lookup"><span data-stu-id="86395-130">To set the Authentication Level to None on a computer-wide basis:</span></span>

> [!Note]  
> <span data-ttu-id="86395-131">Das Festlegen der Computer weiten Authentifizierungs Ebene auf None ist äußerst unsicher.</span><span class="sxs-lookup"><span data-stu-id="86395-131">Setting the computer-wide Authentication Level to None is extremely unsecure.</span></span>

 

1.  <span data-ttu-id="86395-132">Führen Sie "Dcomcnfg.exe" aus.</span><span class="sxs-lookup"><span data-stu-id="86395-132">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="86395-133">Wählen Sie die Registerkarte **Standardeigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="86395-133">Choose the **Default Properties** tab.</span></span>
3.  <span data-ttu-id="86395-134">Wählen Sie im Listenfeld **Standard Authentifizierungs Ebene** die Option **(keine)** aus.</span><span class="sxs-lookup"><span data-stu-id="86395-134">From the **Default Authentication Level** list box, choose **(None)**.</span></span>
4.  <span data-ttu-id="86395-135">Klicken Sie auf die Schaltfläche **OK** .</span><span class="sxs-lookup"><span data-stu-id="86395-135">Click the **OK** button.</span></span>

## <a name="turning-off-call-security-programmatically"></a><span data-ttu-id="86395-136">Programm gesteuertes Ausschalten der Rückruf Sicherheit</span><span class="sxs-lookup"><span data-stu-id="86395-136">Turning Off Call Security Programmatically</span></span>

<span data-ttu-id="86395-137">Um die Aufruf Sicherheit Programm gesteuert zu aktivieren, müssen sowohl der Client als auch der Server **CoInitializeSecurity** aufrufen und die Authentifizierungs Ebene im Parameter *dwauthnlevel* auf RPC \_ C \_ authn \_ Level \_ None festlegen.</span><span class="sxs-lookup"><span data-stu-id="86395-137">To turn call security off programmatically, both the client and the server must call **CoInitializeSecurity**, setting the authentication level in the *dwAuthnLevel* parameter to RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86395-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86395-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86395-139">Deaktivieren der Aktivierungs Sicherheit</span><span class="sxs-lookup"><span data-stu-id="86395-139">Turning Off Activation Security</span></span>](turning-off-activation-security.md)
</dt> </dl>

 

 




