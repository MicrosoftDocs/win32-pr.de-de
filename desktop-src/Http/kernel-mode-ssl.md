---
title: Kernelmodusssl
description: Kernelmodusssl
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- Kernelmodusssl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737ac7c6c25bac6e7b66d91aa967fc6fa550459b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340452"
---
# <a name="kernel-mode-ssl"></a><span data-ttu-id="bf14d-104">Kernelmodusssl</span><span class="sxs-lookup"><span data-stu-id="bf14d-104">Kernel Mode SSL</span></span>

<span data-ttu-id="bf14d-105">Der kernelmodusssl wurde in Windows Server 2003 mit Service Pack 1 (SP1) mit eingeschränkter Unterstützung eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bf14d-105">Kernel mode SSL was introduced in Windows Server 2003 with Service Pack 1 (SP1) with limited support.</span></span> <span data-ttu-id="bf14d-106">Für Computer, die unter Windows Server 2003 mit SP1 ausgeführt werden, muss ein Registrierungsschlüssel festgelegt werden, um Kernel-SSL zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf14d-106">For computers running on Windows Server 2003 with SP1 a registry key must be set to enable kernel SSL.</span></span> <span data-ttu-id="bf14d-107">Für Computer, die unter Windows Server 2008 und Windows Vista ausgeführt werden, wird eine vollständige Kernel Modus-Unterstützung für SSL bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bf14d-107">For computers running on Windows Server 2008 and Windows Vista, full kernel mode support for SSL is provided.</span></span>

<span data-ttu-id="bf14d-108">In den folgenden Abschnitten wird die SSL-Unterstützung im Kernel Modus beschrieben</span><span class="sxs-lookup"><span data-stu-id="bf14d-108">The following sections describe kernel mode SSL support:</span></span>

-   <span data-ttu-id="bf14d-109">Kernelmodusssl in Windows Server 2003 mit SP1</span><span class="sxs-lookup"><span data-stu-id="bf14d-109">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>
-   <span data-ttu-id="bf14d-110">Kernelmodusssl in Windows Server 2008 und Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf14d-110">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a><span data-ttu-id="bf14d-111">Kernelmodusssl in Windows Server 2003 mit SP1</span><span class="sxs-lookup"><span data-stu-id="bf14d-111">Kernel Modes SSL in Windows Server 2003 with SP1</span></span>

