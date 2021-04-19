---
description: Stellt com-Standardmethoden zum Verwalten geschützter Speicherdaten Elemente bereit.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Ipstore-Schnittstelle (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373604"
---
# <a name="ipstore-interface"></a><span data-ttu-id="665d8-103">Ipstore-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="665d8-103">IPStore interface</span></span>

<span data-ttu-id="665d8-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="665d8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="665d8-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="665d8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="665d8-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="665d8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="665d8-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="665d8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="665d8-108">\[Diese Schnittstelle kann geändert werden oder ist in zukünftigen Versionen von Windows nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="665d8-108">\[This interface may be altered or unavailable in future versions of Windows.\]</span></span>

<span data-ttu-id="665d8-109">Stellt com-Standardmethoden zum Verwalten geschützter Speicherdaten Elemente bereit.</span><span class="sxs-lookup"><span data-stu-id="665d8-109">Provides COM-standard methods to manage protected storage data items.</span></span> <span data-ttu-id="665d8-110">Die [**pstorecreatanstance**](pstorecreateinstance.md) -Methode gibt einen Zeiger auf diese Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="665d8-110">The [**PStoreCreateInstance**](pstorecreateinstance.md) method returns a pointer to this interface.</span></span>

## <a name="members"></a><span data-ttu-id="665d8-111">Member</span><span class="sxs-lookup"><span data-stu-id="665d8-111">Members</span></span>

<span data-ttu-id="665d8-112">Die **ipstore** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="665d8-112">The **IPStore** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="665d8-113">**Ipstore** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="665d8-113">**IPStore** also has these types of members:</span></span>

-   [<span data-ttu-id="665d8-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="665d8-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="665d8-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="665d8-115">Methods</span></span>

<span data-ttu-id="665d8-116">Die **ipstore** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="665d8-116">The **IPStore** interface has these methods.</span></span>



| <span data-ttu-id="665d8-117">Methode</span><span class="sxs-lookup"><span data-stu-id="665d8-117">Method</span></span>                                                   | <span data-ttu-id="665d8-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="665d8-118">Description</span></span>                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="665d8-119">**Closeitem**</span><span class="sxs-lookup"><span data-stu-id="665d8-119">**CloseItem**</span></span>](ipstore-closeitem.md)                   | <span data-ttu-id="665d8-120">Schließt ein angegebenes Datenelement aus dem geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="665d8-120">Closes a specified data item from protected storage.</span></span><br/>                                                       |
| [<span data-ttu-id="665d8-121">**"Kreatesubtype"**</span><span class="sxs-lookup"><span data-stu-id="665d8-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)           | <span data-ttu-id="665d8-122">Erstellt den angegebenen Untertyp innerhalb des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="665d8-122">Creates the specified subtype within the specified type.</span></span><br/>                                                   |
| [<span data-ttu-id="665d8-123">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="665d8-123">**CreateType**</span></span>](ipstore-createtype.md)                 | <span data-ttu-id="665d8-124">Erstellt den angegebenen Typ mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="665d8-124">Creates the specified type with the specified name.</span></span><br/>                                                        |
| [<span data-ttu-id="665d8-125">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="665d8-125">**DeleteItem**</span></span>](ipstore-deleteitem.md)                 | <span data-ttu-id="665d8-126">Löscht das angegebene Element aus dem geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="665d8-126">Deletes the specified item from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="665d8-127">**Delta esubtype**</span><span class="sxs-lookup"><span data-stu-id="665d8-127">**DeleteSubtype**</span></span>](ipstore-deletesubtype.md)           | <span data-ttu-id="665d8-128">Löscht den angegebenen Element Untertyp aus dem geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="665d8-128">Deletes the specified item subtype from the protected storage.</span></span><br/>                                             |
| [<span data-ttu-id="665d8-129">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="665d8-129">**DeleteType**</span></span>](ipstore-deletetype.md)                 | <span data-ttu-id="665d8-130">Löscht den angegebenen Typ aus dem geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="665d8-130">Deletes the specified type from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="665d8-131">**-Elemente**</span><span class="sxs-lookup"><span data-stu-id="665d8-131">**EnumItems**</span></span>](ipstore-enumitems.md)                   | <span data-ttu-id="665d8-132">Gibt den Schnittstellen Zeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicher Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="665d8-132">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span><br/>        |
| [<span data-ttu-id="665d8-133">**Enumunter Typen**</span><span class="sxs-lookup"><span data-stu-id="665d8-133">**EnumSubtypes**</span></span>](ipstore-enumsubtypes.md)             | <span data-ttu-id="665d8-134">Gibt eine-Schnittstelle zum Auflisten von Untertypen der Typen zurück, die derzeit in der geschützten Datenbank registriert sind.</span><span class="sxs-lookup"><span data-stu-id="665d8-134">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span><br/> |
| [<span data-ttu-id="665d8-135">**Enumtypes**</span><span class="sxs-lookup"><span data-stu-id="665d8-135">**EnumTypes**</span></span>](ipstore-enumtypes.md)                   | <span data-ttu-id="665d8-136">Gibt eine-Schnittstelle zum Auflisten der Typen zurück, die derzeit in der geschützten Datenbank registriert sind.</span><span class="sxs-lookup"><span data-stu-id="665d8-136">Returns an interface for enumerating the types currently registered in the protected database.</span></span><br/>             |
| [<span data-ttu-id="665d8-137">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="665d8-137">**GetInfo**</span></span>](ipstore-getinfo.md)                       | <span data-ttu-id="665d8-138">Ruft Informationen zum Speicher Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="665d8-138">Retrieves information about the storage provider.</span></span><br/>                                                          |
| [<span data-ttu-id="665d8-139">**Getprovparam**</span><span class="sxs-lookup"><span data-stu-id="665d8-139">**GetProvParam**</span></span>](ipstore-getprovparam.md)             | <span data-ttu-id="665d8-140">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="665d8-140">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="665d8-141">**Getsubtypeingefo**</span><span class="sxs-lookup"><span data-stu-id="665d8-141">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)         | <span data-ttu-id="665d8-142">Ruft Informationen ab, die einem Untertyp zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="665d8-142">Retrieves information associated with a subtype.</span></span><br/>                                                           |
| [<span data-ttu-id="665d8-143">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="665d8-143">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)               | <span data-ttu-id="665d8-144">Ruft Informationen ab, die einem-Typ zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="665d8-144">Retrieves information associated with a type.</span></span><br/>                                                              |
| [<span data-ttu-id="665d8-145">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="665d8-145">**OpenItem**</span></span>](ipstore-openitem.md)                     | <span data-ttu-id="665d8-146">Öffnet ein Element für mehrere Zugriffe.</span><span class="sxs-lookup"><span data-stu-id="665d8-146">Opens an item for multiple accesses.</span></span><br/>                                                                       |
| [<span data-ttu-id="665d8-147">**"Read accessruleset"**</span><span class="sxs-lookup"><span data-stu-id="665d8-147">**ReadAccessRuleSet**</span></span>](ipstore-readaccessruleset.md)   | <span data-ttu-id="665d8-148">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="665d8-148">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="665d8-149">**"ReadItem"**</span><span class="sxs-lookup"><span data-stu-id="665d8-149">**ReadItem**</span></span>](ipstore-readitem.md)                     | <span data-ttu-id="665d8-150">Liest das angegebene Datenelement aus dem geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="665d8-150">Reads the specified data item from protected storage.</span></span><br/>                                                      |
| [<span data-ttu-id="665d8-151">**Setprovparam**</span><span class="sxs-lookup"><span data-stu-id="665d8-151">**SetProvParam**</span></span>](ipstore-setprovparam.md)             | <span data-ttu-id="665d8-152">Legt die angegebenen Parameterinformationen fest.</span><span class="sxs-lookup"><span data-stu-id="665d8-152">Sets the specified parameter information.</span></span><br/>                                                                  |
| [<span data-ttu-id="665d8-153">**"Write-accessruleset"**</span><span class="sxs-lookup"><span data-stu-id="665d8-153">**WriteAccessRuleset**</span></span>](ipstore-writeaccessruleset.md) | <span data-ttu-id="665d8-154">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="665d8-154">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="665d8-155">**Schreib Element**</span><span class="sxs-lookup"><span data-stu-id="665d8-155">**WriteItem**</span></span>](ipstore-writeitem.md)                   | <span data-ttu-id="665d8-156">Schreibt ein Datenelement in den geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="665d8-156">Writes a data item to protected storage.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="665d8-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="665d8-157">Requirements</span></span>



| <span data-ttu-id="665d8-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="665d8-158">Requirement</span></span> | <span data-ttu-id="665d8-159">Wert</span><span class="sxs-lookup"><span data-stu-id="665d8-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="665d8-160">Header</span><span class="sxs-lookup"><span data-stu-id="665d8-160">Header</span></span><br/> | <dl> <span data-ttu-id="665d8-161"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="665d8-161"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="665d8-162">DLL</span><span class="sxs-lookup"><span data-stu-id="665d8-162">DLL</span></span><br/>    | <dl> <span data-ttu-id="665d8-163"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="665d8-163"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
