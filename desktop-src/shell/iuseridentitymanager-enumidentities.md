---
description: Iuseridentitymanager::-Eigenschaften werden nicht unterstützt und können in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'Iuseridentitymanager:: sumidentities-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127833"
---
# <a name="iuseridentitymanagerenumidentities-method"></a><span data-ttu-id="74e91-104">Iuseridentitymanager:: sumidentities-Methode</span><span class="sxs-lookup"><span data-stu-id="74e91-104">IUserIdentityManager::EnumIdentities method</span></span>

<span data-ttu-id="74e91-105">\[**Iuseridentitymanager::-Eigenschaften** werden nicht unterstützt und können in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="74e91-105">\[**IUserIdentityManager::EnumIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="74e91-106">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="74e91-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="74e91-107">Ruft ein [**ienumuseridentity**](ienumuseridentity.md) -Objekt ab, das verwendet werden kann, um die Benutzer Identitäten aufzulisten, die auf dem System vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="74e91-107">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="74e91-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="74e91-108">Syntax</span></span>


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a><span data-ttu-id="74e91-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="74e91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74e91-110">" *ppumuser* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="74e91-110">*ppEnumUser* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74e91-111">Typ: **[ **iumumuseridentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="74e91-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="74e91-112">Die Adresse des Zeigers auf das neue identitätsenumerationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="74e91-112">The address of the pointer to the new identity enumeration object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74e91-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74e91-113">Return value</span></span>

<span data-ttu-id="74e91-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="74e91-114">Type: **HRESULT**</span></span>

<span data-ttu-id="74e91-115">Das Ergebnis des Abruf Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="74e91-115">The result of the retrieval operation.</span></span> <span data-ttu-id="74e91-116">Bei erfolgreicher Ausführung wird S OK zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="74e91-116">If successful, it returns S\_OK.</span></span> <span data-ttu-id="74e91-117">Wenn das Enumerationsobjekt nicht erstellt werden konnte, wird E \_ outo-Memory zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="74e91-117">If the enumeration object could not be created, it returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="74e91-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74e91-118">Remarks</span></span>

<span data-ttu-id="74e91-119">Diese Methode ist nützlich für die iterierung der Liste der Identitäten im System.</span><span class="sxs-lookup"><span data-stu-id="74e91-119">This method is useful for iteration over the list of identities on the system.</span></span> <span data-ttu-id="74e91-120">Um eine einzelne Identität über das Cookie abzurufen, ohne auf die Liste zuzugreifen, rufen Sie [**iuseridentitymanager:: getidentitybycookie**](iuseridentitymanager-getidentitybycookie.md)auf.</span><span class="sxs-lookup"><span data-stu-id="74e91-120">To retrieve a single identity by its cookie without accessing the list, call [**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74e91-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="74e91-121">Requirements</span></span>



| <span data-ttu-id="74e91-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74e91-122">Requirement</span></span> | <span data-ttu-id="74e91-123">Wert</span><span class="sxs-lookup"><span data-stu-id="74e91-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74e91-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74e91-124">Minimum supported client</span></span><br/> | <span data-ttu-id="74e91-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74e91-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="74e91-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74e91-126">Minimum supported server</span></span><br/> | <span data-ttu-id="74e91-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74e91-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="74e91-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="74e91-128">End of client support</span></span><br/>    | <span data-ttu-id="74e91-129">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="74e91-129">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="74e91-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="74e91-130">End of server support</span></span><br/>    | <span data-ttu-id="74e91-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74e91-131">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="74e91-132">Header</span><span class="sxs-lookup"><span data-stu-id="74e91-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="74e91-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="74e91-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="74e91-134">IDL</span><span class="sxs-lookup"><span data-stu-id="74e91-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="74e91-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="74e91-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="74e91-136">DLL</span><span class="sxs-lookup"><span data-stu-id="74e91-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74e91-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74e91-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74e91-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="74e91-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e91-139">**Iuseridentitymanager**</span><span class="sxs-lookup"><span data-stu-id="74e91-139">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="74e91-140">**Iumumuseridentity**</span><span class="sxs-lookup"><span data-stu-id="74e91-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="74e91-141">**Iuseridentitymanager:: getidentitybycookie**</span><span class="sxs-lookup"><span data-stu-id="74e91-141">**IUserIdentityManager::GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




