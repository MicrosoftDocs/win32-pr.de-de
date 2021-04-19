---
description: Schreibt ein Datenelement in den geschützten Speicher.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'Ipstore:: Write teitem-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370751"
---
# <a name="ipstorewriteitem-method"></a><span data-ttu-id="7d291-103">Ipstore:: Write teitem-Methode</span><span class="sxs-lookup"><span data-stu-id="7d291-103">IPStore::WriteItem method</span></span>

<span data-ttu-id="7d291-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d291-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="7d291-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d291-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="7d291-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="7d291-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="7d291-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="7d291-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="7d291-108">Schreibt ein Datenelement in den geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="7d291-108">Writes a data item to protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d291-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d291-109">Syntax</span></span>


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7d291-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d291-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d291-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d291-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-112">Der Speicherbereich des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="7d291-112">The provider storage area.</span></span>



| <span data-ttu-id="7d291-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7d291-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="7d291-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7d291-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="7d291-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="7d291-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="7d291-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7d291-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="7d291-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7d291-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="7d291-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7d291-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d291-119">*pitemtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d291-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-120">Ein Zeiger auf eine **GUID** , die den Datentyp des Datenelements identifiziert, das geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7d291-120">A pointer to a **GUID** that identifies the data type of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="7d291-121">*pitemsubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d291-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-122">Ein Zeiger auf eine **GUID** , die den Daten Untertyp des Datenelements identifiziert, das geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7d291-122">A pointer to a **GUID** that identifies the data subtype of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="7d291-123">" *szitemname* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="7d291-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-124">Ein Zeiger auf eine Zeichenfolge, die den Namen enthält, der dem gespeicherten Datenelement zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7d291-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="7d291-125">*cbData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7d291-125">*cbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-126">Ein Zeiger auf ein **DWORD** , das die Größe des Puffers angibt, der das gespeicherte Datenelement enthält.</span><span class="sxs-lookup"><span data-stu-id="7d291-126">A pointer to a **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="7d291-127">*ppbdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7d291-127">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-128">Ein Zeiger auf einen Puffer, der das Datenelement enthält, das geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7d291-128">A pointer to a buffer that contains the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="7d291-129">*pproomptinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d291-129">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-130">Zeiger auf eine [**PST- \_ promptinfo**](pst-promptinfo.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7d291-130">Pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7d291-131">*dwdefaultconfirmationstyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d291-131">*dwDefaultConfirmationStyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-132">Der standardmäßige Bestätigungs Stil.</span><span class="sxs-lookup"><span data-stu-id="7d291-132">The default confirmation style.</span></span>



| <span data-ttu-id="7d291-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7d291-133">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="7d291-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7d291-134">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <span data-ttu-id="7d291-135"><dt>**PST \_ CF \_ Standard**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="7d291-135"><dt>**PST\_CF\_DEFAULT**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="7d291-136">Ermöglicht es dem Benutzer, den Bestätigungs Stil auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7d291-136">Allows the user to choose the confirmation style.</span></span> <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <span data-ttu-id="7d291-137"><dt>**PST \_ CF \_ None**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7d291-137"><dt>**PST\_CF\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="7d291-138">Erzwingt die Erstellung eines automatischen Elements.</span><span class="sxs-lookup"><span data-stu-id="7d291-138">Forces silent item creation.</span></span> <br/>                      |



 

</dd> <dt>

<span data-ttu-id="7d291-139">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d291-139">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d291-140">Die Benutzeroberfläche und das Sicherheits Verhalten für den Schreibvorgang.</span><span class="sxs-lookup"><span data-stu-id="7d291-140">The user interface and security behaviors for the write operation.</span></span>



| <span data-ttu-id="7d291-141">Wert</span><span class="sxs-lookup"><span data-stu-id="7d291-141">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="7d291-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7d291-142">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <span data-ttu-id="7d291-143"><dt>**PST \_ Kein über \_ Schreiben**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="7d291-143"><dt>**PST\_NO\_OVERWRITE**</dt> <dt>0x00000002</dt></span></span> </dl>                            | <span data-ttu-id="7d291-144">Gibt an, dass das Element im geschützten Speicher erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d291-144">Specifies that the item be created in protected storage.</span></span> <span data-ttu-id="7d291-145">Das Überschreiben eines vorhandenen Elements ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="7d291-145">Overwriting of an existing item is disallowed.</span></span><br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="7d291-146"><dt>**PST \_ Uneingeschränktes \_ ItemData**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7d291-146"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="7d291-147">Gibt an, dass der Datenstrom nicht sicher ist.</span><span class="sxs-lookup"><span data-stu-id="7d291-147">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="7d291-148">Standardmäßig sind Element Aufrufe sicher.</span><span class="sxs-lookup"><span data-stu-id="7d291-148">By default, item calls are secure.</span></span><br/>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d291-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d291-149">Return value</span></span>

<span data-ttu-id="7d291-150">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="7d291-150">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="7d291-151">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7d291-151">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d291-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d291-152">Requirements</span></span>



| <span data-ttu-id="7d291-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d291-153">Requirement</span></span> | <span data-ttu-id="7d291-154">Wert</span><span class="sxs-lookup"><span data-stu-id="7d291-154">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d291-155">Header</span><span class="sxs-lookup"><span data-stu-id="7d291-155">Header</span></span><br/> | <dl> <span data-ttu-id="7d291-156"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d291-156"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="7d291-157">DLL</span><span class="sxs-lookup"><span data-stu-id="7d291-157">DLL</span></span><br/>    | <dl> <span data-ttu-id="7d291-158"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d291-158"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d291-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d291-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d291-160">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="7d291-160">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="7d291-161">**PST \_ promptinfo**</span><span class="sxs-lookup"><span data-stu-id="7d291-161">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
