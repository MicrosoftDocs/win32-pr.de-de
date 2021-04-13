---
title: Iwmdrmsecurity-Schnittstelle
description: Die iwmdrmsecurity-Schnittstelle verwaltet eine Reihe von sicherheitsbezogenen Informationen für das Client Computer-und Digital Rights Management-Subsystem (DRM). Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie iwmdrmprovider-Erstellungsobjekt auf.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Iwmdrmsecurity-Schnittstelle Windows Media-Format
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312755"
---
# <a name="iwmdrmsecurity-interface"></a><span data-ttu-id="99da5-105">Iwmdrmsecurity-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="99da5-105">IWMDRMSecurity interface</span></span>

<span data-ttu-id="99da5-106">Die **iwmdrmsecurity** -Schnittstelle verwaltet eine Reihe von sicherheitsbezogenen Informationen für das Client Computer-und Digital Rights Management-Subsystem (DRM).</span><span class="sxs-lookup"><span data-stu-id="99da5-106">The **IWMDRMSecurity** interface manages a variety of security-related information for the client computer and digital rights management (DRM) subsystem.</span></span>

<span data-ttu-id="99da5-107">Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf.</span><span class="sxs-lookup"><span data-stu-id="99da5-107">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="99da5-108">Übergeben Sie **IID \_ iwmdrmsecurity** als *riid* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="99da5-108">Pass **IID\_IWMDRMSecurity** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="99da5-109">Member</span><span class="sxs-lookup"><span data-stu-id="99da5-109">Members</span></span>

<span data-ttu-id="99da5-110">Die **iwmdrmsecurity** -Schnittstelle erbt von [**iwmdrmeventgenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="99da5-110">The **IWMDRMSecurity** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="99da5-111">**Iwmdrmsecurity** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="99da5-111">**IWMDRMSecurity** also has these types of members:</span></span>

-   [<span data-ttu-id="99da5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="99da5-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="99da5-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="99da5-113">Methods</span></span>

<span data-ttu-id="99da5-114">Die **iwmdrmsecurity** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="99da5-114">The **IWMDRMSecurity** interface has these methods.</span></span>



| <span data-ttu-id="99da5-115">Methode</span><span class="sxs-lookup"><span data-stu-id="99da5-115">Method</span></span>                                                                                      | <span data-ttu-id="99da5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99da5-116">Description</span></span>                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99da5-117">**Checkcertforwiderruf**</span><span class="sxs-lookup"><span data-stu-id="99da5-117">**CheckCertForRevocation**</span></span>](iwmdrmsecurity-checkcertforrevocation.md)                     | <span data-ttu-id="99da5-118">Bestimmt, ob ein Zertifikat widerrufen wurde.</span><span class="sxs-lookup"><span data-stu-id="99da5-118">Determines whether a certificate has been revoked.</span></span><br/>                                                    |
| [<span data-ttu-id="99da5-119">**Getcontentenablersforrevocations**</span><span class="sxs-lookup"><span data-stu-id="99da5-119">**GetContentEnablersForRevocations**</span></span>](iwmdrmsecurity-getcontentenablersforrevocations.md) | <span data-ttu-id="99da5-120">Ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten basierend auf gesperrten Zertifikaten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="99da5-120">Retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span><br/> |
| [<span data-ttu-id="99da5-121">**Getcontentenablersfromhashes**</span><span class="sxs-lookup"><span data-stu-id="99da5-121">**GetContentEnablersFromHashes**</span></span>](iwmdrmsecurity-getcontentenablersfromhashes.md)         | <span data-ttu-id="99da5-122">Ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten auf der Grundlage von Hash Zertifikaten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="99da5-122">Retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span><br/>  |
| [<span data-ttu-id="99da5-123">**Getmachinecertificate**</span><span class="sxs-lookup"><span data-stu-id="99da5-123">**GetMachineCertificate**</span></span>](iwmdrmsecurity-getmachinecertificate.md)                       | <span data-ttu-id="99da5-124">Ruft das Computer Zertifikat des DRM-Subsystems auf dem Client Computer ab.</span><span class="sxs-lookup"><span data-stu-id="99da5-124">Retrieves the machine certificate of the DRM subsystem on the client computer.</span></span><br/>                        |
| [<span data-ttu-id="99da5-125">**Getrevocationdata**</span><span class="sxs-lookup"><span data-stu-id="99da5-125">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)                               | <span data-ttu-id="99da5-126">Ruft eine Zertifikat Sperr Liste aus dem lokalen Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="99da5-126">Retrieves a certificate revocation list from the local store.</span></span><br/>                                         |
| [<span data-ttu-id="99da5-127">**Getrevocationdataversion**</span><span class="sxs-lookup"><span data-stu-id="99da5-127">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)                 | <span data-ttu-id="99da5-128">Ruft die Versionsnummer einer Zertifikat Sperr Liste im lokalen Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="99da5-128">Retrieves the version number of a certificate revocation list in the local store.</span></span><br/>                     |
| [<span data-ttu-id="99da5-129">**Getsecurityversion**</span><span class="sxs-lookup"><span data-stu-id="99da5-129">**GetSecurityVersion**</span></span>](iwmdrmsecurity-getsecurityversion.md)                             | <span data-ttu-id="99da5-130">Ruft die Version des DRM-Subsystems auf dem Client Computer ab.</span><span class="sxs-lookup"><span data-stu-id="99da5-130">Retrieves the version of the DRM subsystem on the client computer.</span></span><br/>                                    |
| [<span data-ttu-id="99da5-131">**Performsecurityupdate**</span><span class="sxs-lookup"><span data-stu-id="99da5-131">**PerformSecurityUpdate**</span></span>](iwmdrmsecurity-performsecurityupdate.md)                       | <span data-ttu-id="99da5-132">Initiiert ein Sicherheitsupdate des DRM-Subsystems auf dem Client Computer.</span><span class="sxs-lookup"><span data-stu-id="99da5-132">Initiates a security update to the DRM subsystem on the client computer.</span></span><br/>                              |
| [<span data-ttu-id="99da5-133">**"Abtrevocationdata"**</span><span class="sxs-lookup"><span data-stu-id="99da5-133">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)                               | <span data-ttu-id="99da5-134">Legt eine Zertifikat Sperr Liste im lokalen Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="99da5-134">Sets a certificate revocation list in the local store.</span></span><br/>                                                |



 

## <a name="see-also"></a><span data-ttu-id="99da5-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99da5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99da5-136">**Beispiel für DRM-Individualisierung**</span><span class="sxs-lookup"><span data-stu-id="99da5-136">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="99da5-137">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="99da5-137">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="99da5-138">**Iwmdrmeventgenerator**</span><span class="sxs-lookup"><span data-stu-id="99da5-138">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





