---
title: Erteilen von Zugriffsrechten für das Dienst Anmelde Konto
description: Ein primärer Aspekt beim Installieren einer Dienst Instanz besteht darin sicherzustellen, dass der installierte Dienst auf die erforderlichen Ressourcen zugreifen kann.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Erteilen von Zugriffsrechten für das Dienst Anmelde Konto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106338450"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a><span data-ttu-id="db4bd-104">Erteilen von Zugriffsrechten für das Dienst Anmelde Konto</span><span class="sxs-lookup"><span data-stu-id="db4bd-104">Granting Access Rights to the Service Logon Account</span></span>

<span data-ttu-id="db4bd-105">Ein primärer Aspekt beim Installieren einer Dienst Instanz besteht darin sicherzustellen, dass der installierte Dienst auf die erforderlichen Ressourcen zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="db4bd-105">A primary consideration of installing a service instance is to ensure that the installed service can access the necessary resources.</span></span> <span data-ttu-id="db4bd-106">Legen Sie hierzu in den Sicherheits Beschreibungen von Objekten, auf die der Dienst zugreifen muss, ACEs fest.</span><span class="sxs-lookup"><span data-stu-id="db4bd-106">To do this, set ACEs in the security descriptors of objects that the service must access.</span></span> <span data-ttu-id="db4bd-107">Ein ACE kann Zugriffsrechte für einen angegebenen Sicherheits Prinzipal gewähren oder verweigern, wie z. b. das Dienst Benutzerkonto oder das Computer Konto für einen LocalSystem-Dienst oder eine Gruppe, zu der das Dienst Konto gehört.</span><span class="sxs-lookup"><span data-stu-id="db4bd-107">An ACE can grant or deny access rights to a specified security principal, such as the service user account, or the computer account for a LocalSystem service, or a group to which the service's account belongs.</span></span> <span data-ttu-id="db4bd-108">Weitere Informationen zu ACEs, Sicherheits Deskriptoren und Zugriffs Steuerung finden [Sie Untersteuern des Zugriffs auf Objekte in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) und [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="db4bd-108">For more information about ACEs, security descriptors, and access control, see [Controlling Access to objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="db4bd-109">Weitere Informationen und ein Codebeispiel, mit dem ein ACE festgelegt werden kann, der dem Dienst das Ändern des Dienst Verbindungs Punkts ermöglicht, finden Sie unter [Aktivieren des Dienst Kontos für den Zugriff auf SCP-Eigenschaften](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="db4bd-109">For more information and a code example that can be used to set an ACE that enables the service to modify its service connection point, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>

<span data-ttu-id="db4bd-110">In einigen Fällen müssen Sie Ihr Dienst Benutzerkonto als Mitglied einer oder mehrerer Sicherheitsgruppen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="db4bd-110">In some cases, you must add your service user account as a member of one or more security groups.</span></span> <span data-ttu-id="db4bd-111">Wenn Sie z. b. eine Gruppe "Administratoren" für den Dienst erstellen, können Sie den Dienst als Mitglied der Gruppe festlegen.</span><span class="sxs-lookup"><span data-stu-id="db4bd-111">For example, if you create an administrators group for your service, you might make the service a member of the group.</span></span> <span data-ttu-id="db4bd-112">Sie können der Gruppe dann Zugriffsrechte erteilen, anstatt Sie explizit dem Dienst Konto zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="db4bd-112">You can then grant access rights to the group rather than granting them explicitly to the service account.</span></span> <span data-ttu-id="db4bd-113">Weitere Informationen zu Sicherheitsgruppen finden Sie unter [Verwalten von Gruppen](managing-groups.md).</span><span class="sxs-lookup"><span data-stu-id="db4bd-113">For more information about security groups, see [Managing Groups](managing-groups.md).</span></span>

 

 