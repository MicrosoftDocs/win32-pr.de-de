---
title: Arbeiten mit einem Zustands Server
description: NPS führt die Authentifizierung mithilfe einer Datenbank durch, die auf der NPS-Serversite konfiguriert ist.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341940"
---
# <a name="working-with-a-state-server"></a><span data-ttu-id="bceb5-103">Arbeiten mit einem Zustands Server</span><span class="sxs-lookup"><span data-stu-id="bceb5-103">Working With a State Server</span></span>

> [!Note]  
> <span data-ttu-id="bceb5-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bceb5-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="bceb5-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="bceb5-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="bceb5-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="bceb5-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="bceb5-107">NPS führt die Authentifizierung mithilfe einer Datenbank durch, die auf der NPS-Serversite konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="bceb5-107">NPS performs authentication using a database that is configured at the NPS server site.</span></span> <span data-ttu-id="bceb5-108">Bei dieser Authentifizierungs Datenbank kann es sich um die Benutzerdatenbank für eine Windows-Domäne oder um die Benutzerinformationen handeln, die Sie aus dem Windows-Active Directory abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="bceb5-108">This authentication database could be the user database for a Windows Domain or it could draw upon the user information obtained from the Windows Active Directory.</span></span> <span data-ttu-id="bceb5-109">Das folgende Diagramm veranschaulicht eine typische Konfiguration, die zeigt, wie NPS mit Authentifizierungs Datenbanken interagiert, z. b. eine Windows-Domänen Benutzerdatenbank oder Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bceb5-109">The following diagram illustrates a typical configuration that shows how NPS interacts with authentication databases such as a Windows Domain user database or Active Directory.</span></span> <span data-ttu-id="bceb5-110">Das Diagramm zeigt auch, wie NPS mit einem Zustands Server interagieren kann, der von einem Drittanbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bceb5-110">The diagram also shows how NPS could interact with a state server that is provided by a third party.</span></span> <span data-ttu-id="bceb5-111">Der Hauptzweck eines Zustands Servers besteht darin, die Anzahl der gleichzeitigen Anmelde Sitzungen einzuschränken, die ein einzelner Benutzer ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="bceb5-111">The primary purpose of a state server is to limit the number of simultaneous logon sessions a single user can run.</span></span>

![NPS-Interaktion mit Zustands Server-und Authentifizierungs Datenbanken](images/ias02.png)

<span data-ttu-id="bceb5-113">Es gibt zwei Aspekte der Interaktion zwischen NPS und dem Zustands Server.</span><span class="sxs-lookup"><span data-stu-id="bceb5-113">There are two points of interaction between NPS and the state server.</span></span> <span data-ttu-id="bceb5-114">Eine Interaktion findet statt, wenn NPS eine Authentifizierungsanforderung vom NAS empfängt.</span><span class="sxs-lookup"><span data-stu-id="bceb5-114">One interaction takes place when NPS receives an authentication request from the NAS.</span></span> <span data-ttu-id="bceb5-115">Der Zustands Server stellt Informationen aus seiner Datenbank bereit, um zu bestimmen, ob die Anforderung akzeptiert oder verweigert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bceb5-115">The state server provides information from its database to determine whether to accept or deny the request.</span></span> <span data-ttu-id="bceb5-116">Die andere Interaktion findet statt, wenn NPS Buchhaltungs Anforderungen vom NAS empfängt.</span><span class="sxs-lookup"><span data-stu-id="bceb5-116">The other interaction takes place when NPS receives accounting requests from the NAS.</span></span> <span data-ttu-id="bceb5-117">Der Zustands Server verwendet die Informationen aus diesen Buchhaltungs Anforderungen, um seine Datenbank zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bceb5-117">The state server uses the information form these accounting requests to update its database.</span></span>

<span data-ttu-id="bceb5-118">Weitere Informationen zu Status Servern finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="bceb5-118">For more information on state servers see:</span></span>

-   [<span data-ttu-id="bceb5-119">Überlegungen zum Status Server Entwurf</span><span class="sxs-lookup"><span data-stu-id="bceb5-119">State Server Design Considerations</span></span>](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a><span data-ttu-id="bceb5-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bceb5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bceb5-121">Internet Authentifizierungsdienst und Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="bceb5-121">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="bceb5-122">RADIUS-Authentifizierung,-Autorisierung und-Kontoführung</span><span class="sxs-lookup"><span data-stu-id="bceb5-122">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="bceb5-123">Protokollierung mit dem Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="bceb5-123">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 