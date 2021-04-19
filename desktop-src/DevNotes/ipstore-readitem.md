---
description: Liest das angegebene Datenelement aus dem geschützten Speicher.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'Ipstore:: ReadItem-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359734"
---
# <a name="ipstorereaditem-method"></a><span data-ttu-id="7ecd5-103">Ipstore:: ReadItem-Methode</span><span class="sxs-lookup"><span data-stu-id="7ecd5-103">IPStore::ReadItem method</span></span>

<span data-ttu-id="7ecd5-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="7ecd5-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="7ecd5-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="7ecd5-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="7ecd5-108">Liest das angegebene Datenelement aus dem geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-108">Reads the specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ecd5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ecd5-109">Syntax</span></span>


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7ecd5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ecd5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ecd5-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ecd5-112">Der Speicherbereich des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-112">The provider storage area.</span></span>



| <span data-ttu-id="7ecd5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7ecd5-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="7ecd5-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7ecd5-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="7ecd5-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="7ecd5-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="7ecd5-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="7ecd5-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="7ecd5-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="7ecd5-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7ecd5-119">*pitemtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ecd5-120">Ein Zeiger auf eine GUID, die den Datentyp des zu lesenden Elements identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-120">A pointer to a GUID that identifies the data type of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="7ecd5-121">*pitemsubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ecd5-122">Ein Zeiger auf eine GUID, die den Daten Untertyp des zu lesenden Elements identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-122">A pointer to a GUID that identifies the data subtype of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="7ecd5-123">" *szitemname* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ecd5-124">Ein Zeiger auf eine Zeichenfolge, die den Namen enthält, der dem gespeicherten Datenelement zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="7ecd5-125">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-125">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ecd5-126">Ein **DWORD** , das die Größe des Puffers angibt, der das gespeicherte Datenelement enthält.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-126">A **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="7ecd5-127">*pbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-127">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ecd5-128">Ein Zeiger auf einen Puffer, der das gespeicherte Datenelement enthält.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-128">A pointer to a buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="7ecd5-129">*ppromptinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-129">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ecd5-130">Ein Zeiger auf eine [**PST- \_ promptinfo**](pst-promptinfo.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-130">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7ecd5-131">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ecd5-131">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ecd5-132">Gibt die Benutzeroberfläche und das Sicherheits Verhalten für den Lesevorgang an.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-132">Specifies user interface and security behaviors for the read operation.</span></span>

<span data-ttu-id="7ecd5-133">Die Flagwerte können mit einem logischen OR kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-133">The flag values can be combined with a logical OR.</span></span>



| <span data-ttu-id="7ecd5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="7ecd5-134">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="7ecd5-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7ecd5-135">Meaning</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="7ecd5-136"><dt>**PST \_ Uneingeschränktes \_ ItemData**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="7ecd5-136"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="7ecd5-137">Gibt an, dass der Datenstrom nicht sicher ist.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-137">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="7ecd5-138">Standardmäßig sind Element Aufrufe sicher.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-138">By default, item calls are secure.</span></span><br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <span data-ttu-id="7ecd5-139"><dt>**PST \_ \_Abfrage der Abfrage**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="7ecd5-139"><dt>**PST\_PROMPT\_QUERY**</dt> <dt>0x00000008</dt></span></span> </dl>                            | <span data-ttu-id="7ecd5-140">Gibt an, dass die Bestätigung bei Erfolg zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-140">Specifies that the confirmation be returned upon success.</span></span> <span data-ttu-id="7ecd5-141">Wenn die Benutzeroberfläche aktiviert ist, wird der Erfolg **PST \_ E \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-141">If the user interface is enabled, a success of **PST\_E\_OK** is returned.</span></span> <span data-ttu-id="7ecd5-142">Wenn die Benutzeroberfläche nicht aktiviert ist, wird der Wert **" \_ PST \_ E \_ Item** " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-142">If the user interface is not enabled, a value of **PST\_E\_ITEM\_EXISTS** is returned.</span></span><br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="7ecd5-143"><dt>**PST \_ Keine \_ UI- \_ Migration**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="7ecd5-143"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl>                  | <span data-ttu-id="7ecd5-144">Zeigen Sie die Benutzeroberfläche nur an, wenn ein benutzerdefiniertes Kennwort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-144">Do not show user interface unless a custom password is required.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ecd5-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ecd5-145">Return value</span></span>

<span data-ttu-id="7ecd5-146">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-146">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="7ecd5-147">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-147">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ecd5-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ecd5-148">Remarks</span></span>

<span data-ttu-id="7ecd5-149">Wenn **ReadItem** erfolgreich abgeschlossen wird, ist die Anwendung dafür verantwortlich, den zurückgegebenen Datenpuffer mithilfe der [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) -Funktion freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7ecd5-149">If **ReadItem** completes successfully, the application is responsible for freeing the returned data buffer using the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ecd5-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ecd5-150">Requirements</span></span>



| <span data-ttu-id="7ecd5-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ecd5-151">Requirement</span></span> | <span data-ttu-id="7ecd5-152">Wert</span><span class="sxs-lookup"><span data-stu-id="7ecd5-152">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ecd5-153">Header</span><span class="sxs-lookup"><span data-stu-id="7ecd5-153">Header</span></span><br/> | <dl> <span data-ttu-id="7ecd5-154"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ecd5-154"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="7ecd5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="7ecd5-155">DLL</span></span><br/>    | <dl> <span data-ttu-id="7ecd5-156"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ecd5-156"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ecd5-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ecd5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ecd5-158">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="7ecd5-158">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="7ecd5-159">**PST \_ promptinfo**</span><span class="sxs-lookup"><span data-stu-id="7ecd5-159">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
