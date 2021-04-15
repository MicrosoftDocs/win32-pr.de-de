---
description: Das LocalService-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: LocalService-Konto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529867"
---
# <a name="localservice-account"></a><span data-ttu-id="2a5b2-103">LocalService-Konto</span><span class="sxs-lookup"><span data-stu-id="2a5b2-103">LocalService Account</span></span>

<span data-ttu-id="2a5b2-104">Das LocalService-Konto ist ein vordefiniertes lokales Konto, das vom Dienststeuerungs-Manager verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a5b2-104">The LocalService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="2a5b2-105">Er verfügt über minimale Berechtigungen auf dem lokalen Computer und stellt anonyme Anmelde Informationen im Netzwerk dar.</span><span class="sxs-lookup"><span data-stu-id="2a5b2-105">It has minimum privileges on the local computer and presents anonymous credentials on the network.</span></span>

<span data-ttu-id="2a5b2-106">Dieses Konto kann in einem aufzurufenden Rückruf [**der Funktionen**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) "-Funktion" und " [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) " angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2a5b2-106">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="2a5b2-107">Beachten Sie, dass dieses Konto nicht über ein Kennwort verfügt, sodass alle Kenn Wort Informationen, die Sie in diesem Bericht angeben, ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="2a5b2-107">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="2a5b2-108">Obwohl das Sicherheits Subsystem diesen Kontonamen lokalisiert, unterstützt der SCM keine lokalisierten Namen.</span><span class="sxs-lookup"><span data-stu-id="2a5b2-108">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="2a5b2-109">Daher erhalten Sie einen lokalisierten Namen für dieses Konto von der [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) -Funktion, aber der Name des Kontos muss NT Authority \\ LocalService lauten, wenn Sie " **kreateservice** " oder " **ChangeServiceConfig**" aufrufen, unabhängig vom Gebiets Schema oder unerwartete Ergebnisse können auftreten.</span><span class="sxs-lookup"><span data-stu-id="2a5b2-109">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\LocalService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="2a5b2-110">Die Benutzer-SID wird aus dem RID-Wert des **\_ lokalen \_ \_ Diensts der Sicherheit** erstellt.</span><span class="sxs-lookup"><span data-stu-id="2a5b2-110">The user SID is created from the **SECURITY\_LOCAL\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="2a5b2-111">Das LocalService-Konto verfügt über einen eigenen Unterschlüssel unter dem Registrierungsschlüssel " **HKEY \_ Users** ".</span><span class="sxs-lookup"><span data-stu-id="2a5b2-111">The LocalService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="2a5b2-112">Daher ist der Registrierungsschlüssel des **aktuellen HKEY- \_ \_ Benutzers** dem LocalService-Konto zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2a5b2-112">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the LocalService account.</span></span>

<span data-ttu-id="2a5b2-113">Das LocalService-Konto verfügt über die folgenden Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="2a5b2-113">The LocalService account has the following privileges:</span></span>

-   <span data-ttu-id="2a5b2-114">**SE \_ \_Name des zugriffsmarytokens** (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="2a5b2-114">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="2a5b2-115">**SE \_ Überwachungs \_ Name** (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="2a5b2-115">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="2a5b2-116">**SE \_ \_Benachrichtigungs \_ Name ändern** (aktiviert)</span><span class="sxs-lookup"><span data-stu-id="2a5b2-116">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="2a5b2-117">**SE \_ \_Globalen \_ Namen erstellen** (aktiviert)</span><span class="sxs-lookup"><span data-stu-id="2a5b2-117">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="2a5b2-118">**SE \_ Identität des \_ namens** annehmen (aktiviert)</span><span class="sxs-lookup"><span data-stu-id="2a5b2-118">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="2a5b2-119">**SE \_ \_Kontingent \_ Namen erhöhen** (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="2a5b2-119">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="2a5b2-120">**SE \_ \_Name des herunter** Fahrens (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="2a5b2-120">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="2a5b2-121">**SE \_ \_Name der nicht-Dock** (deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="2a5b2-121">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="2a5b2-122">Alle Berechtigungen, die Benutzern und authentifizierten Benutzern zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="2a5b2-122">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="2a5b2-123">Weitere Informationen finden Sie unter [Dienst Sicherheit und Zugriffsrechte](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="2a5b2-123">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
