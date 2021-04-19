---
description: Erstellt den angegebenen Untertyp innerhalb des angegebenen Typs.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'Ipstore:: kreatesubtype-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352863"
---
# <a name="ipstorecreatesubtype-method"></a><span data-ttu-id="d9374-103">Ipstore:: kreatesubtype-Methode</span><span class="sxs-lookup"><span data-stu-id="d9374-103">IPStore::CreateSubtype method</span></span>

<span data-ttu-id="d9374-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9374-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d9374-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9374-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d9374-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="d9374-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d9374-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="d9374-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d9374-108">Erstellt den angegebenen Untertyp innerhalb des angegebenen Typs.</span><span class="sxs-lookup"><span data-stu-id="d9374-108">Creates the specified subtype within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9374-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9374-109">Syntax</span></span>


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d9374-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9374-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9374-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9374-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9374-112">Gibt den Speicherbereich des Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="d9374-112">Specifies the provider storage area.</span></span>



| <span data-ttu-id="d9374-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d9374-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="d9374-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d9374-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="d9374-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d9374-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="d9374-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d9374-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="d9374-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d9374-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="d9374-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d9374-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d9374-119">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9374-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9374-120">Ein Zeiger auf eine **GUID** , die den Datentyp des Speichers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d9374-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="d9374-121">*psubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9374-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9374-122">Ein Zeiger auf eine **GUID** , die den Daten Untertyp des Speichers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d9374-122">A pointer to a **GUID** that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="d9374-123">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9374-123">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9374-124">Ein Zeiger auf eine [**PST- \_ TypInfo**](pst-typeinfo.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d9374-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d9374-125">*prules* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9374-125">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9374-126">Ein Zeiger auf eine [**PST- \_ accessruleset**](pst-accessruleset.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d9374-126">A pointer to a [**PST\_ACCESSRULESET**](pst-accessruleset.md) structure.</span></span>

<span data-ttu-id="d9374-127">**Windows XP:** Dieser Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d9374-127">**Windows XP:** This parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d9374-128">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9374-128">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9374-129">Bleiben muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d9374-129">Reserved; must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9374-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9374-130">Return value</span></span>

<span data-ttu-id="d9374-131">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="d9374-131">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="d9374-132">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d9374-132">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9374-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9374-133">Requirements</span></span>



| <span data-ttu-id="d9374-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9374-134">Requirement</span></span> | <span data-ttu-id="d9374-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d9374-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9374-136">Header</span><span class="sxs-lookup"><span data-stu-id="d9374-136">Header</span></span><br/> | <dl> <span data-ttu-id="d9374-137"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9374-137"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d9374-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d9374-138">DLL</span></span><br/>    | <dl> <span data-ttu-id="d9374-139"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9374-139"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9374-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9374-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9374-141">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="d9374-141">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="d9374-142">**PST- \_ accessruleset**</span><span class="sxs-lookup"><span data-stu-id="d9374-142">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> <dt>

[<span data-ttu-id="d9374-143">**PST- \_ Typeingabe Info**</span><span class="sxs-lookup"><span data-stu-id="d9374-143">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
