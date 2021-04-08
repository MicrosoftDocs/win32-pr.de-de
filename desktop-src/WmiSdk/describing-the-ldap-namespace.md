---
description: Wenn Sie eine Remote Verbindung mit einem Active Directory-Server herstellen, der nicht der in Ihrer aktuellen Domäne ist, müssen Sie den Namen eines Computers angeben, der bereits Mitglied der Domäne ist, die zum gewünschten Active Directory gehört.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Beschreiben des LDAP-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050266"
---
# <a name="describing-the-ldap-namespace"></a><span data-ttu-id="276aa-103">Beschreiben des LDAP-Namespace</span><span class="sxs-lookup"><span data-stu-id="276aa-103">Describing the LDAP Namespace</span></span>

<span data-ttu-id="276aa-104">Wenn Sie eine Remote Verbindung mit einem Active Directory-Server herstellen, der nicht der in Ihrer aktuellen Domäne ist, müssen Sie den Namen eines Computers angeben, der bereits Mitglied der Domäne ist, die zum gewünschten Active Directory gehört.</span><span class="sxs-lookup"><span data-stu-id="276aa-104">When connecting remotely to an Active Directory server other than the one in your current domain, you must specify the name of a computer that is already a member of the domain belonging to the Active Directory you want.</span></span>

<span data-ttu-id="276aa-105">Geben Sie den folgenden Befehl ein, um eine Remote Verbindung mit einem Computer herzustellen, der bereits Mitglied der Domäne ist, die zum Active Directory-Server gehört.</span><span class="sxs-lookup"><span data-stu-id="276aa-105">To remotely connect to a computer that is already a member of the domain belonging to the Active Directory server, type the following command.</span></span>

<span data-ttu-id="276aa-106">**\\\\Remote Computer- \\ Stamm \\ Verzeichnis \\ LDAP**</span><span class="sxs-lookup"><span data-stu-id="276aa-106">**\\\\RemoteComputer\\root\\directory\\LDAP**</span></span>

<span data-ttu-id="276aa-107">Dieses Beispiel zeigt, dass es zwei Teile gibt, die einen voll qualifizierten Namespace Namen bilden.</span><span class="sxs-lookup"><span data-stu-id="276aa-107">This example shows that there are two parts that make up a fully qualified namespace name.</span></span> <span data-ttu-id="276aa-108">Der erste Teil ( \\ \\ Remotecomputer) stellt den Computer dar, der bereits Mitglied der Domäne ist, die zum gewünschten Active Directory Server gehört.</span><span class="sxs-lookup"><span data-stu-id="276aa-108">The first part (\\\\RemoteComputer) represents the computer that is already a member of the domain belonging to the Active Directory server you want.</span></span> <span data-ttu-id="276aa-109">Der zweite Teil ( \\ Stamm \\ Verzeichnis \\ LDAP) stellt das Active Directory Schema im Verzeichnisdienst Anbieter dar.</span><span class="sxs-lookup"><span data-stu-id="276aa-109">The second part (\\root\\directory\\LDAP) represents the Active Directory schema in the Directory Services Provider.</span></span>

> [!Note]  
> <span data-ttu-id="276aa-110">Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="276aa-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



