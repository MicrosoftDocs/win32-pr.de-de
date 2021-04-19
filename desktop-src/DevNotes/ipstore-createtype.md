---
description: Erstellt den angegebenen Typ mit dem angegebenen Namen.
ms.assetid: eb85477c-d750-46d2-8b32-450f672e7601
title: 'Ipstore:: kreatetype-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7a8c855fd5b50adf41986ef27a1bd296894b12bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369542"
---
# <a name="ipstorecreatetype-method"></a><span data-ttu-id="51544-103">Ipstore:: kreatetype-Methode</span><span class="sxs-lookup"><span data-stu-id="51544-103">IPStore::CreateType method</span></span>

<span data-ttu-id="51544-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51544-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="51544-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51544-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="51544-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="51544-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="51544-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="51544-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="51544-108">Erstellt den angegebenen Typ mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="51544-108">Creates the specified type with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="51544-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="51544-109">Syntax</span></span>


```C++
HRESULT CreateType(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO pInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="51544-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="51544-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51544-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51544-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51544-112">Gibt an, ob der Typ auf dem Computer lokal ist oder nur dem erstellerstellerbenutzer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="51544-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="51544-113">Wert</span><span class="sxs-lookup"><span data-stu-id="51544-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="51544-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="51544-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="51544-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="51544-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="51544-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="51544-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="51544-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="51544-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="51544-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="51544-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="51544-119">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51544-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51544-120">Ein Zeiger auf eine **GUID** , die den Datentyp des Speichers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51544-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="51544-121">*pinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51544-121">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51544-122">Ein Zeiger auf eine [**PST- \_ TypeInfo**](pst-typeinfo.md) -Struktur, die den Namen des Datentyps enthält.</span><span class="sxs-lookup"><span data-stu-id="51544-122">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure that contains the name of the data type.</span></span>

</dd> <dt>

<span data-ttu-id="51544-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51544-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51544-124">Reserviert: muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51544-124">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51544-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51544-125">Return value</span></span>

<span data-ttu-id="51544-126">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="51544-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="51544-127">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="51544-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="51544-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51544-128">Requirements</span></span>



| <span data-ttu-id="51544-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51544-129">Requirement</span></span> | <span data-ttu-id="51544-130">Wert</span><span class="sxs-lookup"><span data-stu-id="51544-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51544-131">Header</span><span class="sxs-lookup"><span data-stu-id="51544-131">Header</span></span><br/> | <dl> <span data-ttu-id="51544-132"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="51544-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="51544-133">DLL</span><span class="sxs-lookup"><span data-stu-id="51544-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="51544-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51544-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51544-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51544-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51544-136">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="51544-136">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="51544-137">**PST- \_ Typeingabe Info**</span><span class="sxs-lookup"><span data-stu-id="51544-137">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
