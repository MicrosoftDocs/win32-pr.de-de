---
description: Listet die Schnittstellen in den Authentifizierungs-APIs auf.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Authentifizierungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216544"
---
# <a name="authentication-interfaces"></a><span data-ttu-id="9bd1a-103">Authentifizierungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9bd1a-103">Authentication Interfaces</span></span>

<span data-ttu-id="9bd1a-104">Authentifizierungs Schnittstellen werden gemäß der Verwendung wie folgt kategorisiert:</span><span class="sxs-lookup"><span data-stu-id="9bd1a-104">Authentication interfaces are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="9bd1a-105">Smartcardschnittstellen</span><span class="sxs-lookup"><span data-stu-id="9bd1a-105">Smart Card Interfaces</span></span>](#smart-card-interfaces)
-   [<span data-ttu-id="9bd1a-106">Identitäts Freigabe Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9bd1a-106">Identity Sharing Interfaces</span></span>](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a><span data-ttu-id="9bd1a-107">Smartcardschnittstellen</span><span class="sxs-lookup"><span data-stu-id="9bd1a-107">Smart Card Interfaces</span></span>

<span data-ttu-id="9bd1a-108">Das Smartcard-SDK stellt die folgenden COM-Schnittstellen bereit.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-108">The Smart Card SDK provides the following COM interfaces.</span></span> <span data-ttu-id="9bd1a-109">Die Methoden für eine bestimmte Schnittstelle werden im Inhaltsverzeichnis und auf der Referenzseite für diese Schnittstelle aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-109">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="9bd1a-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9bd1a-110">Interface</span></span>                                    | <span data-ttu-id="9bd1a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bd1a-111">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bd1a-112">**Ibytebuffer**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-112">**IByteBuffer**</span></span>](ibytebuffer.md)           | <span data-ttu-id="9bd1a-113">Verwaltet ein Stream-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-113">Manages a stream object.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="9bd1a-114">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-114">**ISCard**</span></span>](iscard.md)                     | <span data-ttu-id="9bd1a-115">Öffnet und verwaltet eine Verbindung mit einer [*Smartcard*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="9bd1a-115">Opens and manages a connection to a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span>                                                                    |
| [<span data-ttu-id="9bd1a-116">**Iscardauth**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-116">**ISCardAuth**</span></span>](iscardauth.md)             | <span data-ttu-id="9bd1a-117">Authentifiziert eine Anwendung, eine Smartcard oder einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-117">Authenticates an application, smart card, or user.</span></span>                                                                                                                                       |
| [<span data-ttu-id="9bd1a-118">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-118">**ISCardCmd**</span></span>](iscardcmd.md)               | <span data-ttu-id="9bd1a-119">Erstellt und verwaltet eine Smartcard-APDU ( [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) ).</span><span class="sxs-lookup"><span data-stu-id="9bd1a-119">Constructs and manages a smart card [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) (APDU).</span></span> |
| [<span data-ttu-id="9bd1a-120">**Iscarddatabase**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-120">**ISCardDatabase**</span></span>](iscarddatabase.md)     | <span data-ttu-id="9bd1a-121">Führt Smartcard- [*Ressourcen-Manager*](/windows/desktop/SecGloss/r-gly) -Daten Bank Vorgänge aus</span><span class="sxs-lookup"><span data-stu-id="9bd1a-121">Performs smart card [*resource manager*](/windows/desktop/SecGloss/r-gly) database operations.</span></span>                                              |
| [<span data-ttu-id="9bd1a-122">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md) | <span data-ttu-id="9bd1a-123">Führt allgemeine Dateidienste aus, z. b. suchen, auswählen, lesen, schreiben, erstellen und Löschen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-123">Performs common file services such as locating, selecting, reading, writing, creating, and deleting files.</span></span>                                                                               |
| [<span data-ttu-id="9bd1a-124">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-124">**ISCardISO7816**</span></span>](iscardiso7816.md)       | <span data-ttu-id="9bd1a-125">Erstellt einen APDU-Befehl.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-125">Constructs an APDU command.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="9bd1a-126">**Iscardsuche**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-126">**ISCardLocate**</span></span>](iscardlocate.md)         | <span data-ttu-id="9bd1a-127">Es wird eine Smartcard angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-127">Locates a smart card.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="9bd1a-128">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-128">**ISCardManage**</span></span>](iscardmanage.md)         | <span data-ttu-id="9bd1a-129">Verwaltet das Smartcardsystem.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-129">Manages the smart card system.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="9bd1a-130">**Iscardtypeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-130">**ISCardTypeConv**</span></span>](iscardtypeconv.md)     | <span data-ttu-id="9bd1a-131">Stellt Methoden zur Unterstützung anderer Smartcard-com-Schnittstellen bereit.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-131">Provides methods used to support other smart card COM interfaces.</span></span> <span data-ttu-id="9bd1a-132">Diese Schnittstelle wird nur aus Gründen der Abwärtskompatibilität bereitgestellt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-132">This interface is provided for backward compatibility only and should no longer be used.</span></span>                               |
| [<span data-ttu-id="9bd1a-133">**Iscardverify**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-133">**ISCardVerify**</span></span>](iscardverify.md)         | <span data-ttu-id="9bd1a-134">Überprüft oder ändert die Richtlinie der Karteninhaber Überprüfung (CHV).</span><span class="sxs-lookup"><span data-stu-id="9bd1a-134">Verifies or changes card holder verification (CHV) policy.</span></span>                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a><span data-ttu-id="9bd1a-135">Identitäts Freigabe Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9bd1a-135">Identity Sharing Interfaces</span></span>

<span data-ttu-id="9bd1a-136">Das Identitäts Freigabe-SDK stellt die folgenden COM-Schnittstellen bereit.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-136">The Identity Sharing SDK provides the following COM interfaces.</span></span> <span data-ttu-id="9bd1a-137">Die Methoden für eine bestimmte Schnittstelle werden im Inhaltsverzeichnis und auf der Referenzseite für diese Schnittstelle aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-137">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="9bd1a-138">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9bd1a-138">Interface</span></span>                                                          | <span data-ttu-id="9bd1a-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bd1a-139">Description</span></span>                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bd1a-140">**Iassociatedidentityprovider**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-140">**IAssociatedIdentityProvider**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | <span data-ttu-id="9bd1a-141">Ermöglicht einem Identitäts Anbieter das Zuordnen von Identitäten zu lokalen Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-141">Allows an identity provider to associate identities with local user accounts.</span></span>            |
| [<span data-ttu-id="9bd1a-142">**Iidentityrat**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-142">**IIdentityAdvise**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | <span data-ttu-id="9bd1a-143">Ermöglicht einem Identitäts Anbieter, eine aufrufende Anwendung zu benachrichtigen, wenn eine Identität aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-143">Allows an identity provider to notify a calling application when an identity is updated.</span></span> |
| [<span data-ttu-id="9bd1a-144">**Iidentityprovider**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-144">**IIdentityProvider**</span></span>](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | <span data-ttu-id="9bd1a-145">Stellt einen Identitätsanbieter dar.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-145">Represents an identity provider.</span></span>                                                         |
| [<span data-ttu-id="9bd1a-146">**Iidentitystore**</span><span class="sxs-lookup"><span data-stu-id="9bd1a-146">**IIdentityStore**</span></span>](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | <span data-ttu-id="9bd1a-147">Stellt Methoden zum Auflisten und Verwalten von Identitäten und Identitäts Anbietern bereit.</span><span class="sxs-lookup"><span data-stu-id="9bd1a-147">Provides methods to enumerate and manage identities and identity providers.</span></span>              |



 

 

 
