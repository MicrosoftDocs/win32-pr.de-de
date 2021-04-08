---
title: Session. Delete-Methode (WSManDisp. h)
description: Löscht die im Ressourcen-URI angegebene Ressource.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Delete-Methode Windows-Remoteverwaltung
- Delete-Methode Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, DELETE-Methode
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949609"
---
# <a name="sessiondelete-method"></a><span data-ttu-id="f2c39-106">Session. Delete-Methode</span><span class="sxs-lookup"><span data-stu-id="f2c39-106">Session.Delete method</span></span>

<span data-ttu-id="f2c39-107">Löscht die im Ressourcen-URI angegebene Ressource.</span><span class="sxs-lookup"><span data-stu-id="f2c39-107">Deletes the resource specified in the resource URI.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c39-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2c39-108">Syntax</span></span>


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f2c39-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2c39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2c39-110">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2c39-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c39-111">Der URI der zu löschenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="f2c39-111">The URI of the resource to be deleted.</span></span> <span data-ttu-id="f2c39-112">Sie können auch ein [**ResourceLocator**](resourcelocator.md) -Objekt verwenden, um die Ressource anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f2c39-112">You can also use a [**ResourceLocator**](resourcelocator.md) object to specify the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f2c39-113">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f2c39-113">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2c39-114">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f2c39-114">Reserved for future use.</span></span> <span data-ttu-id="f2c39-115">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f2c39-115">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2c39-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2c39-116">Return value</span></span>

<span data-ttu-id="f2c39-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f2c39-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2c39-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2c39-118">Remarks</span></span>

<span data-ttu-id="f2c39-119">Die folgende Syntax wird verwendet, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f2c39-119">The following syntax is used to call this method.</span></span>


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a><span data-ttu-id="f2c39-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2c39-120">Examples</span></span>

<span data-ttu-id="f2c39-121">Im folgenden VBScript-Codebeispiel werden die für den HTTP-Transport konfigurierten Listener gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f2c39-121">The following VBScript code example deletes the listeners configured for HTTP transport.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a><span data-ttu-id="f2c39-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2c39-122">Requirements</span></span>



| <span data-ttu-id="f2c39-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2c39-123">Requirement</span></span> | <span data-ttu-id="f2c39-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f2c39-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c39-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2c39-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f2c39-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2c39-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f2c39-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2c39-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f2c39-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2c39-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f2c39-129">Header</span><span class="sxs-lookup"><span data-stu-id="f2c39-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2c39-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2c39-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2c39-131">IDL</span><span class="sxs-lookup"><span data-stu-id="f2c39-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2c39-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2c39-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f2c39-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2c39-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2c39-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2c39-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2c39-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f2c39-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2c39-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2c39-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2c39-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2c39-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c39-138">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="f2c39-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





