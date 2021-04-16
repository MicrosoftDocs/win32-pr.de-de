---
title: Iwmdrmlicense-Schnittstelle
description: Die iwmdrmlicense-Schnittstelle stellt eine Liste mit mindestens einer Lizenz dar.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Iwmdrmlicense-Schnittstelle Windows Media-Format
- Iwmdrmlicense-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473580"
---
# <a name="iwmdrmlicense-interface"></a><span data-ttu-id="7bf1f-105">Iwmdrmlicense-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7bf1f-105">IWMDRMLicense interface</span></span>

<span data-ttu-id="7bf1f-106">Die **iwmdrmlicense** -Schnittstelle stellt eine Liste mit mindestens einer Lizenz dar.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-106">The **IWMDRMLicense** interface represents a list of one or more licenses.</span></span>

## <a name="members"></a><span data-ttu-id="7bf1f-107">Member</span><span class="sxs-lookup"><span data-stu-id="7bf1f-107">Members</span></span>

<span data-ttu-id="7bf1f-108">Die **iwmdrmlicense** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-108">The **IWMDRMLicense** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7bf1f-109">**Iwmdrmlicense** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7bf1f-109">**IWMDRMLicense** also has these types of members:</span></span>

-   [<span data-ttu-id="7bf1f-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7bf1f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7bf1f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7bf1f-111">Methods</span></span>

<span data-ttu-id="7bf1f-112">Die **iwmdrmlicense** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-112">The **IWMDRMLicense** interface has these methods.</span></span>



| <span data-ttu-id="7bf1f-113">Methode</span><span class="sxs-lookup"><span data-stu-id="7bf1f-113">Method</span></span>                                                                                   | <span data-ttu-id="7bf1f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bf1f-114">Description</span></span>                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bf1f-115">**Canpersistent**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-115">**CanPersist**</span></span>](iwmdrmlicense-canpersist.md)                                           | <span data-ttu-id="7bf1f-116">Fragt ab, ob die Lizenz in einem lokalen Lizenz Speicher persistent gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-116">Queries whether the license can be persisted on in a local license store.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="7bf1f-117">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-117">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)                                 | <span data-ttu-id="7bf1f-118">Erstellt ein Entschlüsselungsobjekt mit den Einstellungen der aktuellen Lizenz.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-118">Creates a decryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="7bf1f-119">**CreateEncryptor**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-119">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)                                 | <span data-ttu-id="7bf1f-120">Erstellt ein Verschlüsselungs Objekt mit den Einstellungen der aktuellen Lizenz.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-120">Creates an encryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="7bf1f-121">**"Kreatesecuredecryptor"**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-121">**CreateSecureDecryptor**</span></span>](iwmdrmlicense-createsecuredecryptor.md)                     | <span data-ttu-id="7bf1f-122">Erstellt ein sicheres Entschlüsselungs-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-122">Creates a secure decryptor object.</span></span> <span data-ttu-id="7bf1f-123">Der sichere entschlüsselungstyp unterscheidet sich vom normalen entschlüsselungstyp darin, dass er den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-123">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span><br/> |
| [<span data-ttu-id="7bf1f-124">**Getanalogvideorestrictionlevels**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-124">**GetAnalogVideoRestrictionLevels**</span></span>](iwmdrmlicense-getanalogvideorestrictionlevels.md) | <span data-ttu-id="7bf1f-125">Ruft alle analogen Video Einschränkungen ab, die für die aktuelle Lizenz festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-125">Retrieves all analog video restrictions set on the current license.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="7bf1f-126">**Getinclusionlist**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-126">**GetInclusionList**</span></span>](iwmdrmlicense-getinclusionlist.md)                               | <span data-ttu-id="7bf1f-127">Ruft die gesamte Inklusions Liste für die aktuelle Lizenz oder Lizenz Kette ab.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-127">Retrieves the entire inclusion list for the current license or license chain.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="7bf1f-128">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-128">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)                                           | <span data-ttu-id="7bf1f-129">Ruft die Lizenz als Extensible Markup Language (XML) oder XMR-Daten (Extensible Media Rights) ab.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-129">Retrieves the license as Extensible Markup Language (XML) or Extensible Media Rights (XMR) data.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="7bf1f-130">**Getliceneinproperty**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-130">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)                           | <span data-ttu-id="7bf1f-131">Ruft eine Eigenschaft aus der aktuellen Lizenz ab.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-131">Retrieves a property from the current license.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="7bf1f-132">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-132">**GetNext**</span></span>](iwmdrmlicense-getnext.md)                                                 | <span data-ttu-id="7bf1f-133">Lädt die Informationen über die nächste Lizenz in der Liste.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-133">Loads the information about the next license in the list.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="7bf1f-134">**Getoutputschutzlevels**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-134">**GetOutputProtectionLevels**</span></span>](iwmdrmlicense-getoutputprotectionlevels.md)             | <span data-ttu-id="7bf1f-135">Ruft Informationen zu allen Ausgabe Schutz Ebenen (opls) ab, die der Lizenz zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-135">Retrieves information about all output protection levels (OPLs) assigned to the license.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="7bf1f-136">**Persistlicense**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-136">**PersistLicense**</span></span>](iwmdrmlicense-persistlicense.md)                                   | <span data-ttu-id="7bf1f-137">Speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-137">Saves the current license from the temporary store into the permanent local license store.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="7bf1f-138">**Retenumeration**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-138">**ResetEnumeration**</span></span>](iwmdrmlicense-resetenumeration.md)                               | <span data-ttu-id="7bf1f-139">Setzt die Lizenz Liste auf den ursprünglichen Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="7bf1f-139">Resets the license list to its original state.</span></span><br/>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="7bf1f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bf1f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf1f-141">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="7bf1f-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

