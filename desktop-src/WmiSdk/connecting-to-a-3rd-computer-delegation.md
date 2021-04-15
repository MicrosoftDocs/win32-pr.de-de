---
description: Wenn Sie ein Skript auf einem lokalen System ausführen, das Daten von einem Remote System abruft, stellt WMI Ihre Anmelde Informationen für den Anbieter der Daten auf dem Remote System bereit.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delegierung mit WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393866"
---
# <a name="delegating-with-wmi"></a><span data-ttu-id="f7a89-103">Delegierung mit WMI</span><span class="sxs-lookup"><span data-stu-id="f7a89-103">Delegating with WMI</span></span>

<span data-ttu-id="f7a89-104">Wenn Sie ein Skript auf einem lokalen System ausführen, das Daten von einem Remote System abruft, stellt WMI Ihre Anmelde Informationen für den Anbieter der Daten auf dem Remote System bereit.</span><span class="sxs-lookup"><span data-stu-id="f7a89-104">When you run a script on a local system that obtains data from a remote system, WMI supplies your credentials to the provider of the data on the remote system.</span></span> <span data-ttu-id="f7a89-105">Dies erfordert nur eine Identitätswechsel **Ebene des Identitäts** Wechsels, da nur ein Netzwerkhop erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f7a89-105">This requires only an impersonation level of **Impersonate**, because only one network hop is required.</span></span> <span data-ttu-id="f7a89-106">Wenn das Skript jedoch eine Verbindung mit WMI auf dem Remote System herstellt und versucht, eine Protokolldatei auf einem zusätzlichen Remote System zu öffnen, schlägt das Skript fehl, es sei denn, die Identitätswechsel **Ebene ist "** Delegat".</span><span class="sxs-lookup"><span data-stu-id="f7a89-106">However, if the script connects to WMI on the remote system and attempts to open a log file on an additional remote system, then the script fails unless the impersonation level is **Delegate**.</span></span> <span data-ttu-id="f7a89-107"> Die Identitätswechsel Ebene des Delegaten ist für jeden Vorgang erforderlich, der mehr als einen Netzwerkhop umfasst.</span><span class="sxs-lookup"><span data-stu-id="f7a89-107">**Delegate** impersonation level is required by any operation that involves more than one network hop.</span></span> <span data-ttu-id="f7a89-108">Weitere Informationen zur DCOM-Sicherheit in WMI finden Sie unter [Festlegen der Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="f7a89-108">For more information about DCOM security in WMI, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="f7a89-109">Weitere Informationen zu einer Verbindung mit einem Netzwerk Hop zwischen zwei Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f7a89-109">For more information about a one-network hop connection between two computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="f7a89-110">**So verwenden Sie die Delegierung für die Verbindung mit einem Computer über einen anderen Computer**</span><span class="sxs-lookup"><span data-stu-id="f7a89-110">**To use delegation to connect to a computer through another computer**</span></span>

1.  <span data-ttu-id="f7a89-111">Aktivieren Sie die Delegierung in Active Directory (**Active Directory Benutzer und Computer** in der **System Steuerungs** **Verwaltungsaufgabe**) auf dem Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="f7a89-111">Enable delegation in Active Directory (**Active Directory Users and Computers** in **Control Panel** **Administrative Tasks**) on the domain controller.</span></span> <span data-ttu-id="f7a89-112">Das Konto auf dem Remote System muss **für die Delegierung als vertrauenswürdig** gekennzeichnet sein, und das Konto auf dem lokalen System darf nicht als Konto vertraulich gekennzeichnet **und kann nicht delegiert** werden.</span><span class="sxs-lookup"><span data-stu-id="f7a89-112">The account on the remote system must be marked as **Trusted for delegation** and the account on the local system must not be marked as **Account is sensitive and cannot be delegated**.</span></span> <span data-ttu-id="f7a89-113">das lokale System, das Remote System und der Domänen Controller müssen Mitglieder derselben Domäne oder in vertrauenswürdigen Domänen sein.</span><span class="sxs-lookup"><span data-stu-id="f7a89-113">the local system, the remote system, and the domain controller must be members of the same domain or in trusted domains.</span></span>

    <span data-ttu-id="f7a89-114">**Hinweis**  Die Verwendung der Delegierung stellt ein Sicherheitsrisiko dar, da Prozesse außerhalb ihrer direkten Kontrolle die Möglichkeit zur Verwendung Ihrer Anmelde Informationen bieten.</span><span class="sxs-lookup"><span data-stu-id="f7a89-114">**Note**  Using delegation is a security risk because it gives processes outside of your direct control the ability to use your credentials.</span></span>

