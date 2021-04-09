---
description: Entschlüsselt ein einzelnes Secure Sockets Layer Protocol (SSL)-Paket.
ms.assetid: 22a7dd2b-d023-47b9-8f76-1c17c2dd6466
title: Ssldecryptpacket-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cd568596b7e780242c0ff8d9c522a9e1758c60b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959429"
---
# <a name="ssldecryptpacket-function"></a><span data-ttu-id="57c33-103">Ssldecryptpacket-Funktion</span><span class="sxs-lookup"><span data-stu-id="57c33-103">SslDecryptPacket function</span></span>

<span data-ttu-id="57c33-104">die **ssldecryptpacket** -Funktion entschlüsselt ein einzelnes [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL)-Paket.</span><span class="sxs-lookup"><span data-stu-id="57c33-104">the **SslDecryptPacket** function decrypts a single [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="57c33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57c33-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="57c33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57c33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57c33-107">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57c33-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-108">Das Handle der SSL-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="57c33-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="57c33-109">*HKEY* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="57c33-109">*hKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-110">Das Handle für den Schlüssel, der zum Entschlüsseln des Pakets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57c33-110">The handle to the key that is used to decrypt the packet.</span></span>

</dd> <dt>

<span data-ttu-id="57c33-111">*pbinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57c33-111">*pbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-112">Ein Zeiger auf den Puffer, der das Paket enthält, das entschlüsselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="57c33-112">A pointer to the buffer that contains the packet to be decrypted.</span></span>

</dd> <dt>

<span data-ttu-id="57c33-113">*cbinput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57c33-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-114">Die Länge des *pbinput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="57c33-114">The length, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="57c33-115">*pboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57c33-115">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-116">Ein Zeiger auf einen Puffer, der das entschlüsselte Paket enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="57c33-116">A pointer to a buffer to contain the decrypted packet.</span></span>

</dd> <dt>

<span data-ttu-id="57c33-117">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57c33-117">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-118">Die Länge (Bytes) des *pboutput* -Puffers.</span><span class="sxs-lookup"><span data-stu-id="57c33-118">The length, bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="57c33-119">*pcbresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57c33-119">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-120">Die Anzahl der in den *pboutput* -Puffer geschriebenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="57c33-120">The number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="57c33-121">*Sequencennummer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57c33-121">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-122">Die Sequenznummer, die diesem Paket entspricht.</span><span class="sxs-lookup"><span data-stu-id="57c33-122">The sequence number that corresponds to this packet.</span></span>

</dd> <dt>

<span data-ttu-id="57c33-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57c33-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57c33-124">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="57c33-124">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57c33-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57c33-125">Return value</span></span>

<span data-ttu-id="57c33-126">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="57c33-126">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="57c33-127">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="57c33-127">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="57c33-128">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="57c33-128">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="57c33-129">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="57c33-129">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="57c33-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="57c33-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="57c33-131"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="57c33-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="57c33-132">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="57c33-132">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57c33-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57c33-133">Remarks</span></span>

<span data-ttu-id="57c33-134">Die Länge des Pakets kann NULL sein, z. b. Wenn eine "hellorequest"-Meldung entschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="57c33-134">The length of the packet can be zero, such as when a "HelloRequest" message is decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="57c33-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57c33-135">Requirements</span></span>



| <span data-ttu-id="57c33-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57c33-136">Requirement</span></span> | <span data-ttu-id="57c33-137">Wert</span><span class="sxs-lookup"><span data-stu-id="57c33-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="57c33-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57c33-138">Minimum supported client</span></span><br/> | <span data-ttu-id="57c33-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57c33-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="57c33-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57c33-140">Minimum supported server</span></span><br/> | <span data-ttu-id="57c33-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57c33-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="57c33-142">Header</span><span class="sxs-lookup"><span data-stu-id="57c33-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="57c33-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="57c33-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="57c33-144">DLL</span><span class="sxs-lookup"><span data-stu-id="57c33-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57c33-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57c33-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

