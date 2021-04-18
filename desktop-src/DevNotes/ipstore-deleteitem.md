---
description: Löscht das angegebene Element aus dem geschützten Speicher.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: Ipstore::D eleteitem-Methode (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368681"
---
# <a name="ipstoredeleteitem-method"></a><span data-ttu-id="10b38-103">Ipstore::D eleteitem-Methode</span><span class="sxs-lookup"><span data-stu-id="10b38-103">IPStore::DeleteItem method</span></span>

<span data-ttu-id="10b38-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10b38-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="10b38-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10b38-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="10b38-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="10b38-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="10b38-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="10b38-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="10b38-108">Löscht das angegebene Element aus dem geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="10b38-108">Deletes the specified item from the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b38-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="10b38-109">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="10b38-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10b38-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b38-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10b38-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b38-112">Der Speicherbereich des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="10b38-112">The provider storage area.</span></span>



| <span data-ttu-id="10b38-113">Wert</span><span class="sxs-lookup"><span data-stu-id="10b38-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="10b38-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="10b38-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="10b38-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="10b38-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="10b38-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="10b38-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="10b38-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="10b38-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="10b38-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="10b38-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="10b38-119">*pitemtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10b38-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b38-120">Ein Zeiger auf eine **GUID** , die den Datentyp des zu löschenden Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="10b38-120">A pointer to a **GUID** that identifies the data type of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="10b38-121">*pitemsubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10b38-121">*pItemSubType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b38-122">Eine **GUID** , die den zu löschenden Element Untertyp angibt.</span><span class="sxs-lookup"><span data-stu-id="10b38-122">A **GUID** that indicates the item subtype to delete.</span></span>

</dd> <dt>

<span data-ttu-id="10b38-123">" *szitemname* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="10b38-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b38-124">Eine Zeichenfolge, die den Namen des zu löschenden Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="10b38-124">A string that contains the name of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="10b38-125">*ppromptinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10b38-125">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b38-126">Ein Zeiger auf eine [**PST- \_ promptinfo**](pst-promptinfo.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="10b38-126">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="10b38-127">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10b38-127">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b38-128">Gibt die Benutzeroberfläche und das Sicherheits Verhalten für den Löschvorgang an.</span><span class="sxs-lookup"><span data-stu-id="10b38-128">Specifies user interface and security behaviors for the delete operation.</span></span>



| <span data-ttu-id="10b38-129">Wert</span><span class="sxs-lookup"><span data-stu-id="10b38-129">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="10b38-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="10b38-130">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="10b38-131"><dt>**PST \_ Keine \_ UI- \_ Migration**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="10b38-131"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="10b38-132">Zeigen Sie die Benutzeroberfläche nur an, wenn ein benutzerdefiniertes Kennwort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="10b38-132">Do not show user interface unless a custom password is required.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b38-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10b38-133">Return value</span></span>

<span data-ttu-id="10b38-134">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="10b38-134">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="10b38-135">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="10b38-135">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b38-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10b38-136">Requirements</span></span>



| <span data-ttu-id="10b38-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10b38-137">Requirement</span></span> | <span data-ttu-id="10b38-138">Wert</span><span class="sxs-lookup"><span data-stu-id="10b38-138">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10b38-139">Header</span><span class="sxs-lookup"><span data-stu-id="10b38-139">Header</span></span><br/> | <dl> <span data-ttu-id="10b38-140"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b38-140"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="10b38-141">DLL</span><span class="sxs-lookup"><span data-stu-id="10b38-141">DLL</span></span><br/>    | <dl> <span data-ttu-id="10b38-142"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10b38-142"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10b38-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10b38-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b38-144">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="10b38-144">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="10b38-145">**PST \_ promptinfo**</span><span class="sxs-lookup"><span data-stu-id="10b38-145">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