<span data-ttu-id="bf14d-112">In Windows Server 2003 mit SP1 bietet die HTTP-Server-API die Option zum Ausführen der SSL-Sicherheit im Kernel Modus (Benutzermodus SSL ist die Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="bf14d-112">In Windows Server 2003 with SP1, HTTP Server API provides the option of running SSL security in kernel mode (user mode SSL is the default).</span></span> <span data-ttu-id="bf14d-113">Die kernelmodusfunktion verbessert die SSL-Leistung durch Verschieben von Verschlüsselungs-und Entschlüsselungs Vorgängen in den Kernel, wodurch die Anzahl der Übergänge zwischen Kernel Modus und Benutzermodus verringert wird.</span><span class="sxs-lookup"><span data-stu-id="bf14d-113">The kernel mode feature improves SSL performance by moving encryption and decryption operations to the kernel, thus reducing the number of transitions between kernel mode and user mode.</span></span>

<span data-ttu-id="bf14d-114">Die folgenden Funktionen werden nicht unterstützt, wenn SSL im Kernel Modus ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="bf14d-114">The following features are not supported when SSL is run in kernel mode:</span></span>

-   <span data-ttu-id="bf14d-115">Clientzertifikate</span><span class="sxs-lookup"><span data-stu-id="bf14d-115">Client certificates</span></span>
-   <span data-ttu-id="bf14d-116">RC2-Chiffren</span><span class="sxs-lookup"><span data-stu-id="bf14d-116">RC2 ciphers</span></span>
-   <span data-ttu-id="bf14d-117">Das PCT 1,0-Protokoll</span><span class="sxs-lookup"><span data-stu-id="bf14d-117">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="bf14d-118">Änderungen der Server Zertifikat Konfiguration erfordern einen Neustart des HTTP-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="bf14d-118">Server certificate configuration changes require a restart of the HTTP service</span></span>
-   <span data-ttu-id="bf14d-119">Unterstützung für die Massen Verschlüsselung und-Auslagerung</span><span class="sxs-lookup"><span data-stu-id="bf14d-119">Bulk encryption and offload support</span></span>

## <a name="configuring-kernel-mode-ssl"></a><span data-ttu-id="bf14d-120">Konfigurieren des Kernel Modus-SSL</span><span class="sxs-lookup"><span data-stu-id="bf14d-120">Configuring Kernel Mode SSL</span></span>

<span data-ttu-id="bf14d-121">Der kernelmodusssl wird durch den Registrierungs Wert **EnableKernelSSL** gesteuert und aktiviert, indem der Wert auf 1 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bf14d-121">Kernel mode SSL is controlled by the **EnableKernelSSL** registry value and is enabled by setting the value to 1.</span></span> <span data-ttu-id="bf14d-122">Wenn Sie den kernelmodusssl aktivieren, wird SSL im Benutzermodus deaktiviert, und der HTTP-Dienst muss neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="bf14d-122">Enabling kernel mode SSL will disable user mode SSL and requires the HTTP service to be restarted to take effect.</span></span> <span data-ttu-id="bf14d-123">Der Registrierungsschlüssel " **EnableKernelSSL** " befindet sich unter:</span><span class="sxs-lookup"><span data-stu-id="bf14d-123">The **EnableKernelSSL** registry key is located at:</span></span>

<span data-ttu-id="bf14d-124">**HKEY \_ LOCAL \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **http** \\ **Parameters** \\ **EnableKernelSSL**</span><span class="sxs-lookup"><span data-stu-id="bf14d-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**HTTP**\\**Parameters**\\**EnableKernelSSL**</span></span>

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a><span data-ttu-id="bf14d-125">Kernelmodusssl in Windows Server 2008 und Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf14d-125">Kernel Mode SSL in Windows Server 2008 and Windows Vista</span></span>

<span data-ttu-id="bf14d-126">Für Computer, die unter Windows Server 2008 und Windows Vista ausgeführt werden, bietet die HTTP-Server-API erweiterte SSL-Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="bf14d-126">For computers running on Windows Server 2008 and Windows Vista, the HTTP Server API features enhanced SSL functionality.</span></span>

<span data-ttu-id="bf14d-127">Die folgenden neuen Features werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bf14d-127">The following new features are supported:</span></span>

-   <span data-ttu-id="bf14d-128">Vollständige Client Zertifikat Unterstützung im Kernel Modus-SSL</span><span class="sxs-lookup"><span data-stu-id="bf14d-128">Full client certificate support in kernel mode SSL</span></span>
-   <span data-ttu-id="bf14d-129">Kernelmodusssl für alle HTTP-SSL-Transaktionen</span><span class="sxs-lookup"><span data-stu-id="bf14d-129">Kernel mode SSL for all HTTP SSL transactions</span></span>
-   <span data-ttu-id="bf14d-130">Unterstützung für die Massen Verschlüsselung und-Auslagerung</span><span class="sxs-lookup"><span data-stu-id="bf14d-130">Bulk encryption and offload support</span></span>
-   <span data-ttu-id="bf14d-131">Das PCT 1,0-Protokoll</span><span class="sxs-lookup"><span data-stu-id="bf14d-131">The PCT 1.0 protocol</span></span>
-   <span data-ttu-id="bf14d-132">RC2-Chiffren</span><span class="sxs-lookup"><span data-stu-id="bf14d-132">RC2 ciphers</span></span>
-   <span data-ttu-id="bf14d-133">Bessere Leistung im Benutzermodus (SSL)</span><span class="sxs-lookup"><span data-stu-id="bf14d-133">Increased performance over user mode SSL</span></span>

## <a name="configuration"></a><span data-ttu-id="bf14d-134">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="bf14d-134">Configuration</span></span>

<span data-ttu-id="bf14d-135">Der kernelmodusssl kann durch zwei Registrierungs Werte unter dem Schlüssel "http-Parameter" konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="bf14d-135">Kernel mode SSL is configurable through two registry values under the HTTP Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

<span data-ttu-id="bf14d-136">Ein Benutzer muss über Administrator-/lokale System Berechtigungen verfügen, um die Registrierungs Werte zu ändern und die Protokolldateien und den Ordner zu ändern, in dem Sie enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bf14d-136">A user must have Administrator/Local System privileges to modify the registry values and view, or modify, the log files and the folder that contains them.</span></span>

<span data-ttu-id="bf14d-137">Konfigurationsinformationen in den Registrierungs Werten werden gelesen, wenn der HTTP-Server-API-Treiber gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="bf14d-137">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="bf14d-138">Wenn die Einstellungen geändert werden, muss der Treiber daher beendet und neu gestartet werden, um die neuen Werte zu lesen.</span><span class="sxs-lookup"><span data-stu-id="bf14d-138">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="bf14d-139">Dies kann mithilfe der folgenden Konsolenbefehle erreicht werden:</span><span class="sxs-lookup"><span data-stu-id="bf14d-139">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="bf14d-140">**NET stopphttp**</span><span class="sxs-lookup"><span data-stu-id="bf14d-140">**net stop http**</span></span>

<span data-ttu-id="bf14d-141">**NET Start http**</span><span class="sxs-lookup"><span data-stu-id="bf14d-141">**net start http**</span></span>

<span data-ttu-id="bf14d-142">In der folgenden Tabelle sind die Registrierungs Konfigurationswerte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf14d-142">The following table lists registry configuration values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf14d-143">Registrierungs Wert</span><span class="sxs-lookup"><span data-stu-id="bf14d-143">Registry Value</span></span></th>
<th><span data-ttu-id="bf14d-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf14d-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf14d-145">EnableKernelSSL</span><span class="sxs-lookup"><span data-stu-id="bf14d-145">EnableKernelSSL</span></span></td>
<td><span data-ttu-id="bf14d-146"><strong>Windows Server 2008 und Windows Vista:</strong> Dieser Registrierungs Wert ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="bf14d-146"><strong>Windows Server 2008 and Windows Vista:</strong> This registry value is obsolete.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf14d-147">Enablesslclosenotify</span><span class="sxs-lookup"><span data-stu-id="bf14d-147">EnableSslCloseNotify</span></span></td>
<td><span data-ttu-id="bf14d-148">Ein <strong>DWORD</strong> -Wert, der auf <strong>true</strong> festgelegt ist, um close-notify zu aktivieren, oder <strong>false</strong> , um die Anforderung für die schließende Benachrichtigung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf14d-148">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable close-notify, or <strong>FALSE</strong> to disable the close-notify requirement.</span></span> <span data-ttu-id="bf14d-149">Close-Notify ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf14d-149">Close-notify is disabled by default.</span></span><br/> <span data-ttu-id="bf14d-150">Wenn Close-notify aktiviert ist, muss die Client Anwendung vor dem Schließen von TCP-Verbindungen eine Nachricht mit dem Schluss benachrichtigen senden.</span><span class="sxs-lookup"><span data-stu-id="bf14d-150">When close-notify is enabled, the client application is required to send a close-notify message before closing TCP connections.</span></span> <span data-ttu-id="bf14d-151">Die HTTP-Server-API sendet vor dem Schließen der Verbindung auch eine schließende Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="bf14d-151">The HTTP Server API also sends a close-notify before closing the connection.</span></span><br/> <span data-ttu-id="bf14d-152">Wenn Close-notify aktiviert ist und der Client eine Nachricht mit der Meldung "Close-notify" sendet, wird die SSL-Sitzung von der HTTP-Server-API bei zukünftigen Verbindungen mit dem Client wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf14d-152">When close-notify is enabled, and the client sends a close-notify message, the HTTP Server API will reuse the SSL session on future connections to the client.</span></span> <span data-ttu-id="bf14d-153">Wenn der Client keine close-notify-Benachrichtigung sendet, wird die gleiche SSL-Sitzung von der HTTP-Server-API bei zukünftigen Verbindungen nicht wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf14d-153">If the client does not send a close-notify, the HTTP Server API will not reuse the same SSL session on future connections.</span></span> <span data-ttu-id="bf14d-154">Daher wird ein vollständiger SSL-Handshake für die neue Verbindung ausgelöst, wodurch die Leistung reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="bf14d-154">Thus, a full SSL handshake is triggered on the new connection thereby reducing performance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bf14d-155">Durch das Aktivieren von Close-notify werden abschneidender Angriffe gegen die HTTPS-Anforderungen und-Antworten minimiert.</span><span class="sxs-lookup"><span data-stu-id="bf14d-155">Enabling close-notify helps mitigate truncation attacks against the HTTPS requests and responses.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="bf14d-156">Wenn Close-notify deaktiviert ist, wird die SSL-Sitzung von der HTTP-Server-API für zukünftige Verbindungen erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf14d-156">When close-notify is disabled, the HTTP Server API reuses the SSL session for future connections.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf14d-157">Disablesslcertchaincacheonlyurlretrieval</span><span class="sxs-lookup"><span data-stu-id="bf14d-157">DisableSslCertChainCacheOnlyUrlRetrieval</span></span></td>
<td><span data-ttu-id="bf14d-158">Ein <strong>DWORD</strong> -Wert, der auf " <strong>true</strong> " festgelegt ist, damit die HTTP-Server-API zwischen Zertifikate aus dem Internet oder dem lokalen Speicher abrufen kann, oder " <strong>false</strong> ", um nur zwischen Zertifikate aus dem lokalen Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bf14d-158">A <strong>DWORD</strong> value that is set to <strong>TRUE</strong> to enable the HTTP Server API to retrieve intermediate certificates from either the Internet, or the local store, or <strong>FALSE</strong> to retrieve intermediate certificates from the local store only.</span></span> <span data-ttu-id="bf14d-159">Der Standard Registrierungs Wert ist <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf14d-159">The default registry value is <strong>FALSE</strong>.</span></span><br/> <span data-ttu-id="bf14d-160">Standardmäßig erstellt die HTTP-Server-API eine Client Zertifikat Kette, indem die zwischen Zertifikate aus dem zwischen Zertifizierungsstellen-Speicher unter dem lokalen Computer Konto abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bf14d-160">By default, the HTTP Server API builds a client certificate chain by retrieving the intermediate certificates from the Intermediate Certificate Authority store under the local machine account.</span></span> <span data-ttu-id="bf14d-161">Wenn dieser Wert auf <strong>true</strong> festgelegt wird, kann die HTTP-Server-API die zwischen Zertifikate nicht nur aus dem lokalen Speicher abrufen, sondern auch von der zwischen Zertifizierungsstelle im Internet.</span><span class="sxs-lookup"><span data-stu-id="bf14d-161">Setting this value to <strong>TRUE</strong> enables the HTTP Server API to retrieve the intermediate certificates not only from the local store, but also from the Intermediate Certificate Authority on the Internet.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





