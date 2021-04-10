---
description: Wird verwendet, um Arbeitsspeicher freizugeben, der von einer der Funktionen des Secure Sockets Layer-Protokolls (SSL) zugewiesen wurde.
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Sslfrebuffer-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050562"
---
# <a name="sslfreebuffer-function"></a><span data-ttu-id="aa62f-103">Sslfrebuffer-Funktion</span><span class="sxs-lookup"><span data-stu-id="aa62f-103">SslFreeBuffer function</span></span>

<span data-ttu-id="aa62f-104">Die **sslfreebuffer** -Funktion wird verwendet, um Arbeitsspeicher freizugeben, der von einer der Funktionen des [*Secure Sockets Layer-Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL) zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="aa62f-104">The **SslFreeBuffer** function is used to free memory that was allocated by one of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa62f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa62f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a><span data-ttu-id="aa62f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa62f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa62f-107">*pvinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa62f-107">*pvInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa62f-108">Ein Zeiger auf den Speicherpuffer, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa62f-108">A pointer to the memory buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa62f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa62f-109">Return value</span></span>

<span data-ttu-id="aa62f-110">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="aa62f-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="aa62f-111">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa62f-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="aa62f-112">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="aa62f-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="aa62f-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="aa62f-113">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="aa62f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa62f-114">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa62f-115"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="aa62f-115"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="aa62f-116">Der Parameter " *pdwprovidercount* " oder " *ppproviderlist* " ist **null**.</span><span class="sxs-lookup"><span data-stu-id="aa62f-116">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aa62f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa62f-117">Requirements</span></span>



| <span data-ttu-id="aa62f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa62f-118">Requirement</span></span> | <span data-ttu-id="aa62f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="aa62f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa62f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa62f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa62f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa62f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aa62f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa62f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa62f-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa62f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aa62f-124">Header</span><span class="sxs-lookup"><span data-stu-id="aa62f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa62f-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa62f-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="aa62f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="aa62f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa62f-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa62f-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

