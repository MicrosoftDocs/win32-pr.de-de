---
title: Iwmdrmlicenabmanagement-Schnittstelle
description: Die iwmdrmlicenabmanagement-Schnittstelle stellt Methoden bereit, die allgemeine Vorgänge im Zusammenhang mit dem lokalen Lizenz Speicher ausführen. Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie iwmdrmprovider-Erstellungsobjekt auf. Übergeben Sie IID \_ iwmdrmlicenpasmanagement als riid-Parameter.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Iwmdrmlicenabmanagement Interface Windows Media-Format
- Iwmdrmlicensmanagement Interface Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312480"
---
# <a name="iwmdrmlicensemanagement-interface"></a><span data-ttu-id="b5037-106">Iwmdrmlicenabmanagement-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b5037-106">IWMDRMLicenseManagement interface</span></span>

<span data-ttu-id="b5037-107">Die **iwmdrmlicenabmanagement** -Schnittstelle stellt Methoden bereit, die allgemeine Vorgänge im Zusammenhang mit dem lokalen Lizenz Speicher ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5037-107">The **IWMDRMLicenseManagement** interface provides methods that perform general operations related to the local license store.</span></span>

<span data-ttu-id="b5037-108">Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf.</span><span class="sxs-lookup"><span data-stu-id="b5037-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="b5037-109">Übergeben Sie **IID \_ iwmdrmlicenpasmanagement** als *riid* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="b5037-109">Pass **IID\_IWMDRMLicenseManagement** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="b5037-110">Member</span><span class="sxs-lookup"><span data-stu-id="b5037-110">Members</span></span>

<span data-ttu-id="b5037-111">Die **iwmdrmlicenermanagement** -Schnittstelle erbt von [**iwmdrmeventgenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="b5037-111">The **IWMDRMLicenseManagement** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="b5037-112">**Iwmdrmlicensmanagement** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b5037-112">**IWMDRMLicenseManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="b5037-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b5037-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b5037-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="b5037-114">Methods</span></span>

<span data-ttu-id="b5037-115">Die **iwmdrmlicenermanagement** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b5037-115">The **IWMDRMLicenseManagement** interface has these methods.</span></span>



| <span data-ttu-id="b5037-116">Methode</span><span class="sxs-lookup"><span data-stu-id="b5037-116">Method</span></span>                                                                                               | <span data-ttu-id="b5037-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5037-117">Description</span></span>                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5037-118">**AcquireLicense**</span><span class="sxs-lookup"><span data-stu-id="b5037-118">**AcquireLicense**</span></span>](iwmdrmlicensemanagement-acquirelicense.md)                                     | <span data-ttu-id="b5037-119">Ruft asynchron eine Lizenz von einer angegebenen URL ab.</span><span class="sxs-lookup"><span data-stu-id="b5037-119">Asynchronously acquires a license from a specified URL.</span></span><br/>                                                      |
| [<span data-ttu-id="b5037-120">**Backuplicenses**</span><span class="sxs-lookup"><span data-stu-id="b5037-120">**BackupLicenses**</span></span>](iwmdrmlicensemanagement-backuplicenses.md)                                     | <span data-ttu-id="b5037-121">Erstellt eine Sicherung der Lizenzen im lokalen Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="b5037-121">Creates a backup of the licenses in the local license store.</span></span><br/>                                                 |
| [<span data-ttu-id="b5037-122">**Cleanlicenabstore**</span><span class="sxs-lookup"><span data-stu-id="b5037-122">**CleanLicenseStore**</span></span>](iwmdrmlicensemanagement-cleanlicensestore.md)                               | <span data-ttu-id="b5037-123">Entfernt markierte Lizenzen aus dem Lizenz Speicher und zerlegt den Speicher, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="b5037-123">Removes marked licenses from the license store and defragments the store to improve performance.</span></span><br/>             |
| [<span data-ttu-id="b5037-124">**"-Enumeration"**</span><span class="sxs-lookup"><span data-stu-id="b5037-124">**CreateLicenseEnumeration**</span></span>](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | <span data-ttu-id="b5037-125">Erstellt ein Lizenz-Enumeratorobjekt, das anhand von Parameterwerten mit Lizenzinformationen aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="b5037-125">Creates a license enumerator object populated with license information based on parameter values.</span></span><br/>            |
| [<span data-ttu-id="b5037-126">**"Featelicenserevocationchallenge"**</span><span class="sxs-lookup"><span data-stu-id="b5037-126">**CreateLicenseRevocationChallenge**</span></span>](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | <span data-ttu-id="b5037-127">Generiert eine Lizenz Sperr Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="b5037-127">Generates a license revocation challenge.</span></span><br/>                                                                    |
| [<span data-ttu-id="b5037-128">**Delta eLicense**</span><span class="sxs-lookup"><span data-stu-id="b5037-128">**DeleteLicense**</span></span>](iwmdrmlicensemanagement-deletelicense.md)                                       | <span data-ttu-id="b5037-129">Löscht eine Lizenz aus dem temporären lokalen Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="b5037-129">Deletes a license from the temporary local license store.</span></span><br/>                                                    |
| [<span data-ttu-id="b5037-130">**Monitorlicensererwerbs**</span><span class="sxs-lookup"><span data-stu-id="b5037-130">**MonitorLicenseAcquisition**</span></span>](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | <span data-ttu-id="b5037-131">Initiiert die Überwachung für einen Lizenz Erwerbs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b5037-131">Initiates monitoring for a license acquisition process.</span></span><br/>                                                      |
| [<span data-ttu-id="b5037-132">**Processlicenabdeletionmessage**</span><span class="sxs-lookup"><span data-stu-id="b5037-132">**ProcessLicenseDeletionMessage**</span></span>](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | <span data-ttu-id="b5037-133">Löscht eine Lizenz, die für den ursprünglich mit einem anderen Inhalts Schutzsystem geschützten Inhalt importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b5037-133">Deletes a license that was imported for content originally protected with another content protection system.</span></span><br/> |
| [<span data-ttu-id="b5037-134">**Processlicenserevocationresponse**</span><span class="sxs-lookup"><span data-stu-id="b5037-134">**ProcessLicenseRevocationResponse**</span></span>](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | <span data-ttu-id="b5037-135">Widerruft Lizenzen aus dem lokalen Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="b5037-135">Revokes licenses from the local license store.</span></span><br/>                                                               |
| [<span data-ttu-id="b5037-136">**Restorelicenses**</span><span class="sxs-lookup"><span data-stu-id="b5037-136">**RestoreLicenses**</span></span>](iwmdrmlicensemanagement-restorelicenses.md)                                   | <span data-ttu-id="b5037-137">Stellt zuvor gesicherte Lizenzen wieder her.</span><span class="sxs-lookup"><span data-stu-id="b5037-137">Restores previously backed up licenses.</span></span><br/>                                                                      |
| [<span data-ttu-id="b5037-138">**Storelicense**</span><span class="sxs-lookup"><span data-stu-id="b5037-138">**StoreLicense**</span></span>](iwmdrmlicensemanagement-storelicense.md)                                         | <span data-ttu-id="b5037-139">Fügt eine Lizenz zum lokalen Lizenz Speicher hinzu.</span><span class="sxs-lookup"><span data-stu-id="b5037-139">Adds a license to the local license store.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="b5037-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5037-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5037-141">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="b5037-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b5037-142">**Iwmdrmeventgenerator**</span><span class="sxs-lookup"><span data-stu-id="b5037-142">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





