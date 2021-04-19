---
description: Die rkeyopenkeyservice-Funktion wird nicht unterstützt.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Rkeyopenkeyservice-Funktion (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348729"
---
# <a name="rkeyopenkeyservice-function"></a><span data-ttu-id="e55ff-103">Rkeyopenkeyservice-Funktion</span><span class="sxs-lookup"><span data-stu-id="e55ff-103">RKeyOpenKeyService function</span></span>

<span data-ttu-id="e55ff-104">Die **rkeyopenkeyservice** -Funktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e55ff-104">The **RKeyOpenKeyService** function is not supported.</span></span>

<span data-ttu-id="e55ff-105">**Windows Server 2003:** Die **rkeyopenkeyservice** -Funktion stellt eine Verbindung mit einem Remote Computer her und öffnet ein Schlüsseldienst handle.</span><span class="sxs-lookup"><span data-stu-id="e55ff-105">**Windows Server 2003:** The **RKeyOpenKeyService** function establishes a connection to a remote computer and opens a key service handle.</span></span> <span data-ttu-id="e55ff-106">Das Schlüsseldienst Handle kann anschließend von der Funktion [**rkeypfxinstall**](rkeypfxinstall.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e55ff-106">The key service handle can subsequently be used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span> <span data-ttu-id="e55ff-107">Beachten Sie, dass sich dieses Verhalten in Windows Server 2003 mit Service Pack 1 (SP1) geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e55ff-107">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="e55ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e55ff-108">Syntax</span></span>


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a><span data-ttu-id="e55ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e55ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e55ff-110">*pszmachinename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e55ff-110">*pszMachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e55ff-111">Langer Zeiger auf eine auf NULL endende Zeichenfolge, die den Computer darstellt, auf dem das Schlüsseldienst Handle geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e55ff-111">Long pointer to a null-terminated string that represents the computer where the key service handle will be opened.</span></span>

</dd> <dt>

<span data-ttu-id="e55ff-112">*Besitztyp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e55ff-112">*OwnerType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e55ff-113">[**Keysvc \_ Der Typwert**](keysvc-type.md) , der den Schlüsseltyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="e55ff-113">[**KEYSVC\_TYPE**](keysvc-type.md) value that represents the key type.</span></span> <span data-ttu-id="e55ff-114">Der einzige unterstützte Wert ist " **keysvcmachine**".</span><span class="sxs-lookup"><span data-stu-id="e55ff-114">The only supported value is **KeySvcMachine**.</span></span>

</dd> <dt>

<span data-ttu-id="e55ff-115">*pwszownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e55ff-115">*pwszOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e55ff-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e55ff-116">Reserved.</span></span> <span data-ttu-id="e55ff-117">Legen Sie diesen Wert auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="e55ff-117">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e55ff-118">*pauthentication* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e55ff-118">*pAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e55ff-119">Ein Zeiger auf ein **void** -, das die Authentifizierungs Einstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="e55ff-119">A pointer to a **void** that represents the authentication settings.</span></span> <span data-ttu-id="e55ff-120">Dieser Zeiger kann auf einen Wert von 0 (null) oder auf den folgenden Wert zeigen.</span><span class="sxs-lookup"><span data-stu-id="e55ff-120">This pointer can point to a value of zero or the following value.</span></span>



| <span data-ttu-id="e55ff-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e55ff-121">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="e55ff-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e55ff-122">Meaning</span></span>                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <span data-ttu-id="e55ff-123"><dt>**Rkeysvc \_ \_ \_ nur sichere Verbindung herstellen**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="e55ff-123"><dt>**RKEYSVC\_CONNECT\_SECURE\_ONLY**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="e55ff-124">Für den Client ist eine gegenseitige Authentifizierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e55ff-124">The client requires mutual authentication.</span></span> <span data-ttu-id="e55ff-125">Wenn dieser Wert angegeben wird, tritt ein Fall Back auf NTLM auf.</span><span class="sxs-lookup"><span data-stu-id="e55ff-125">If this value is specified, fallback to NTLM will fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e55ff-126">*beibehalten* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e55ff-126">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e55ff-127">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="e55ff-127">Reserved.</span></span> <span data-ttu-id="e55ff-128">Legen Sie diesen Wert auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="e55ff-128">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e55ff-129">*phkeysvccli* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e55ff-129">*phKeySvcCli* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e55ff-130">Ein Zeiger auf ein [**keysvcc- \_ handle**](keysvcc-handle.md) , das das geöffnete Schlüsseldienst handle empfängt.</span><span class="sxs-lookup"><span data-stu-id="e55ff-130">A pointer to a [**KEYSVCC\_HANDLE**](keysvcc-handle.md) that receives the opened key service handle.</span></span> <span data-ttu-id="e55ff-131">Wenn Sie die Verwendung des Handles abgeschlossen haben, können Sie die Ressource freigeben, indem Sie die [**rkeyclosekeyservice**](rkeyclosekeyservice.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e55ff-131">When you have finished using the handle, free the resource by calling the [**RKeyCloseKeyService**](rkeyclosekeyservice.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e55ff-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e55ff-132">Return value</span></span>

<span data-ttu-id="e55ff-133">Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e55ff-133">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="e55ff-134">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein **ulong** -Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="e55ff-134">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e55ff-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e55ff-135">Requirements</span></span>



| <span data-ttu-id="e55ff-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e55ff-136">Requirement</span></span> | <span data-ttu-id="e55ff-137">Wert</span><span class="sxs-lookup"><span data-stu-id="e55ff-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e55ff-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e55ff-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e55ff-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e55ff-139">None supported</span></span><br/>                                                             |
| <span data-ttu-id="e55ff-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e55ff-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e55ff-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e55ff-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e55ff-142">Header</span><span class="sxs-lookup"><span data-stu-id="e55ff-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e55ff-143"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e55ff-143"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e55ff-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e55ff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e55ff-145">**Rkeyclosekeyservice**</span><span class="sxs-lookup"><span data-stu-id="e55ff-145">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="e55ff-146">**Rkeypfxinstall**</span><span class="sxs-lookup"><span data-stu-id="e55ff-146">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




