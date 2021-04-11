---
description: Dekrementierungen der Verweise auf den SSL-Anbieter (Secure Sockets Layer Protocol).
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: Ssldecrementproviderreferencecount-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4d3fe072c02f22b713115dd5191b0b5e0cedbb37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959432"
---
# <a name="ssldecrementproviderreferencecount-function"></a><span data-ttu-id="37ac2-103">Ssldecrementproviderreferencecount-Funktion</span><span class="sxs-lookup"><span data-stu-id="37ac2-103">SslDecrementProviderReferenceCount function</span></span>

<span data-ttu-id="37ac2-104">Die **ssldecrementproviderreferencecount-Funktion dekrementierungen** die Verweise auf den SSL-Anbieter ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="37ac2-104">The **SslDecrementProviderReferenceCount** function decrements the references to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="37ac2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37ac2-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="37ac2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37ac2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37ac2-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37ac2-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37ac2-108">Das Handle der SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="37ac2-108">The handle of the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37ac2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="37ac2-109">Return value</span></span>

<span data-ttu-id="37ac2-110">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="37ac2-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="37ac2-111">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37ac2-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="37ac2-112">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="37ac2-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="37ac2-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="37ac2-113">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="37ac2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37ac2-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="37ac2-115"><dt> **\_ Ungültiger \_ handle**</dt> <dt>0xc0000008l</dt></span><span class="sxs-lookup"><span data-stu-id="37ac2-115"><dt>**STATUS\_INVALID\_HANDLE** </dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="37ac2-116">Das SSL-Anbieter Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="37ac2-116">The SSL provider handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="37ac2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37ac2-117">Requirements</span></span>



| <span data-ttu-id="37ac2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37ac2-118">Requirement</span></span> | <span data-ttu-id="37ac2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="37ac2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="37ac2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37ac2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="37ac2-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37ac2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="37ac2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37ac2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="37ac2-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37ac2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="37ac2-124">Header</span><span class="sxs-lookup"><span data-stu-id="37ac2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="37ac2-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="37ac2-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="37ac2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="37ac2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37ac2-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37ac2-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

