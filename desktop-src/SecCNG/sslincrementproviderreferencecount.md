---
description: Erhöht den Verweis Zähler auf eine Instanz des Secure Sockets Layer Protocol (SSL)-Anbieters.
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: Sslinkrementproviderreferencecount-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 862697035d978db082c303c6e1df6f2a444d8be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351142"
---
# <a name="sslincrementproviderreferencecount-function"></a><span data-ttu-id="c03b7-103">Sslinkrementproviderreferencecount-Funktion</span><span class="sxs-lookup"><span data-stu-id="c03b7-103">SslIncrementProviderReferenceCount function</span></span>

<span data-ttu-id="c03b7-104">Die **sslinkrementproviderreferencecount** -Funktion erhöht den Verweis Zähler auf eine Instanz des [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL)-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="c03b7-104">The **SslIncrementProviderReferenceCount** function increments the reference count to a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="c03b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c03b7-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="c03b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c03b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c03b7-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c03b7-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c03b7-108">Das Handle für die SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="c03b7-108">The handle to the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c03b7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c03b7-109">Return value</span></span>

<span data-ttu-id="c03b7-110">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="c03b7-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c03b7-111">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c03b7-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c03b7-112">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="c03b7-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c03b7-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="c03b7-113">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="c03b7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c03b7-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="c03b7-115"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="c03b7-115"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="c03b7-116">Das *hsslprovider* -Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c03b7-116">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c03b7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c03b7-117">Requirements</span></span>



| <span data-ttu-id="c03b7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c03b7-118">Requirement</span></span> | <span data-ttu-id="c03b7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c03b7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c03b7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c03b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c03b7-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c03b7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c03b7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c03b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c03b7-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c03b7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c03b7-124">Header</span><span class="sxs-lookup"><span data-stu-id="c03b7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c03b7-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c03b7-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c03b7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c03b7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c03b7-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c03b7-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

