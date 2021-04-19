---
description: Öffnet ein Element für mehrere Zugriffe.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'Ipstore:: OpenItem-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353798"
---
# <a name="ipstoreopenitem-method"></a><span data-ttu-id="db776-103">Ipstore:: OpenItem-Methode</span><span class="sxs-lookup"><span data-stu-id="db776-103">IPStore::OpenItem method</span></span>

<span data-ttu-id="db776-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db776-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="db776-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db776-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="db776-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="db776-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="db776-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="db776-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="db776-108">Öffnet ein Element für mehrere Zugriffe.</span><span class="sxs-lookup"><span data-stu-id="db776-108">Opens an item for multiple accesses.</span></span>

## <a name="syntax"></a><span data-ttu-id="db776-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="db776-109">Syntax</span></span>


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="db776-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="db776-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db776-111">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db776-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db776-112">Gibt an, ob der Typ auf dem Computer lokal ist oder nur dem erstellerstellerbenutzer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="db776-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="db776-113">Wert</span><span class="sxs-lookup"><span data-stu-id="db776-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="db776-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="db776-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="db776-115"><dt>**PST \_ Schlüssel \_ aktueller \_ Benutzer**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="db776-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="db776-116">Der Speicher wird im Abschnitt Aktueller Benutzer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="db776-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="db776-117"><dt>**PST \_ Key \_ local \_ Machine**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="db776-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="db776-118">Der Speicher wird im Abschnitt lokaler Computer der Registrierung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="db776-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="db776-119">*pitemtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db776-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db776-120">Ein Zeiger auf eine GUID, die den Datentyp des zu öffnenden Elements identifiziert.</span><span class="sxs-lookup"><span data-stu-id="db776-120">A pointer to a GUID that identifies the data type of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="db776-121">*pitemsubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db776-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db776-122">Ein Zeiger auf eine GUID, die den zu öffnenden Element Untertyp angibt.</span><span class="sxs-lookup"><span data-stu-id="db776-122">A pointer to a GUID that indicates the item subtype to open.</span></span>

</dd> <dt>

<span data-ttu-id="db776-123">" *szitemname* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="db776-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db776-124">Eine Zeichenfolge, die den Namen des zu öffnenden Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="db776-124">A string that contains the name of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="db776-125">*Modeflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db776-125">*ModeFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db776-126">Beschreibt die Zugriffs Modi, auf die sich ein angegebener Satz von Zugriffs Klauseln bezieht.</span><span class="sxs-lookup"><span data-stu-id="db776-126">Describes the access modes to which a specified set of access clauses pertains.</span></span> <span data-ttu-id="db776-127">Weitere Informationen finden Sie unter [**pstore-Typen**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="db776-127">For more information, see [**PStore Types**](pstore-types.md).</span></span>



| <span data-ttu-id="db776-128">Wert</span><span class="sxs-lookup"><span data-stu-id="db776-128">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="db776-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="db776-129">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="db776-130"><dt>**PST \_ Lesen**</dt> von <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="db776-130"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="db776-131">Lese Zugriffsmodus.</span><span class="sxs-lookup"><span data-stu-id="db776-131">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="db776-132"><dt>**PST \_ Schreiben**</dt> von <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="db776-132"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="db776-133">Schreibzugriffs Modus.</span><span class="sxs-lookup"><span data-stu-id="db776-133">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="db776-134">*pproomptinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db776-134">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db776-135">Ein Zeiger auf eine [**PST- \_ promptinfo**](pst-promptinfo.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="db776-135">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="db776-136">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db776-136">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db776-137">Reserviert: muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="db776-137">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db776-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db776-138">Return value</span></span>

<span data-ttu-id="db776-139">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="db776-139">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="db776-140">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="db776-140">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="db776-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db776-141">Remarks</span></span>

<span data-ttu-id="db776-142">Wenn Sie ein Element in der geschützten Speicher Datenbank mithilfe von **OpenItem** öffnen, muss es schließlich mithilfe von [**ipstore:: closeitem**](ipstore-closeitem.md) geschlossen werden, um einen Speicherplatz zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="db776-142">Using **OpenItem** to open an item in the protected storage database requires that it eventually be closed using [**IPStore::CloseItem**](ipstore-closeitem.md) to prevent a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="db776-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db776-143">Requirements</span></span>



| <span data-ttu-id="db776-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db776-144">Requirement</span></span> | <span data-ttu-id="db776-145">Wert</span><span class="sxs-lookup"><span data-stu-id="db776-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db776-146">Header</span><span class="sxs-lookup"><span data-stu-id="db776-146">Header</span></span><br/> | <dl> <span data-ttu-id="db776-147"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="db776-147"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="db776-148">DLL</span><span class="sxs-lookup"><span data-stu-id="db776-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="db776-149"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db776-149"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db776-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db776-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db776-151">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="db776-151">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="db776-152">**PST \_ promptinfo**</span><span class="sxs-lookup"><span data-stu-id="db776-152">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
