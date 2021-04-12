---
title: Authentifizierung (AD DS)
description: Jedes Objekt in Active Directory Domain Services verfügt über eine eindeutige Sicherheits Beschreibung, die die Zugriffsberechtigungen definiert, die erforderlich sind, um das Objekt oder seine individuellen Eigenschaften zu lesen oder zu aktualisieren.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden, Bindung, Authentifizierung
- Binden der Authentifizierungs Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472700"
---
# <a name="authentication-ad-ds"></a><span data-ttu-id="595b9-105">Authentifizierung (AD DS)</span><span class="sxs-lookup"><span data-stu-id="595b9-105">Authentication (AD DS)</span></span>

<span data-ttu-id="595b9-106">Jedes Objekt in Active Directory Domain Services verfügt über eine eindeutige Sicherheits Beschreibung, die die Zugriffsberechtigungen definiert, die erforderlich sind, um das Objekt oder seine individuellen Eigenschaften zu lesen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="595b9-106">Every object in Active Directory Domain Services has a unique security descriptor that defines the access permissions that are required to read or update the object or its individual properties.</span></span> <span data-ttu-id="595b9-107">Zugriffsberechtigungen werden durch die Rechte festgelegt, die für das Konto oder die Gruppenmitgliedschaften eines Benutzers erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="595b9-107">Access privileges are determined by the rights granted to a user's account or group memberships.</span></span>

<span data-ttu-id="595b9-108">Wenn eine Anwendung an ein Objekt im Verzeichnis gebunden wird, basieren die Zugriffsrechte, die die Anwendung auf dieses Objekt hat, auf dem Benutzer Kontext, der während des Bindungs Vorgangs angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="595b9-108">When an application binds to an object in the directory, the access privileges that the application has to that object are based on the user context specified during the bind operation.</span></span> <span data-ttu-id="595b9-109">Für die Bindungsfunktionen und-Methoden [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**iadsopendsobject:: opendsobject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject)kann eine Anwendung implizit die Anmelde Informationen des Aufrufers verwenden, die Anmelde Informationen eines Benutzerkontos explizit angeben oder einen nicht authentifizierten Benutzer Kontext (Guest) verwenden.</span><span class="sxs-lookup"><span data-stu-id="595b9-109">For the binding functions and methods [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), an application can implicitly use the credentials of the caller, explicitly specify the credentials of a user account, or use an unauthenticated user context (Guest).</span></span>

 

 