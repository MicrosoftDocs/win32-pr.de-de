---
title: Csecurechannelclient-Klasse
description: Csecurechannelclient-Klasse
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Device Manager, csecurechannelclient-Klasse
- Device Manager, csecurechannelclient-Klasse
- Desktop Anwendungen, csecurechannelclient-Klasse
- Programmier Referenz, csecurechannelclient-Klasse
- Referenz für Windows Media Device Manager, csecurechannelclient-Klasse
- Csecurechannelclient-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337439"
---
# <a name="csecurechannelclient-class"></a><span data-ttu-id="9a8b3-109">Csecurechannelclient-Klasse</span><span class="sxs-lookup"><span data-stu-id="9a8b3-109">CSecureChannelClient Class</span></span>

<span data-ttu-id="9a8b3-110">Die **csecurechannelclient** -Klasse ist eine Hilfsklasse (keine Schnittstelle), die es Anwendungen ermöglicht, sich selbst zu authentifizieren, Daten zu verschlüsseln und zu entschlüsseln und Macs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-110">The **CSecureChannelClient** class is a helper class (not an interface) that enables applications to authenticate themselves, encrypt and decrypt data, and create MACs.</span></span>

<span data-ttu-id="9a8b3-111">Die **csecurechannelclient** -Klasse stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-111">The **CSecureChannelClient** class exposes the following methods.</span></span>



| <span data-ttu-id="9a8b3-112">Methode</span><span class="sxs-lookup"><span data-stu-id="9a8b3-112">Method</span></span>                                                            | <span data-ttu-id="9a8b3-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a8b3-113">Description</span></span>                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a8b3-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span></span>         | <span data-ttu-id="9a8b3-115">Hiermit wird der Austausch von Zertifikaten zwischen Komponenten ausgelöst, um eine Vertrauensstellung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-115">Triggers the exchange of certificates between components to establish trust.</span></span>                                              |
| <span data-ttu-id="9a8b3-116">[**Decryptparam**](/previous-versions/bb231586(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span></span>         | <span data-ttu-id="9a8b3-117">Entschlüsselt Daten, die über einen Parameter empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-117">Decrypts data received through a parameter.</span></span>                                                                               |
| <span data-ttu-id="9a8b3-118">[**Verschlüsseltparam**](/previous-versions/bb231587(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span></span>         | <span data-ttu-id="9a8b3-119">Verschlüsselt Daten, die über einen Parameter gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-119">Encrypts data being sent out through a parameter.</span></span>                                                                         |
| <span data-ttu-id="9a8b3-120">[**fisauthenticated**](/previous-versions/ms868497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span></span> | <span data-ttu-id="9a8b3-121">Mit dieser Option wird überprüft, ob ein sicherer Authentifizierungs Kanal erfolgreich eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-121">Verifies that a secure authentication channel has been successfully established.</span></span> <span data-ttu-id="9a8b3-122">Diese Methode wird von Anwendungen nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-122">This method is not used by applications.</span></span> |
| <span data-ttu-id="9a8b3-123">[**Getappsec**](/previous-versions/ms868498(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span></span>               | <span data-ttu-id="9a8b3-124">Ruft die Anwendungs Sicherheitsgrade der lokalen Komponenten und Remote Komponenten ab.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-124">Retrieves the application security levels of the local and remote components.</span></span>                                             |
| <span data-ttu-id="9a8b3-125">[**Getessionkey**](/previous-versions/bb231590(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span></span>       | <span data-ttu-id="9a8b3-126">Ruft den aktuellen Sitzungsschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-126">Retrieves the current session key.</span></span> <span data-ttu-id="9a8b3-127">Diese Methode wird von Anwendungen nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-127">This method is not used by applications.</span></span>                                               |
| <span data-ttu-id="9a8b3-128">[**Macfinal**](/previous-versions/bb231591(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span></span>                 | <span data-ttu-id="9a8b3-129">Gibt den Mac-Kanal (Message Authentication Code) frei und Ruft einen abschließenden Mac-Wert ab.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-129">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>                                   |
| <span data-ttu-id="9a8b3-130">[**Macinit**](/previous-versions/bb231592(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span></span>                   | <span data-ttu-id="9a8b3-131">Ruft einen Mac-Kanal (Message Authentication Code) ab.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-131">Acquires a message authentication code (MAC) channel.</span></span>                                                                     |
| <span data-ttu-id="9a8b3-132">[**Macupdate**](/previous-versions/bb231593(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span></span>               | <span data-ttu-id="9a8b3-133">Fügt einem Nachrichten Authentifizierungscode (Message Authentication Code, Mac) einen Wert hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-133">Adds a value to a message authentication code (MAC).</span></span>                                                                      |
| <span data-ttu-id="9a8b3-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span></span>     | <span data-ttu-id="9a8b3-135">Gibt das Zertifikat und den privaten Schlüssel des SAC-Clients (Secure authentifiziert Channel) an.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-135">Specifies the certificate and private key of the secure authenticated channel (SAC) client.</span></span>                               |
| <span data-ttu-id="9a8b3-136">[**Setinterface**](/previous-versions/bb231595(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span></span>         | <span data-ttu-id="9a8b3-137">Wählt die für Secure authentifiziert Channel (SAC)-Kommunikation verwendete Schnittstelle aus.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-137">Selects the interface used for secure authenticated channel (SAC) communications.</span></span>                                         |
| <span data-ttu-id="9a8b3-138">[**"-Essionkey"**](/previous-versions/ms868506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9a8b3-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span></span>       | <span data-ttu-id="9a8b3-139">Legt den Sitzungsschlüssel fest, der für die Kommunikation mit einer anderen Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-139">Sets the session key that is used to communicate with another component.</span></span> <span data-ttu-id="9a8b3-140">Diese Methode wird von Anwendungen nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a8b3-140">This method is not used by applications.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="9a8b3-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a8b3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a8b3-142">**Csecurechannelserver-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9a8b3-142">**CSecureChannelServer Class**</span></span>](csecurechannelserver-class.md)
</dt> <dt>

[<span data-ttu-id="9a8b3-143">**Icomponentauthenticate-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9a8b3-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="9a8b3-144">**Schnittstellen für Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="9a8b3-144">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> </dl>

 

 