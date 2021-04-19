---
description: Stellt den einem Zertifikat zugeordneten privaten Schlüssel dar.
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: PrivateKey-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364804"
---
# <a name="privatekey-object"></a><span data-ttu-id="bfeaf-103">PrivateKey-Objekt</span><span class="sxs-lookup"><span data-stu-id="bfeaf-103">PrivateKey object</span></span>

<span data-ttu-id="bfeaf-104">\[Das **PrivateKey** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-104">\[The **PrivateKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bfeaf-105">Verwenden Sie stattdessen die [**X509Certificate2. PrivateKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="bfeaf-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bfeaf-106">Das **PrivateKey** -Objekt stellt den einem Zertifikat zugeordneten [*privaten Schlüssel*](../secgloss/p-gly.md) dar.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-106">The **PrivateKey** object represents the [*private key*](../secgloss/p-gly.md) associated with a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="bfeaf-107">Verwendung</span><span class="sxs-lookup"><span data-stu-id="bfeaf-107">When to use</span></span>

<span data-ttu-id="bfeaf-108">Das **PrivateKey** -Objekt wird verwendet, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="bfeaf-108">The **PrivateKey** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="bfeaf-109">Abrufen von Informationen zum privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-109">Retrieve information about the private key.</span></span>
-   <span data-ttu-id="bfeaf-110">Öffnen Sie den Container für den privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-110">Open the private key container.</span></span>
-   <span data-ttu-id="bfeaf-111">Löschen Sie den privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-111">Delete the private key.</span></span>

## <a name="members"></a><span data-ttu-id="bfeaf-112">Member</span><span class="sxs-lookup"><span data-stu-id="bfeaf-112">Members</span></span>

<span data-ttu-id="bfeaf-113">Das **PrivateKey** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bfeaf-113">The **PrivateKey** object has these types of members:</span></span>

-   [<span data-ttu-id="bfeaf-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="bfeaf-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="bfeaf-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfeaf-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bfeaf-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="bfeaf-116">Methods</span></span>

<span data-ttu-id="bfeaf-117">Das **PrivateKey** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-117">The **PrivateKey** object has these methods.</span></span>



| <span data-ttu-id="bfeaf-118">Methode</span><span class="sxs-lookup"><span data-stu-id="bfeaf-118">Method</span></span>                                                  | <span data-ttu-id="bfeaf-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfeaf-119">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfeaf-120">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-120">**Delete**</span></span>](privatekey-delete.md)                     | <span data-ttu-id="bfeaf-121">Löscht den Container für den privaten Schlüssel, auf den vom **PrivateKey** -Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-121">Deletes the private key container referenced by the **PrivateKey** object.</span></span><br/>                                                                                |
| [<span data-ttu-id="bfeaf-122">**IsAccessible**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-122">**IsAccessible**</span></span>](privatekey-isaccessible.md)         | <span data-ttu-id="bfeaf-123">Ruft einen booleschen Wert ab, der angibt, ob der Benutzer auf den privaten Schlüssel zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-123">Retrieves a Boolean value that indicates whether the private key is accessible by the user.</span></span> <span data-ttu-id="bfeaf-124">True gibt an, dass der Benutzer auf den privaten Schlüssel zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-124">If true, the user can access the private key.</span></span><br/>                 |
| [<span data-ttu-id="bfeaf-125">**IsExportable**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-125">**IsExportable**</span></span>](privatekey-isexportable.md)         | <span data-ttu-id="bfeaf-126">Ruft einen booleschen Wert ab, der angibt, ob der private Schlüssel exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-126">Retrieves a Boolean value that indicates whether the private key can be exported.</span></span> <span data-ttu-id="bfeaf-127">True gibt an, dass der private Schlüssel exportiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-127">If true, the private key can be exported.</span></span><br/>                               |
| [<span data-ttu-id="bfeaf-128">**Ishardwaredevice**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-128">**IsHardwareDevice**</span></span>](privatekey-ishardwaredevice.md) | <span data-ttu-id="bfeaf-129">Ruft einen booleschen Wert ab, der angibt, ob der private Schlüssel auf einem Hardware Gerät gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-129">Retrieves a Boolean value that indicates whether the private key is stored on a hardware device.</span></span> <span data-ttu-id="bfeaf-130">True gibt an, dass der private Schlüssel auf einem Hardware Gerät gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-130">If true, the private key is stored on a hardware device.</span></span><br/> |
| [<span data-ttu-id="bfeaf-131">**Ismachinekeyset**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-131">**IsMachineKeyset**</span></span>](privatekey-ismachinekeyset.md)   | <span data-ttu-id="bfeaf-132">Ruft einen booleschen Wert ab, der angibt, ob der private Schlüssel ein Computer Schlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-132">Retrieves a Boolean value that indicates whether the private key is a machine key.</span></span> <span data-ttu-id="bfeaf-133">True gibt an, dass der private Schlüssel ein Computer Schlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-133">If true, the private key is a machine key.</span></span><br/>                             |
| [<span data-ttu-id="bfeaf-134">**Isprotehiert**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-134">**IsProtected**</span></span>](privatekey-isprotected.md)           | <span data-ttu-id="bfeaf-135">Ruft einen booleschen Wert ab, der angibt, ob der private Schlüssel geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-135">Retrieves a Boolean value that indicates whether the private key is protected.</span></span> <span data-ttu-id="bfeaf-136">True gibt an, dass der private Schlüssel geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-136">If true, the private key is protected.</span></span><br/>                                     |
| [<span data-ttu-id="bfeaf-137">**Iswechsel**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-137">**IsRemovable**</span></span>](privatekey-isremovable.md)           | <span data-ttu-id="bfeaf-138">Ruft einen booleschen Wert ab, der angibt, ob sich der private Schlüssel auf einem Wechselmedium befindet.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-138">Retrieves a Boolean value that indicates whether the private key is on a removable device.</span></span> <span data-ttu-id="bfeaf-139">True gibt an, dass sich der private Schlüssel auf einem Wechsel Datenträger befindet.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-139">If true, the private key is on a removable device.</span></span><br/>             |
| [<span data-ttu-id="bfeaf-140">**Eren**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-140">**Open**</span></span>](privatekey-open.md)                         | <span data-ttu-id="bfeaf-141">Greift auf einen vorhandenen Schlüssel Container zu.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-141">Accesses an existing key container.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="bfeaf-142">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bfeaf-142">Properties</span></span>

<span data-ttu-id="bfeaf-143">Das **PrivateKey** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-143">The **PrivateKey** object has these properties.</span></span>



| <span data-ttu-id="bfeaf-144">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bfeaf-144">Property</span></span>                                                                 | <span data-ttu-id="bfeaf-145">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="bfeaf-145">Access type</span></span>          | <span data-ttu-id="bfeaf-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfeaf-146">Description</span></span>                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfeaf-147">**Container Name**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-147">**ContainerName**</span></span>](privatekey-containername.md)<br/>             | <span data-ttu-id="bfeaf-148">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bfeaf-148">Read-only</span></span><br/> | <span data-ttu-id="bfeaf-149">Ruft eine Zeichenfolge ab, die den Namen des privaten Schlüssel Containers enthält.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-149">Retrieves a string that contains the private key container name.</span></span> <span data-ttu-id="bfeaf-150">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-150">This is the default property.</span></span><br/> |
| [<span data-ttu-id="bfeaf-151">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-151">**KeySpec**</span></span>](privatekey-keyspec.md)<br/>                         | <span data-ttu-id="bfeaf-152">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bfeaf-152">Read-only</span></span><br/> | <span data-ttu-id="bfeaf-153">Ruft die Schlüssel Spezifikation ab.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-153">Retrieves the key specification.</span></span><br/>                                                               |
| [<span data-ttu-id="bfeaf-154">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-154">**ProviderName**</span></span>](privatekey-providername.md)<br/>               | <span data-ttu-id="bfeaf-155">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bfeaf-155">Read-only</span></span><br/> | <span data-ttu-id="bfeaf-156">Ruft eine Zeichenfolge ab, die den Namen des CSP enthält.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-156">Retrieves a string that contains the name of the CSP.</span></span><br/>                                          |
| [<span data-ttu-id="bfeaf-157">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-157">**ProviderType**</span></span>](privatekey-providertype.md)<br/>               | <span data-ttu-id="bfeaf-158">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bfeaf-158">Read-only</span></span><br/> | <span data-ttu-id="bfeaf-159">Ruft einen Enumerationswert ab, der den Typ des Anbieters angibt.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-159">Retrieves an enumeration value that specifies the type of provider.</span></span><br/>                            |
| [<span data-ttu-id="bfeaf-160">**Uniquecontainername**</span><span class="sxs-lookup"><span data-stu-id="bfeaf-160">**UniqueContainerName**</span></span>](privatekey-uniquecontainername.md)<br/> | <span data-ttu-id="bfeaf-161">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bfeaf-161">Read-only</span></span><br/> | <span data-ttu-id="bfeaf-162">Ruft eine Zeichenfolge ab, die den eindeutigen Container Namen des privaten Schlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-162">Retrieves a string that contains the unique private key container name.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="bfeaf-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfeaf-163">Remarks</span></span>

<span data-ttu-id="bfeaf-164">Das **PrivateKey** -Objekt kann erstellt werden und ist für die Skripterstellung sicher.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-164">The **PrivateKey** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="bfeaf-165">Die ProgID für das **PrivateKey** -Objekt ist CAPICOM. PrivateKey. 1.</span><span class="sxs-lookup"><span data-stu-id="bfeaf-165">The ProgID for the **PrivateKey** object is CAPICOM.PrivateKey.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfeaf-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfeaf-166">Requirements</span></span>



| <span data-ttu-id="bfeaf-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfeaf-167">Requirement</span></span> | <span data-ttu-id="bfeaf-168">Wert</span><span class="sxs-lookup"><span data-stu-id="bfeaf-168">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfeaf-169">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="bfeaf-169">Redistributable</span></span><br/> | <span data-ttu-id="bfeaf-170">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="bfeaf-170">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bfeaf-171">DLL</span><span class="sxs-lookup"><span data-stu-id="bfeaf-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="bfeaf-172"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfeaf-172"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
