---
description: Berechnet den Schlüssel Block, der vom EAP (Extensible Authentication Protocol) verwendet wird.
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Sslcomputeeapkeyblock-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367877"
---
# <a name="sslcomputeeapkeyblock-function"></a><span data-ttu-id="ebcc6-103">Sslcomputeeapkeyblock-Funktion</span><span class="sxs-lookup"><span data-stu-id="ebcc6-103">SslComputeEapKeyBlock function</span></span>

<span data-ttu-id="ebcc6-104">Die **sslcomputeeapkeyblock** -Funktion berechnet den Schlüssel Block, der vom Extensible Authentication Protocol (EAP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-104">The **SslComputeEapKeyBlock** function computes the key block used by the Extensible Authentication Protocol (EAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebcc6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebcc6-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ebcc6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebcc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebcc6-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcc6-108">Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="ebcc6-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ebcc6-109">*hmasterkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcc6-110">Das Handle des [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) Objekts.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="ebcc6-111">*pbrandoms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-111">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcc6-112">Ein Zeiger auf einen Puffer, der eine Verkettung der zufälligen Zufallswerte des Clients \_ und \_ des Servers der SSL-Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-112">A pointer to a buffer that contains a concatenation of the client\_random and server\_random values of the SSL session.</span></span>

</dd> <dt>

<span data-ttu-id="ebcc6-113">*cbrandoms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-113">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcc6-114">Die Länge des *pbrandoms* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-114">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ebcc6-115">*pboutput* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-115">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcc6-116">Die Adresse eines Puffers, der das Schlüsselblob empfängt.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-116">The address of a buffer that receives the key BLOB.</span></span> <span data-ttu-id="ebcc6-117">Der *cboutput* -Parameter enthält die Größe dieses Puffers.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-117">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="ebcc6-118">Wenn dieser Parameter **null** ist, fügt diese Funktion die erforderliche Größe (in Bytes) in das **DWORD** ein, auf das durch den *pcbresult* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-118">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ebcc6-119">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-119">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcc6-120">Die Länge des *pboutput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-120">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ebcc6-121">*pcbresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-121">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcc6-122">Ein Zeiger auf einen **DWORD** -Wert, der die Länge des in den *pboutput* -Puffer geschriebenen Hashs in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-122">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ebcc6-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebcc6-124">Legen Sie auf **NCrypt \_ SSL \_ Server \_ Flag** fest, um anzugeben, dass es sich um einen Server-Befehl handelt.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-124">Set to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebcc6-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ebcc6-125">Return value</span></span>

<span data-ttu-id="ebcc6-126">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ebcc6-127">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-127">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="ebcc6-128">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ebcc6-128">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="ebcc6-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebcc6-129">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ebcc6-130"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="ebcc6-130"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="ebcc6-131">Eines der angegebenen Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ebcc6-131">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ebcc6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebcc6-132">Requirements</span></span>



| <span data-ttu-id="ebcc6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebcc6-133">Requirement</span></span> | <span data-ttu-id="ebcc6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ebcc6-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebcc6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebcc6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ebcc6-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-136">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ebcc6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebcc6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ebcc6-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ebcc6-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ebcc6-139">Header</span><span class="sxs-lookup"><span data-stu-id="ebcc6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebcc6-140"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebcc6-140"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ebcc6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ebcc6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebcc6-142"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebcc6-142"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

