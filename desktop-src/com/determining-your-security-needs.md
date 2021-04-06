---
title: Bestimmen Ihrer Sicherheitsanforderungen
description: Wie Sie die com-Sicherheit für Ihre Anwendung einrichten, hängt von der Art der Sicherheit ab, die Ihre Anwendung benötigt. Es gibt verschiedene häufige Situationen, die bestimmen, was Sie tun sollten.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714435"
---
# <a name="determining-your-security-needs"></a><span data-ttu-id="71698-104">Bestimmen Ihrer Sicherheitsanforderungen</span><span class="sxs-lookup"><span data-stu-id="71698-104">Determining Your Security Needs</span></span>

<span data-ttu-id="71698-105">Wie Sie die com-Sicherheit für Ihre Anwendung einrichten, hängt von der Art der Sicherheit ab, die Ihre Anwendung benötigt.</span><span class="sxs-lookup"><span data-stu-id="71698-105">How you set up COM security for your application depends on what kind of security your application needs.</span></span> <span data-ttu-id="71698-106">Es gibt verschiedene häufige Situationen, die bestimmen, was Sie tun sollten.</span><span class="sxs-lookup"><span data-stu-id="71698-106">There are several common situations that determine what you should do.</span></span>

<span data-ttu-id="71698-107">Wenn Sie sich dafür entscheiden, die com-Sicherheits Standardwerte zu verwenden, müssen Sie den com-Vorgang nicht alle durchführen.</span><span class="sxs-lookup"><span data-stu-id="71698-107">If you decide to use the COM security defaults, you do not have to do anythingâ€”COM handles it all.</span></span> <span data-ttu-id="71698-108">Informationen dazu, was diese Standardeinstellungen sind, finden Sie unter [com-Sicherheits Standardwerte](com-security-defaults.md).</span><span class="sxs-lookup"><span data-stu-id="71698-108">For information on what these default settings are, see [COM Security Defaults](com-security-defaults.md).</span></span>

<span data-ttu-id="71698-109">Sie können auch Remote Aufrufe an Ihren Computer verhindern, indem Sie DCOM vollständig deaktivieren (com zwischen Remote Computern).</span><span class="sxs-lookup"><span data-stu-id="71698-109">You can also prevent any remote calls into your machine by disabling DCOM altogether (COM between remote computers).</span></span> <span data-ttu-id="71698-110">Weitere Informationen finden Sie unter [Festlegen von System-Wide Sicherheit mithilfe von DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="71698-110">For more information, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="71698-111">Für ältere oder neue Anwendungen können Sie die Prozess weite Sicherheit in der Registrierung festlegen.</span><span class="sxs-lookup"><span data-stu-id="71698-111">For legacy or new applications, you can set process-wide security in the registry.</span></span> <span data-ttu-id="71698-112">Weitere Informationen finden Sie unter [Festlegen von Processwide Security über die Registrierung](setting-processwide-security-through-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="71698-112">For more information, see [Setting Processwide Security Through the Registry](setting-processwide-security-through-the-registry.md).</span></span>

<span data-ttu-id="71698-113">Sie können auch die Standard Sicherheitseinstellungen für Aufrufe bestimmter Schnittstellen im Prozess überschreiben, während Sie die Standard Sicherheit für den Rest des Prozesses festlegen (damit com die allgemeinen Fälle verarbeiten kann).</span><span class="sxs-lookup"><span data-stu-id="71698-113">You can also override default security settings for calls to certain interfaces in the process while setting default security for the remainder of the process (to allow COM to handle the general cases).</span></span> <span data-ttu-id="71698-114">Weitere Informationen finden Sie unter [Festlegen der Sicherheit auf der Ebene des Schnittstellen Proxys](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="71698-114">For more information, see [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="71698-115">Um komplexe Sicherheitsanforderungen zu erfüllen, können Sie die gesamte Sicherheit Programm gesteuert verarbeiten, anstatt com die Handhabung für Sie zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="71698-115">For complex security requirements, you can handle all security programmatically rather than allowing COM to handle it for you.</span></span> <span data-ttu-id="71698-116">Dazu wird [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) aufgerufen, um die automatische Authentifizierung zu deaktivieren, und dann alle Sicherheitseinstellungen zu steuern, indem die Sicherheit für einen Proxy pro Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="71698-116">To do this, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to disable automatic authentication, and then control all the security settings by setting security on a per-interface proxy basis.</span></span> <span data-ttu-id="71698-117">Weitere Informationen finden Sie unter [Festlegen von Processwide Security mit CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) und [Festlegen der Sicherheit auf der Ebene der Schnittstellen Proxys](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="71698-117">For more information, see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) and [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="71698-118">In einigen Szenarien sollten Sie die Sicherheit vollständig deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="71698-118">In some scenarios, you might want to turn off security completely.</span></span> <span data-ttu-id="71698-119">Sie können entscheiden, dass Ihre Anwendung keine Sicherheit benötigt, oder Sie können die Sicherheit während der Entwicklungszeit deaktivieren, damit Sie die Sicherheitsfeatures einzeln aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="71698-119">You might decide that your application does not need any security, or you might want to disable security during development time so that you can enable security features individually.</span></span> <span data-ttu-id="71698-120">Informationen zum Deaktivieren der com-Sicherheit finden Sie unter [Ausschalten der Sicherheit](turning-off-security.md).</span><span class="sxs-lookup"><span data-stu-id="71698-120">To learn how to disable COM security, see [Turning Off Security](turning-off-security.md).</span></span>

<span data-ttu-id="71698-121">Die Sicherheit in com basiert auf Authentifizierungsdiensten, die von Sicherheitspaketen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="71698-121">Security in COM relies on authentication services administered by security packages.</span></span> <span data-ttu-id="71698-122">NTLMSSP funktioniert für viele Anwendungen gut, bietet jedoch nicht die stabilere Sicherheit, die von anderen Paketen geboten wird.</span><span class="sxs-lookup"><span data-stu-id="71698-122">NTLMSSP works well for many applications but does not provide the more robust security offered by other packages.</span></span> <span data-ttu-id="71698-123">Daher unterstützt com das SChannel-Sicherheitspaket und das Kerberos V5-Sicherheitsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="71698-123">Therefore, COM supports the Schannel security package and the Kerberos v5 security protocol.</span></span> <span data-ttu-id="71698-124">Weitere Informationen zur Verwendung dieser Sicherheitspakete finden Sie unter [com-und Sicherheitspakete](com-and-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="71698-124">For more details on using these security packages, see [COM and Security Packages](com-and-security-packages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71698-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71698-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71698-126">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="71698-126">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




