---
description: Zum Schreiben eines sicheren Anbieters müssen Sie berücksichtigen, wie der Anbieter gehostet wird, wie der Anbieter den Identitätswechsel übernimmt und sicherstellen, dass die Benutzer auf die Daten zugreifen können.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Sichern Ihres Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347068"
---
# <a name="securing-your-provider"></a><span data-ttu-id="cd64d-103">Sichern Ihres Anbieters</span><span class="sxs-lookup"><span data-stu-id="cd64d-103">Securing Your Provider</span></span>

<span data-ttu-id="cd64d-104">Zum Schreiben eines sicheren Anbieters müssen Sie berücksichtigen, wie der Anbieter gehostet wird, wie der Anbieter den Identitätswechsel übernimmt und sicherstellen, dass die Benutzer auf die Daten zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="cd64d-104">Writing a secure provider requires considering how the provider is hosted, how the provider handles impersonation, and ensuring that users are checked for access rights to data.</span></span> <span data-ttu-id="cd64d-105">Sie können die Daten im Anbieter Namespace sichern, indem Sie die Verschlüsselung von Daten vor dem Senden über ein Netzwerk vorschreiben.</span><span class="sxs-lookup"><span data-stu-id="cd64d-105">You can secure the data in your provider namespace by requiring that data be encrypted authentication before sending it over a network.</span></span> <span data-ttu-id="cd64d-106">Weitere Informationen finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="cd64d-106">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="cd64d-107">Wenn ein Benutzer über **vollständigen \_ Schreib** Zugriff in einem Namespace verfügt, kann der Benutzer Namespace übergreifende Abonnements für Daten in einem Namespace erstellen, in dem der Benutzer eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="cd64d-107">If a user has **FULL\_WRITE** access in any namespace, then the user can create cross-namespace subscriptions for data in a namespace in which the user is restricted.</span></span> <span data-ttu-id="cd64d-108">Da ein Anbieter in beliebige Namespaces geladen und in einem beliebigen Sicherheitskontext ausgeführt werden kann, sollte der Anbieter seine eigenen Zugriffs Überprüfungen durchführen, um sicherzustellen, dass nur autorisierte Benutzer Zugriff auf Daten haben oder Methoden ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd64d-108">Because a provider can be loaded into any namespace and be executing in any security context, the provider should perform its own access checks to ensure that only authorized users are allowed access to data or to execute methods.</span></span> <span data-ttu-id="cd64d-109">Weitere Informationen finden Sie unter [Durchführen von Zugriffs Überprüfungen](performing-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="cd64d-109">For more information, see [Performing Access Checks](performing-access-checks.md).</span></span>

<span data-ttu-id="cd64d-110">In den folgenden Themen wird die Anbieter Sicherheit erörtert:</span><span class="sxs-lookup"><span data-stu-id="cd64d-110">The following topics discuss provider security:</span></span>

-   [<span data-ttu-id="cd64d-111">Anbieter Hosting und-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cd64d-111">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
-   [<span data-ttu-id="cd64d-112">Ausführen von Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="cd64d-112">Performing Access Checks</span></span>](performing-access-checks.md)
-   [<span data-ttu-id="cd64d-113">Registrierungsschlüssel zum Steuern der Anbieter Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cd64d-113">Registry Keys for Controlling Provider Security</span></span>](registry-keys-for-controlling-provider-security-.md)
-   [<span data-ttu-id="cd64d-114">Zugriff auf WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="cd64d-114">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
-   [<span data-ttu-id="cd64d-115">Annehmen der Identität eines Clients</span><span class="sxs-lookup"><span data-stu-id="cd64d-115">Impersonating a Client</span></span>](impersonating-a-client.md)

<span data-ttu-id="cd64d-116">In den folgenden Themen wird erläutert, wie Clients und Skripts mit der Anbieter Sicherheit interagieren:</span><span class="sxs-lookup"><span data-stu-id="cd64d-116">The following topics discuss how clients and scripts interact with provider security:</span></span>

-   [<span data-ttu-id="cd64d-117">Festlegen der Authentifizierung in WMI</span><span class="sxs-lookup"><span data-stu-id="cd64d-117">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
-   [<span data-ttu-id="cd64d-118">Herstellen einer Verbindung zwischen verschiedenen Betriebssystemen</span><span class="sxs-lookup"><span data-stu-id="cd64d-118">Connecting Between Different Operating Systems</span></span>](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [<span data-ttu-id="cd64d-119">Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript</span><span class="sxs-lookup"><span data-stu-id="cd64d-119">Setting the Default Process Security Level Using VBScript</span></span>](setting-the-default-process-security-level-using-vbscript.md)
-   [<span data-ttu-id="cd64d-120">Festlegen der Prozesssicherheit für Client Anwendungen</span><span class="sxs-lookup"><span data-stu-id="cd64d-120">Setting Client Application Process Security</span></span>](setting-client-application-process-security.md)

## <a name="related-topics"></a><span data-ttu-id="cd64d-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd64d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd64d-122">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="cd64d-122">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="cd64d-123">Verwenden von WMI</span><span class="sxs-lookup"><span data-stu-id="cd64d-123">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
