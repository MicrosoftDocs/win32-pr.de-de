---
description: Netzwerk Quellen Authentifizierung
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Netzwerk Quellen Authentifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041905"
---
# <a name="network-source-authentication"></a><span data-ttu-id="4abf2-103">Netzwerk Quellen Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="4abf2-103">Network Source Authentication</span></span>

<span data-ttu-id="4abf2-104">Für bestimmte Medien Hosts sind möglicherweise Benutzer Anmelde Informationen von Client Anwendungen erforderlich, bevor der Zugriff auf die Medien zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="4abf2-104">Certain media hosts may require user credentials from client applications before allowing access to the media.</span></span> <span data-ttu-id="4abf2-105">Zu den Benutzer Anmelde Informationen gehören Identifizierung und Nachweis der Identifizierung, wie z. b. Benutzername und Kennwort, die vom Medienserver verwendet werden, um den Zugriff auf die von ihm gehosteten Netzwerkquelle zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="4abf2-105">User credentials include identification and proof of identification, such as user name and password, which are used by the media server to grant access to the network source it hosts.</span></span> <span data-ttu-id="4abf2-106">Die Netzwerkquelle kann die NTLM-, Digest-oder Standard Authentifizierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4abf2-106">The network source can provide NTLM, Digest, or Basic authentication.</span></span>

<span data-ttu-id="4abf2-107">Anwendungen, die auf Media Foundation basieren, können Benutzer Anmelde Informationen für eine bestimmte URL in einem *Anmelde Informationen* -Objekt speichern, das die [**IMF netcredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="4abf2-107">Applications based on Media Foundation can store user credentials for a specific URL in a *credential* object that exposes the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) interface.</span></span> <span data-ttu-id="4abf2-108">Das Anmelde Informationen-Objekt speichert verschlüsselte Anmelde Informationen und stellt Methoden zum Zurückgeben von Informationen wie Benutzername, Kennwort und Domäne bereit.</span><span class="sxs-lookup"><span data-stu-id="4abf2-108">The credential object stores encrypted credentials and provides methods to return information such as user name, password, and domain.</span></span>

<span data-ttu-id="4abf2-109">Die Anmelde Informationsobjekte werden in einem Cache erstellt und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4abf2-109">The credential objects are created and maintained in a cache.</span></span> <span data-ttu-id="4abf2-110">Das-Anmelde Informations *Cache* -Objekt, das von der [**IMF netkredentialcache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) -Schnittstelle verfügbar gemacht wird, stellt Methoden zum Abrufen der Anmelde Informationsobjekte aus dem Anmelde Informations Cache bereit.</span><span class="sxs-lookup"><span data-stu-id="4abf2-110">The *credential cache* object, exposed by the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface provides methods for retrieving the credential objects from the credential cache.</span></span>

<span data-ttu-id="4abf2-111">Eine Anwendung, die die Authentifizierung unterstützt, muss die [**IMF netkredentialmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="4abf2-111">An application that supports authentication must implement the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="4abf2-112">Media Foundation stellt keine Standard Implementierung dieser Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="4abf2-112">Media Foundation does not provide a default implementation of this interface.</span></span> <span data-ttu-id="4abf2-113">Die Anmelde Informationsverwaltung ist dafür verantwortlich, die erforderlichen Anmelde Informationen für eine URL aus der Benutzereingabe oder das Lesen aus dem persistenten Speicher zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="4abf2-113">The credential manager is responsible for gathering the required credentials for a URL from user input or reading from persisted storage.</span></span>

<span data-ttu-id="4abf2-114">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4abf2-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="4abf2-115">Festlegen eines Credential-Managers</span><span class="sxs-lookup"><span data-stu-id="4abf2-115">Setting a Credential Manager</span></span>](setting-a-credential-manager.md)
-   [<span data-ttu-id="4abf2-116">Verwenden des Anmelde Informations Caches</span><span class="sxs-lookup"><span data-stu-id="4abf2-116">Using the Credential Cache</span></span>](using-the-credential-cache.md)
-   [<span data-ttu-id="4abf2-117">Implementieren von IMF netkredentialmanager</span><span class="sxs-lookup"><span data-stu-id="4abf2-117">Implementing IMFNetCredentialManager</span></span>](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a><span data-ttu-id="4abf2-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4abf2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4abf2-119">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4abf2-119">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



