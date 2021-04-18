---
description: Löscht einen angegebenen Untertyp aus dem angegebenen Typ.
ms.assetid: 1c44a609-80af-4e28-b1b5-2b4faea143bd
title: Ipstore::D eletesubtype-Methode (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 6fd89c1dd00a71cb843596e08bc168b90008b180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365581"
---
# <a name="ipstoredeletesubtype-method"></a><span data-ttu-id="4381f-103">Ipstore::D eletesubtype-Methode</span><span class="sxs-lookup"><span data-stu-id="4381f-103">IPStore::DeleteSubtype method</span></span>

<span data-ttu-id="4381f-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4381f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4381f-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4381f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4381f-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="4381f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4381f-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="4381f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4381f-108">Löscht einen angegebenen Untertyp aus dem angegebenen Typ.</span><span class="sxs-lookup"><span data-stu-id="4381f-108">Deletes a specified subtype from within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4381f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4381f-109">Syntax</span></span>


```C++
HRESULT DeleteSubtype(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in] const GUID    *pSubtype,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4381f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4381f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4381f-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4381f-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4381f-112">Gibt an, ob der Typ auf dem Computer lokal ist oder nur dem erstellerstellerbenutzer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4381f-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="4381f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4381f-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4381f-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4381f-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="4381f-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="4381f-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="4381f-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4381f-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="4381f-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4381f-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4381f-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4381f-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4381f-119">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4381f-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4381f-120">Ein Zeiger auf eine GUID, die den Datentyp des Speichers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4381f-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="4381f-121">*psubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4381f-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4381f-122">Ein Zeiger auf eine GUID, die den Daten Untertyp des Speichers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4381f-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="4381f-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4381f-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4381f-124">Reserviert: muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4381f-124">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4381f-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4381f-125">Return value</span></span>

<span data-ttu-id="4381f-126">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="4381f-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="4381f-127">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4381f-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4381f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4381f-128">Requirements</span></span>



| <span data-ttu-id="4381f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4381f-129">Requirement</span></span> | <span data-ttu-id="4381f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="4381f-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4381f-131">Header</span><span class="sxs-lookup"><span data-stu-id="4381f-131">Header</span></span><br/> | <dl> <span data-ttu-id="4381f-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4381f-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4381f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4381f-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="4381f-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4381f-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4381f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4381f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4381f-136">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="4381f-136">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
