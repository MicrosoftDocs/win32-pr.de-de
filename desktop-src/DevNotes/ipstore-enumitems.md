---
description: Gibt den Schnittstellen Zeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicher Datenbank zurück.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'Ipstore:: tumitems-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9b44ee41a7daa4a75a19ca0f7045d69f5b380c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369630"
---
# <a name="ipstoreenumitems-method"></a><span data-ttu-id="0d3c2-103">Ipstore:: endms-Methode</span><span class="sxs-lookup"><span data-stu-id="0d3c2-103">IPStore::EnumItems method</span></span>

<span data-ttu-id="0d3c2-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0d3c2-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0d3c2-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0d3c2-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="0d3c2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0d3c2-108">Gibt den Schnittstellen Zeiger eines Untertyps zum Aufzählen von Elementen in der geschützten Speicher Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-108">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3c2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d3c2-109">Syntax</span></span>


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="0d3c2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d3c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d3c2-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d3c2-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3c2-112">Gibt an, ob der Typ auf dem Computer lokal ist oder nur dem erstellerstellerbenutzer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="0d3c2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0d3c2-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="0d3c2-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0d3c2-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="0d3c2-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0d3c2-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="0d3c2-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="0d3c2-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0d3c2-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0d3c2-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d3c2-119">*pitemtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d3c2-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3c2-120">Ein Zeiger auf eine **GUID** , die den Datentyp des aufzuzählenden Elements identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-120">A pointer to a **GUID** that identifies the data type of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="0d3c2-121">*pitemsubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d3c2-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3c2-122">Ein Zeiger auf eine **GUID** , die den Daten Untertyp des aufzuzählenden Elements identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-122">A pointer to a **GUID** that identifies the data subtype of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="0d3c2-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d3c2-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3c2-124">Reserviert: muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-124">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0d3c2-125">*ppum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d3c2-125">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d3c2-126">Ein Zeiger auf einen Zeiger auf eine [**iumumpstoreitems**](ienumpstoreitems.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-126">A pointer to a pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d3c2-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d3c2-127">Return value</span></span>

<span data-ttu-id="0d3c2-128">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="0d3c2-129">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0d3c2-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d3c2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d3c2-130">Requirements</span></span>



| <span data-ttu-id="0d3c2-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d3c2-131">Requirement</span></span> | <span data-ttu-id="0d3c2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="0d3c2-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3c2-133">Header</span><span class="sxs-lookup"><span data-stu-id="0d3c2-133">Header</span></span><br/> | <dl> <span data-ttu-id="0d3c2-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d3c2-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0d3c2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0d3c2-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="0d3c2-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d3c2-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d3c2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d3c2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3c2-138">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="0d3c2-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
