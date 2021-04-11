---
description: Nachdem Sie den Netzwerkanbieter oder die Anmelde Informationsverwaltung erstellt haben, müssen Sie ihn beim System registrieren.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registrieren von Netzwerkanbietern und Anmelde Informations Managern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216337"
---
# <a name="registering-network-providers-and-credential-managers"></a><span data-ttu-id="1120f-103">Registrieren von Netzwerkanbietern und Anmelde Informations Managern</span><span class="sxs-lookup"><span data-stu-id="1120f-103">Registering Network Providers and Credential Managers</span></span>

<span data-ttu-id="1120f-104">Nachdem Sie den Netzwerkanbieter oder die Anmelde Informationsverwaltung erstellt haben, müssen Sie ihn beim System registrieren.</span><span class="sxs-lookup"><span data-stu-id="1120f-104">After you have created your network provider or credential manager, you must register it with the system.</span></span> <span data-ttu-id="1120f-105">Dies ist erforderlich, damit die MPR weiß, welche Netzwerkanbieter installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1120f-105">This is necessary so the MPR will know what network providers are installed.</span></span> <span data-ttu-id="1120f-106">Beim Start der MPR wird die Registrierung überprüft und alle gefundenen Netzwerkanbieter oder Anmelde Informations-Manager geladen.</span><span class="sxs-lookup"><span data-stu-id="1120f-106">When the MPR starts, it checks the registry and loads any network providers or credential managers it finds.</span></span>

<span data-ttu-id="1120f-107">Da Netzwerkanbieter und Anmelde Informations Verwalter verknüpft sind, werden Sie in denselben unter Schlüsseln der Registrierung registriert.</span><span class="sxs-lookup"><span data-stu-id="1120f-107">Because network providers and credential managers are related, they are registered in the same subkeys of the registry.</span></span> <span data-ttu-id="1120f-108">Tatsächlich können DLLs für Netzwerkanbieter auch Anmelde Informationsmanager sein.</span><span class="sxs-lookup"><span data-stu-id="1120f-108">In fact, network provider DLLs can also be credential managers.</span></span>

<span data-ttu-id="1120f-109">Ausführliche Informationen zu den Registrierungs Schlüsseln, die Sie für Ihren Netzwerkanbieter oder Anmelde Informationsverwaltung erstellen sollten, finden Sie unter [Authentifizierungs Registrierungsschlüssel](authentication-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="1120f-109">For detailed information about the registry keys you should create for your network provider or credential manager, see [Authentication Registry Keys](authentication-registry-keys.md).</span></span>

 

 



