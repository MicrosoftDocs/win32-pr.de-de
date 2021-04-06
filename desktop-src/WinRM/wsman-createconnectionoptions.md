---
title: WSMAN. kreateconnectionoptions-Methode (WSManDisp. h)
description: Erstellt ein ConnectionOptions-Objekt, das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Sitzung verwendet werden.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Windows-Remoteverwaltung der Methode "kreateconnectionoptions"
- Methode "kreateconnectionoptions" Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, Methode "kreateconnectionoptions"
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858764"
---
# <a name="wsmancreateconnectionoptions-method"></a><span data-ttu-id="39732-106">WSMAN. kreateconnectionoptions-Methode</span><span class="sxs-lookup"><span data-stu-id="39732-106">WSMan.CreateConnectionOptions method</span></span>

<span data-ttu-id="39732-107">Erstellt ein [**ConnectionOptions**](connectionoptions.md) -Objekt, das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39732-107">Creates a [**ConnectionOptions**](connectionoptions.md) object that specifies the user name and password used when creating a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="39732-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="39732-108">Syntax</span></span>


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a><span data-ttu-id="39732-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="39732-109">Parameters</span></span>

<span data-ttu-id="39732-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="39732-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39732-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39732-111">Return value</span></span>

<span data-ttu-id="39732-112">Ein [**ConnectionOptions**](connectionoptions.md) -Objekt, mit dem ein Benutzername und ein Kennwort-Paar angegeben werden, mit dem ein Benutzer für die Authentifizierung identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="39732-112">A [**ConnectionOptions**](connectionoptions.md) object used to specify a user name and password pair that is used to identify a user for authentication.</span></span>

## <a name="remarks"></a><span data-ttu-id="39732-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39732-113">Remarks</span></span>

<span data-ttu-id="39732-114">Die folgende Syntax wird verwendet, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="39732-114">The following syntax is used to call this method.</span></span>


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a><span data-ttu-id="39732-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39732-115">Requirements</span></span>



| <span data-ttu-id="39732-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39732-116">Requirement</span></span> | <span data-ttu-id="39732-117">Wert</span><span class="sxs-lookup"><span data-stu-id="39732-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39732-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39732-118">Minimum supported client</span></span><br/> | <span data-ttu-id="39732-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39732-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="39732-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39732-120">Minimum supported server</span></span><br/> | <span data-ttu-id="39732-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39732-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="39732-122">Header</span><span class="sxs-lookup"><span data-stu-id="39732-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="39732-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="39732-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="39732-124">IDL</span><span class="sxs-lookup"><span data-stu-id="39732-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39732-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39732-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="39732-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39732-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="39732-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="39732-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="39732-128">DLL</span><span class="sxs-lookup"><span data-stu-id="39732-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39732-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39732-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="39732-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39732-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39732-131">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="39732-131">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="39732-132">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="39732-132">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





