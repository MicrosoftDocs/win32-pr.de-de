---
description: Das Network Service-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Network Service-Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373242"
---
# <a name="networkservice-account"></a><span data-ttu-id="7a4d2-103">Network Service-Konto</span><span class="sxs-lookup"><span data-stu-id="7a4d2-103">NetworkService Account</span></span>

<span data-ttu-id="7a4d2-104">Das Network Service-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-104">The NetworkService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="7a4d2-105">Dieses Konto wird vom Sicherheits Subsystem nicht erkannt, sodass Sie seinen Namen nicht in einem aufzurufenden [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) -Funktion angeben können.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-105">This account is not recognized by the security subsystem, so you cannot specify its name in a call to the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span> <span data-ttu-id="7a4d2-106">Er verfügt über minimale Berechtigungen auf dem lokalen Computer und fungiert als Computer im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-106">It has minimum privileges on the local computer and acts as the computer on the network.</span></span>

<span data-ttu-id="7a4d2-107">Dieses Konto kann in einem aufzurufenden Rückruf [**der Funktionen**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) "-Funktion" und " [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) " angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-107">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="7a4d2-108">Beachten Sie, dass dieses Konto nicht über ein Kennwort verfügt, sodass alle Kenn Wort Informationen, die Sie in diesem Bericht angeben, ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-108">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="7a4d2-109">Obwohl das Sicherheits Subsystem diesen Kontonamen lokalisiert, unterstützt der SCM keine lokalisierten Namen.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-109">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="7a4d2-110">Aus diesem Grund erhalten Sie einen lokalisierten Namen für dieses Konto von der [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) -Funktion. der Name des Kontos muss jedoch NT Authority \\ Network Service lauten, wenn Sie " **kreateservice** " oder " **ChangeServiceConfig**" aufrufen, unabhängig vom Gebiets Schema, oder unerwartete Ergebnisse auftreten können.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-110">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\NetworkService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="7a4d2-111">Ein Dienst, der im Kontext des Network Service-Kontos ausgeführt wird, stellt die Anmelde Informationen des Computers für Remote Server dar.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-111">A service that runs in the context of the NetworkService account presents the computer's credentials to remote servers.</span></span> <span data-ttu-id="7a4d2-112">Standardmäßig enthält das Remote Token SIDs für die Gruppen "jeder" und "authentifizierte Benutzer".</span><span class="sxs-lookup"><span data-stu-id="7a4d2-112">By default, the remote token contains SIDs for the Everyone and Authenticated Users groups.</span></span> <span data-ttu-id="7a4d2-113">Die Benutzer-SID wird aus dem RID-Wert des **Security \_ Network \_ Service \_** erstellt.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-113">The user SID is created from the **SECURITY\_NETWORK\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="7a4d2-114">Das Network Service-Konto verfügt über einen eigenen Unterschlüssel unter dem Registrierungsschlüssel für **HKEY- \_ Benutzer** .</span><span class="sxs-lookup"><span data-stu-id="7a4d2-114">The NetworkService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="7a4d2-115">Daher ist der Registrierungsschlüssel des **aktuellen HKEY- \_ \_ Benutzers** dem NetworkService-Konto zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="7a4d2-115">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the NetworkService account.</span></span>

<span data-ttu-id="7a4d2-116">Das Network Service-Konto verfügt über die folgenden Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="7a4d2-116">The NetworkService account has the following privileges:</span></span>

-   <span data-ttu-id="7a4d2-117">**SE \_ \_Name des zugriffsmarytokens** (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="7a4d2-117">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="7a4d2-118">**SE \_ Überwachungs \_ Name** (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="7a4d2-118">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="7a4d2-119">**SE \_ \_Benachrichtigungs \_ Name ändern** (aktiviert)</span><span class="sxs-lookup"><span data-stu-id="7a4d2-119">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="7a4d2-120">**SE \_ \_Globalen \_ Namen erstellen** (aktiviert)</span><span class="sxs-lookup"><span data-stu-id="7a4d2-120">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="7a4d2-121">**SE \_ Identität des \_ namens** annehmen (aktiviert)</span><span class="sxs-lookup"><span data-stu-id="7a4d2-121">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="7a4d2-122">**SE \_ \_Kontingent \_ Namen erhöhen** (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="7a4d2-122">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="7a4d2-123">**SE \_ \_Name des herunter** Fahrens (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="7a4d2-123">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="7a4d2-124">**SE \_ \_Name der nicht-Dock** (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="7a4d2-124">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="7a4d2-125">Alle Berechtigungen, die Benutzern und authentifizierten Benutzern zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="7a4d2-125">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="7a4d2-126">Weitere Informationen finden Sie unter [Dienst Sicherheit und Zugriffsrechte](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="7a4d2-126">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
