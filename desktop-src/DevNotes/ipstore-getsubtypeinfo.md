---
description: Ruft Informationen ab, die einem Untertyp zugeordnet sind.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: 'Ipstore:: getsubtypeinfo-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: db7cb02d1c21b8bb1717514a6347339065e4f112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365709"
---
# <a name="ipstoregetsubtypeinfo-method"></a><span data-ttu-id="e7a6b-103">Ipstore:: getsubtypeinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="e7a6b-103">IPStore::GetSubtypeInfo method</span></span>

<span data-ttu-id="e7a6b-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="e7a6b-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="e7a6b-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="e7a6b-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="e7a6b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="e7a6b-108">Ruft Informationen ab, die einem Untertyp zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-108">Retrieves information associated with a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a6b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7a6b-109">Syntax</span></span>


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e7a6b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7a6b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7a6b-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7a6b-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a6b-112">Der Speicherbereich des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-112">The provider storage area.</span></span>



| <span data-ttu-id="e7a6b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e7a6b-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="e7a6b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e7a6b-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="e7a6b-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="e7a6b-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="e7a6b-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="e7a6b-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e7a6b-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="e7a6b-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e7a6b-119">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7a6b-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a6b-120">Ein Zeiger auf eine GUID, die den Datentyp des Speichers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="e7a6b-121">*psubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7a6b-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a6b-122">Ein Zeiger auf eine GUID, die den Daten Untertyp des Speichers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="e7a6b-123">*ppinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7a6b-123">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a6b-124">Ein Zeiger auf eine [**PST- \_ TypInfo**](pst-typeinfo.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e7a6b-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7a6b-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7a6b-126">Reserviert: muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7a6b-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7a6b-127">Return value</span></span>

<span data-ttu-id="e7a6b-128">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="e7a6b-129">Der Wert PST \_ E OK gibt an, dass \_ die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-129">A value of PST\_E\_OK indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a6b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7a6b-130">Requirements</span></span>



| <span data-ttu-id="e7a6b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7a6b-131">Requirement</span></span> | <span data-ttu-id="e7a6b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e7a6b-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a6b-133">Header</span><span class="sxs-lookup"><span data-stu-id="e7a6b-133">Header</span></span><br/> | <dl> <span data-ttu-id="e7a6b-134"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7a6b-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="e7a6b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e7a6b-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="e7a6b-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a6b-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7a6b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7a6b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a6b-138">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="e7a6b-138">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="e7a6b-139">**PST- \_ Typeingabe Info**</span><span class="sxs-lookup"><span data-stu-id="e7a6b-139">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
