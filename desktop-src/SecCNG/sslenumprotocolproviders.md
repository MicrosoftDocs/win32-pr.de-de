---
description: Gibt ein Array installierter SSL-Protokoll Anbieter (Secure Sockets Layer Protocol) zurück.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Sslenenprotocolproviders-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218505"
---
# <a name="sslenumprotocolproviders-function"></a><span data-ttu-id="5ed5e-103">Sslenenprotocolproviders-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ed5e-103">SslEnumProtocolProviders function</span></span>

<span data-ttu-id="5ed5e-104">Die **sslenenprotocolproviders** -Funktion gibt ein Array installierter SSL-Protokoll Anbieter ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-104">The **SslEnumProtocolProviders** function returns an array of installed [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed5e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ed5e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5ed5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ed5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed5e-107">*pdwprovidercount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5ed5e-107">*pdwProviderCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed5e-108">Ein Zeiger auf einen **DWORD** -Wert, der die Anzahl der zurückgegebenen Protokoll Anbieter empfängt.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-108">A pointer to a **DWORD** value to receive the number of protocol providers returned.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5e-109">*ppproviderlist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5ed5e-109">*ppProviderList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed5e-110">Ein Zeiger auf einen Puffer, der das Array von [**ncryptprovidername**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) -Strukturen empfängt.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-110">A pointer to a buffer that receives the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures.</span></span>

</dd> <dt>

<span data-ttu-id="5ed5e-111">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ed5e-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed5e-112">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-112">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed5e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ed5e-113">Return value</span></span>

<span data-ttu-id="5ed5e-114">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-114">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5ed5e-115">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-115">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5ed5e-116">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="5ed5e-116">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5ed5e-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5ed5e-117">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="5ed5e-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ed5e-118">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ed5e-119"><dt>**Ernte \_ Ungültige \_ Flags**</dt> <dt>0x80090009l</dt></span><span class="sxs-lookup"><span data-stu-id="5ed5e-119"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="5ed5e-120">Der *dwFlags* -Parameter ist nicht 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5ed5e-120">The *dwFlags* parameter is not zero.</span></span><br/>                              |
| <dl> <span data-ttu-id="5ed5e-121"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="5ed5e-121"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="5ed5e-122">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-122">Not enough memory is available to allocate necessary buffers.</span></span><br/>     |
| <dl> <span data-ttu-id="5ed5e-123"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="5ed5e-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="5ed5e-124">Der Parameter " *pdwprovidercount* " oder " *ppproviderlist* " ist **null**.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-124">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ed5e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ed5e-125">Remarks</span></span>

<span data-ttu-id="5ed5e-126">Wenn Sie die Verwendung des Arrays von [**ncryptprovidername**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) -Strukturen abgeschlossen haben, können Sie die [**sslfreebuffer**](sslfreebuffer.md) -Funktion aufrufen, um das Array freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5ed5e-126">When you have finished using the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures, call the [**SslFreeBuffer**](sslfreebuffer.md) function to free the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed5e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ed5e-127">Requirements</span></span>



| <span data-ttu-id="5ed5e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ed5e-128">Requirement</span></span> | <span data-ttu-id="5ed5e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5ed5e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed5e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ed5e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed5e-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ed5e-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5ed5e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ed5e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed5e-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ed5e-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5ed5e-134">Header</span><span class="sxs-lookup"><span data-stu-id="5ed5e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed5e-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ed5e-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5ed5e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5ed5e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed5e-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed5e-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

