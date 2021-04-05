---
title: Remotedesktop Gateway-Schnittstellen
description: Die Remotedesktop Gateway-API (RD-Gateway) unterstützt die folgenden Schnittstellen. Sie können diese Schnittstellen zum Implementieren von Plug-Ins verwenden, die eine angepasste Authentifizierung und Autorisierung bereitstellen.
ms.assetid: a457574a-d856-4490-b20d-48343a82acff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2b0a17c19431ea69419443459639d199219a61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947445"
---
# <a name="remote-desktop-gateway-interfaces"></a><span data-ttu-id="59433-104">Remotedesktop Gateway-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="59433-104">Remote Desktop Gateway Interfaces</span></span>

<span data-ttu-id="59433-105">Die Remotedesktop Gateway-API (RD-Gateway) unterstützt die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="59433-105">The Remote Desktop Gateway (RD Gateway) API supports the following interfaces.</span></span> <span data-ttu-id="59433-106">Sie können diese Schnittstellen zum Implementieren von Plug-Ins verwenden, die eine angepasste Authentifizierung und Autorisierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="59433-106">You can use these interfaces to implement plug-ins that provide customized authentication and authorization.</span></span> <span data-ttu-id="59433-107">Es besteht keine Abhängigkeit zwischen dem Authentifizierungs-Plug-in und dem Autorisierungs-Plug-in, und Sie können nur ein einzelnes Plug-in implementieren, wenn Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="59433-107">There is no dependency between the authentication plug-in and the authorization plug-in, and you can implement only a single plug-in if you choose.</span></span>

<span data-ttu-id="59433-108">Die Authentifizierungs-Plug-ins sind [**itsgauthentiereusersink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) und [**itsgauthenticationengine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span><span class="sxs-lookup"><span data-stu-id="59433-108">The authentication plug-ins are [**ITSGAuthenticateUserSink**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink) and [**ITSGAuthenticationEngine**](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine).</span></span>

<span data-ttu-id="59433-109">Die Autorisierungs-Plug-ins sind [**itsgaccountingengine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**itsgauthorizeconnectionsink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**itsgautorizeresourcesink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)und [**itsgpolicyengine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span><span class="sxs-lookup"><span data-stu-id="59433-109">The authorization plug-ins are [**ITSGAccountingEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine), [**ITSGAuthorizeConnectionSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink), [**ITSGAuthorizeResourceSink**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink), and [**ITSGPolicyEngine**](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="59433-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="59433-110">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="59433-111">**Itsgaccountingengine**</span><span class="sxs-lookup"><span data-stu-id="59433-111">**ITSGAccountingEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgaccountingengine)
</dt> <dd>

<span data-ttu-id="59433-112">Macht Methoden verfügbar, die Informationen über das Erstellen oder Schließen von Sitzungen für eine Verbindung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="59433-112">Exposes methods that provide information about the creation or closing of sessions for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="59433-113">**Itsgauthentisineusersink**</span><span class="sxs-lookup"><span data-stu-id="59433-113">**ITSGAuthenticateUserSink**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticateusersink)
</dt> <dd>

<span data-ttu-id="59433-114">Macht Methoden verfügbar, die RD-Gateway über Authentifizierungs Ereignisse benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="59433-114">Exposes methods that notify RD Gateway about authentication events.</span></span>

</dd> <dt>

[<span data-ttu-id="59433-115">**Itsgauthenticationengine**</span><span class="sxs-lookup"><span data-stu-id="59433-115">**ITSGAuthenticationEngine**</span></span>](/windows/desktop/api/TSGAuthenticationEngine/nn-tsgauthenticationengine-itsgauthenticationengine)
</dt> <dd>

<span data-ttu-id="59433-116">Macht Methoden verfügbar, die Benutzer für RD-Gateway authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="59433-116">Exposes methods that authenticate users for RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="59433-117">**Itsgauthorizeconnectionsink**</span><span class="sxs-lookup"><span data-stu-id="59433-117">**ITSGAuthorizeConnectionSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeconnectionsink)
</dt> <dd>

<span data-ttu-id="59433-118">Macht Methoden verfügbar, die RD-Gateway über das Ergebnis des Versuchs, eine Verbindung zu autorisieren, benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="59433-118">Exposes methods that notify RD Gateway about the result of an attempt to authorize a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="59433-119">**Itsgautorizeresourcesink**</span><span class="sxs-lookup"><span data-stu-id="59433-119">**ITSGAuthorizeResourceSink**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgauthorizeresourcesink)
</dt> <dd>

<span data-ttu-id="59433-120">Macht Methoden verfügbar, die RD-Gateway über das Ergebnis des Versuchs, eine Ressource zu autorisieren, benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="59433-120">Exposes methods that notify RD Gateway about the result of an attempt to authorize a resource.</span></span>

</dd> <dt>

[<span data-ttu-id="59433-121">**Itsgpolicyengine**</span><span class="sxs-lookup"><span data-stu-id="59433-121">**ITSGPolicyEngine**</span></span>](/windows/desktop/api/TSGPolicyEngine/nn-tsgpolicyengine-itsgpolicyengine)
</dt> <dd>

<span data-ttu-id="59433-122">Macht Methoden verfügbar, die Verbindungen und Ressourcen autorisieren.</span><span class="sxs-lookup"><span data-stu-id="59433-122">Exposes methods that authorize connections and resources.</span></span>

</dd> </dl>

 

 




