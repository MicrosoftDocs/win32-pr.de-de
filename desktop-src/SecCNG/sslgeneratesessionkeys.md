---
description: Generiert einen Satz von SSL-Sitzungs Schlüsseln (Secure Sockets Layer Protocol).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Sslgeneratesessionkeys-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366337"
---
# <a name="sslgeneratesessionkeys-function"></a><span data-ttu-id="e2da8-103">Sslgeneratesessionkeys-Funktion</span><span class="sxs-lookup"><span data-stu-id="e2da8-103">SslGenerateSessionKeys function</span></span>

<span data-ttu-id="e2da8-104">Die **sslgeneratesessionkeys** -Funktion generiert einen Satz von SSL-Sitzungs Schlüsseln ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="e2da8-104">The **SslGenerateSessionKeys** function generates a set of [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) session keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2da8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2da8-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e2da8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2da8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2da8-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2da8-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2da8-108">Das Handle für die SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="e2da8-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="e2da8-109">*hmasterkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2da8-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2da8-110">Das Handle für das [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2da8-110">The handle to the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="e2da8-111">*Phread Key* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e2da8-111">*phReadKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2da8-112">Ein Zeiger auf das zurückgegebene Lese Schlüssel handle.</span><span class="sxs-lookup"><span data-stu-id="e2da8-112">A pointer to the returned read key handle.</span></span>

</dd> <dt>

<span data-ttu-id="e2da8-113">*phschreitekey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e2da8-113">*phWriteKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2da8-114">Ein Zeiger auf das zurückgegebene Schreib Schlüssel handle.</span><span class="sxs-lookup"><span data-stu-id="e2da8-114">A pointer to the returned write key handle.</span></span>

</dd> <dt>

<span data-ttu-id="e2da8-115">*pparameterlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2da8-115">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2da8-116">Ein Zeiger auf ein Array von [**ncryptbuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) -Puffern, die Informationen enthalten, die als Teil des Schlüsselaustausch Vorgangs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2da8-116">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="e2da8-117">Der genaue Satz Puffer ist abhängig vom verwendeten Protokoll und der Verschlüsselungs Sammlung.</span><span class="sxs-lookup"><span data-stu-id="e2da8-117">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="e2da8-118">Die Liste enthält mindestens Puffer, die den vom Client und vom Server bereitgestellten Zufallswert enthalten.</span><span class="sxs-lookup"><span data-stu-id="e2da8-118">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="e2da8-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2da8-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2da8-120">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e2da8-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2da8-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2da8-121">Return value</span></span>

<span data-ttu-id="e2da8-122">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e2da8-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="e2da8-123">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2da8-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="e2da8-124">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="e2da8-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="e2da8-125">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="e2da8-125">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="e2da8-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2da8-126">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2da8-127"><dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt></span><span class="sxs-lookup"><span data-stu-id="e2da8-127"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="e2da8-128">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e2da8-128">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="e2da8-129"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="e2da8-129"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="e2da8-130">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e2da8-130">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="e2da8-131"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="e2da8-131"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="e2da8-132">Der Parameter " *Phread Key* " oder " *phschreitekey* " ist NULL.</span><span class="sxs-lookup"><span data-stu-id="e2da8-132">The *phReadKey* or *phWriteKey* parameter is null.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="e2da8-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2da8-133">Requirements</span></span>



| <span data-ttu-id="e2da8-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2da8-134">Requirement</span></span> | <span data-ttu-id="e2da8-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e2da8-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2da8-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2da8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e2da8-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2da8-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2da8-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2da8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e2da8-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2da8-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e2da8-140">Header</span><span class="sxs-lookup"><span data-stu-id="e2da8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2da8-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2da8-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e2da8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e2da8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2da8-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2da8-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

