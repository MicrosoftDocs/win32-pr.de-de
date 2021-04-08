---
description: Gibt ein Handle für den Handshake-Hash zurück.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Sslhashhandshake-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960469"
---
# <a name="sslhashhandshake-function"></a><span data-ttu-id="e24c3-103">Sslhashhandshake-Funktion</span><span class="sxs-lookup"><span data-stu-id="e24c3-103">SslHashHandshake function</span></span>

<span data-ttu-id="e24c3-104">Die **sslhashhandshake** -Funktion gibt ein Handle für den Handshake-Hash zurück.</span><span class="sxs-lookup"><span data-stu-id="e24c3-104">The **SslHashHandshake** function returns a handle to the handshake hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e24c3-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e24c3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e24c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e24c3-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e24c3-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24c3-108">Das Handle für die Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="e24c3-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="e24c3-109">*hhandshakehash* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e24c3-109">*hHandshakeHash* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e24c3-110">Das Handle für das Hash Objekt.</span><span class="sxs-lookup"><span data-stu-id="e24c3-110">The handle to the hash object.</span></span>

</dd> <dt>

<span data-ttu-id="e24c3-111">*pbinput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e24c3-111">*pbInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e24c3-112">Die Adresse eines Puffers, der die Daten enthält, für die ein Hashwert erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e24c3-112">The address of a buffer that contains the data to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="e24c3-113">*cbinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e24c3-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24c3-114">Die Größe des *pbinput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e24c3-114">The size, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e24c3-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e24c3-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24c3-116">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e24c3-116">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e24c3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e24c3-117">Return value</span></span>

<span data-ttu-id="e24c3-118">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e24c3-118">If the function succeeds, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e24c3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e24c3-119">Remarks</span></span>

<span data-ttu-id="e24c3-120">Die **sslhashhandshake** -Funktion ist eine von drei Funktionen, die verwendet werden, um einen Hash zu generieren, der während des SSL-Handshake verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e24c3-120">The **SslHashHandshake** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="e24c3-121">Die [**sslkreatehandshakehash**](sslcreatehandshakehash.md) -Funktion wird aufgerufen, um ein Hashhandle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e24c3-121">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="e24c3-122">Die **sslhashhandshake** -Funktion wird beliebig oft mit dem Hashhandle aufgerufen, um dem Hash Daten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e24c3-122">The **SslHashHandshake** function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="e24c3-123">Die [**sslcomputefinishedhash**](sslcomputefinishedhash.md) -Funktion wird mit dem Hashhandle aufgerufen, um den Digest der Hash Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e24c3-123">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24c3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e24c3-124">Requirements</span></span>



| <span data-ttu-id="e24c3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e24c3-125">Requirement</span></span> | <span data-ttu-id="e24c3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e24c3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e24c3-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e24c3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e24c3-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e24c3-128">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e24c3-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e24c3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e24c3-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e24c3-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e24c3-131">Header</span><span class="sxs-lookup"><span data-stu-id="e24c3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e24c3-132"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="e24c3-132"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e24c3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e24c3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e24c3-134"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e24c3-134"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

