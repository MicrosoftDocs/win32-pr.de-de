---
description: In den folgenden Abschnitten werden häufige Probleme beschrieben, die Entwickler beim Erstellen einer WMI-Remote Verbindung haben können.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Problembehandlung bei einer Remote-WMI-Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345237"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a><span data-ttu-id="30202-103">Problembehandlung bei einer Remote-WMI-Verbindung</span><span class="sxs-lookup"><span data-stu-id="30202-103">Troubleshooting a Remote WMI Connection</span></span>

<span data-ttu-id="30202-104">In den folgenden Abschnitten werden häufige Probleme beschrieben, die Entwickler beim Erstellen einer WMI-Remote Verbindung haben können.</span><span class="sxs-lookup"><span data-stu-id="30202-104">The following sections describe common issues developers may have with creating a remote WMI connection.</span></span>

<span data-ttu-id="30202-105">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="30202-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="30202-106">DCOM-Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="30202-106">DCOM Access Denied</span></span>](#dcom-access-denied)
-   [<span data-ttu-id="30202-107">Fehler beim Herstellen der Verbindung</span><span class="sxs-lookup"><span data-stu-id="30202-107">Failure to Connect</span></span>](#failure-to-connect)
-   [<span data-ttu-id="30202-108">Timeout bei WMI-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="30202-108">WMI Connection Timed Out</span></span>](#wmi-connection-timed-out)
-   [<span data-ttu-id="30202-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30202-109">Related topics</span></span>](#related-topics)

## <a name="dcom-access-denied"></a><span data-ttu-id="30202-110">DCOM-Zugriff verweigert</span><span class="sxs-lookup"><span data-stu-id="30202-110">DCOM Access Denied</span></span>

<dl> <dt>

<span data-ttu-id="30202-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span><span class="sxs-lookup"><span data-stu-id="30202-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="30202-112">bei der Verbindung ist der Fehler "DCOM-Zugriff verweigert" zusammen mit dem Dezimalwert-2147024891 oder Hex value0x80070005 aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="30202-112">your connection failed with the error "DCOM Access Denied", along with the decimal value -2147024891 or hex value0x80070005.</span></span>

</dd> <dt>

<span data-ttu-id="30202-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Betrifft</span><span class="sxs-lookup"><span data-stu-id="30202-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="30202-114">DCOM kann nicht konfiguriert werden, um eine WMI-Verbindung zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="30202-114">DCOM may not be configured to allow a WMI connection.</span></span>

</dd> <dt>

<span data-ttu-id="30202-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Lösungs</span><span class="sxs-lookup"><span data-stu-id="30202-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="30202-116">Sie können DCOM-Einstellungen für WMI mithilfe des DCOM-Konfigurations Hilfsprogramms (**DCOMCnfg.exe**) konfigurieren, das Sie in der **Systemsteuerung** unter **Verwaltung** finden.</span><span class="sxs-lookup"><span data-stu-id="30202-116">You can configure DCOM settings for WMI using the DCOM Config utility (**DCOMCnfg.exe**) found in **Administrative Tools** in **Control Panel**.</span></span> <span data-ttu-id="30202-117">Dieses Hilfsprogramm macht die Einstellungen verfügbar, mit denen bestimmte Benutzer eine Remote Verbindung mit dem Computer über DCOM herstellen können.</span><span class="sxs-lookup"><span data-stu-id="30202-117">This utility exposes the settings that enable certain users to connect to the computer remotely through DCOM.</span></span> <span data-ttu-id="30202-118">Mitglieder der Gruppe "Administratoren" können standardmäßig eine Remote Verbindung mit dem Computer herstellen.</span><span class="sxs-lookup"><span data-stu-id="30202-118">Members of the Administrators group are allowed to remotely connect to the computer by default.</span></span> <span data-ttu-id="30202-119">Mit diesem Hilfsprogramm können Sie die Sicherheit festlegen, um den WMI-Dienst zu starten, darauf zuzugreifen und ihn zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30202-119">With this utility you can set the security to start, access, and configure the WMI service.</span></span>

<span data-ttu-id="30202-120">Weitere Informationen finden Sie unter [Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="30202-120">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

</dd> </dl>

## <a name="failure-to-connect"></a><span data-ttu-id="30202-121">Fehler beim Herstellen der Verbindung</span><span class="sxs-lookup"><span data-stu-id="30202-121">Failure to Connect</span></span>

<dl> <dt>

<span data-ttu-id="30202-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span><span class="sxs-lookup"><span data-stu-id="30202-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="30202-123">Es ist nicht möglich, eine Verbindung mit WMI auf einem Remote System herzustellen.</span><span class="sxs-lookup"><span data-stu-id="30202-123">You cannot connect to WMI on a remote system.</span></span>

</dd> <dt>

<span data-ttu-id="30202-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Betrifft</span><span class="sxs-lookup"><span data-stu-id="30202-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="30202-125">Möglicherweise versuchen Sie, eine Verbindung mit einem System herzustellen, das WMI nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30202-125">You may be trying to connect to a system that does not support WMI.</span></span> <span data-ttu-id="30202-126">Die folgenden Verbindungen zwischen Betriebssystemversionen werden nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="30202-126">The following connections between operating system versions are not supported:</span></span>

-   <span data-ttu-id="30202-127">Sie können keine Verbindung mit einem Computer herstellen, auf dem eine Starter-, Basic-oder Home-Edition ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30202-127">You cannot connect to a computer that is running a Starter, Basic, or Home edition.</span></span>

<span data-ttu-id="30202-128">Alternativ können Sie versuchen, eine Verbindung mit einem Namespace herzustellen, für den eine verschlüsselte Verbindung erforderlich ist, die eine Authentifizierungs Ebene von `pktPrivacy` , **wbemauthenticationlevelpzprivacy** oder **RPC \_ C \_ authn \_ Level \_ Pkt \_ Privacy** erfordert.</span><span class="sxs-lookup"><span data-stu-id="30202-128">Alternately, you may be trying to connect to a namespace which requires an encrypted connection, one that requires an authentication level of `pktPrivacy`, **WbemAuthenticationLevelPktPrivacy**, or **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

</dd> <dt>

<span data-ttu-id="30202-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Lösungs</span><span class="sxs-lookup"><span data-stu-id="30202-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="30202-130">Weitere Informationen finden Sie unter [Sichern von WMI-Namespaces](securing-wmi-namespaces.md), [Sichern von C++-Clients und-Anbietern](securing-c---clients-and-providers.md)oder [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="30202-130">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

</dd> </dl>

## <a name="wmi-connection-timed-out"></a><span data-ttu-id="30202-131">Timeout bei WMI-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="30202-131">WMI Connection Timed Out</span></span>

<dl> <dt>

<span data-ttu-id="30202-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span><span class="sxs-lookup"><span data-stu-id="30202-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="30202-133">Timeout bei der WMI-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="30202-133">Your WMI connection times out.</span></span>

</dd> <dt>

<span data-ttu-id="30202-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Betrifft</span><span class="sxs-lookup"><span data-stu-id="30202-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="30202-135">Aufgrund von Problemen mit der Netzwerkverzögerung kann der Computer nicht rechtzeitig antworten.</span><span class="sxs-lookup"><span data-stu-id="30202-135">Due to network lag issues, the computer is simply not able to respond in time.</span></span>

</dd> <dt>

<span data-ttu-id="30202-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Lösungs</span><span class="sxs-lookup"><span data-stu-id="30202-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="30202-137">Beim Herstellen einer Verbindung mit WMI durch einen Aufruf von "WS [**. ConnectServer**](swbemlocator-connectserver.md) " oder " [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)" können Sie das Flag " **wbemconnectflagusemaxwait** " (Skripterstellung) oder das **WBEM- \_ Flag " \_ \_ use \_ Max \_ Wait** in C++ Value" auf "128 (0x80)" festlegen, um einen zwei (2) Timeout</span><span class="sxs-lookup"><span data-stu-id="30202-137">When connecting to WMI through a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) or [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), you can set the **wbemConnectFlagUseMaxWait** flag (scripting) or the **WBEM\_FLAG\_CONNECT\_USE\_MAX\_WAIT** in C++ value to 128 (0x80) to impose a two (2) minute time-out on the call.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="30202-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30202-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30202-139">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="30202-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