2.  <span data-ttu-id="f7a89-115">Ändern Sie den Code wie folgt, um anzugeben, dass Sie die Delegierung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f7a89-115">Modify your code in the following manner to indicate that you want to use delegation.</span></span>

    <dl> <dt>

    <span data-ttu-id="f7a89-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7a89-116"><span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell</span></span>
    </dt> <dd>

    <span data-ttu-id="f7a89-117">Legen Sie den Parameter-Identitäts **Wechsel für das** WMI *-* Cmdlet auf Delegat fest.</span><span class="sxs-lookup"><span data-stu-id="f7a89-117">Set the *-Impersonation* parameter on the WMI cmdlet to **Delegate**.</span></span>

    </dd> <dt>

    <span data-ttu-id="f7a89-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span><span class="sxs-lookup"><span data-stu-id="f7a89-118"><span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript</span></span>
    </dt> <dd>

    <span data-ttu-id="f7a89-119">Legen Sie den Parameter "Identitätswechsel *Ebene* " auf "Delegat" fest, indem Sie in der [Monikerzeichenfolge](constructing-a-moniker-string.md) auf " [Swap-Server](swbemlocator-connectserver.md) **" oder "** Delegat" **delegieren** .</span><span class="sxs-lookup"><span data-stu-id="f7a89-119">Set the *impersonationLevel* parameter to **Delegate** in the call to [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) or **Delegate** in the [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="f7a89-120">Sie können auch den Identitätswechsel in einem " [**Swap Security**](swbemsecurity.md)"-Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7a89-120">You can also set the impersonation in a [**SWbemSecurity**](swbemsecurity.md)object.</span></span>

    </dd> <dt>

    <span data-ttu-id="f7a89-121"><span id="C__"></span><span id="c__"></span>C++</span><span class="sxs-lookup"><span data-stu-id="f7a89-121"><span id="C__"></span><span id="c__"></span>C++</span></span>
    </dt> <dd>

    <span data-ttu-id="f7a89-122">Legen Sie im Aufruf von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) oder [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)den Parameter für die Identitätswechsel Ebene auf den **RPC-C- \_ \_ IMP- \_ Ebenen \_** -Delegaten fest.</span><span class="sxs-lookup"><span data-stu-id="f7a89-122">Set the impersonation level parameter to **RPC\_C\_IMP\_LEVEL\_DELEGATE** in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="f7a89-123">Weitere Informationen dazu, wann diese Aufrufe durchführen werden sollten, finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="f7a89-123">For more information about when to make these calls, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="f7a89-124">Um die Client Identität an Remote-com-Server in C++ zu übergeben, legen Sie das Cloaking im Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)fest.</span><span class="sxs-lookup"><span data-stu-id="f7a89-124">To pass the client identity to remote COM servers in C++, set cloaking in the call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span> <span data-ttu-id="f7a89-125">Weitere Informationen finden Sie unter [Cloaking](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="f7a89-125">For more information, see [Cloaking](../com/cloaking.md).</span></span>

    </dd> </dl>

## <a name="examples"></a><span data-ttu-id="f7a89-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7a89-126">Examples</span></span>

<span data-ttu-id="f7a89-127">Das folgende Codebeispiel zeigt eine Monikerzeichenfolge, die den Identitätswechsel zum Delegaten **festlegt.**</span><span class="sxs-lookup"><span data-stu-id="f7a89-127">The following code example shows a moniker string that sets the impersonation to **Delegate**.</span></span> <span data-ttu-id="f7a89-128">Beachten Sie, dass die Autorität auf Kerberos festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f7a89-128">Be aware that the authority must be set to Kerberos.</span></span>


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



<span data-ttu-id="f7a89-129">Im folgenden Codebeispiel wird veranschaulicht, wie der Identitätswechsel **mithilfe von "** [**Swap-Server**](swbemlocator-connectserver.md)" (ein Wert von 4) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f7a89-129">The following code example shows how to set impersonation to **Delegate** (a value of 4) using [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a><span data-ttu-id="f7a89-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7a89-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7a89-131">Sichern einer Remote-WMI-Verbindung</span><span class="sxs-lookup"><span data-stu-id="f7a89-131">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="f7a89-132">Erstellen von Prozessen per Remote Verbindung mit WMI</span><span class="sxs-lookup"><span data-stu-id="f7a89-132">Creating Processes Remotely with WMI</span></span>](creating-processes-remotely.md)
</dt> </dl>

 

 
