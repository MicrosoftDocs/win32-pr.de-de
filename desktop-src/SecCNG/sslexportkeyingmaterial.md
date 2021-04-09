---
description: Exportiert das Schlüsselmaterial gemäß RFC 5705-Standard.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Sslexportkeyingmaterial-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760105"
---
# <a name="sslexportkeyingmaterial-function"></a><span data-ttu-id="f24a7-103">Sslexportkeyingmaterial-Funktion</span><span class="sxs-lookup"><span data-stu-id="f24a7-103">SslExportKeyingMaterial function</span></span>

<span data-ttu-id="f24a7-104">Exportiert das Schlüsselmaterial gemäß [RFC 5705-Standard](https://tools.ietf.org/html/rfc5705).</span><span class="sxs-lookup"><span data-stu-id="f24a7-104">Exports keying material per the [RFC 5705 standard](https://tools.ietf.org/html/rfc5705).</span></span> <span data-ttu-id="f24a7-105">Diese Funktion verwendet die Funktion "TLS Pseudo Zufalls", um einen Byte Puffer mit Schlüsselmaterial zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f24a7-105">This function uses the TLS pseudorandom function to produce a byte buffer of keying material.</span></span> <span data-ttu-id="f24a7-106">Es wird ein Verweis auf den geheimen Hauptschlüssel, die Mehrdeutigkeit der ASCII-Bezeichnung, Client-und Server Zufallswerte und optional die Anwendungskontext Daten benötigt.</span><span class="sxs-lookup"><span data-stu-id="f24a7-106">It takes a reference to the master secret, the disambiguating ASCII label, client and server random values, and optionally the application context data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f24a7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f24a7-107">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f24a7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f24a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f24a7-109">*hsslprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-109">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-110">Das Handle der TLS-Protokoll Anbieter Instanz.</span><span class="sxs-lookup"><span data-stu-id="f24a7-110">The handle of the TLS protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-111">*hmasterkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-111">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-112">Das Handle des Hauptschlüssel Objekts, das verwendet wird, um das Schlüsselmaterial zu erstellen, das von BR exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="f24a7-112">The handle of the master key object that will be used to create the keying material to br exported.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-113">*slabel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-113">*sLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-114">eine Zeichenfolge mit einer Zeichenfolge, die eine Zeichenfolge mit Zeichen</span><span class="sxs-lookup"><span data-stu-id="f24a7-114">a NUL-terminated ASCII label string.</span></span> <span data-ttu-id="f24a7-115">SChannel entfernt das abschließende NUL-Zeichen, bevor es an die Pseudo Zufalls-Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f24a7-115">Schannel will remove the terminating NUL character before passing it to the pseudorandom function.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-116">*pbrandoms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-116">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-117">Ein Zeiger auf einen Puffer, der eine Verkettung der *\_ zufälligen* Zufallswerte des *Clients \_* und des Servers der TLS-Verbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="f24a7-117">A pointer to a buffer that contains a concatenation of the *client\_random* and *server\_random* values of the TLS connection.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-118">*cbrandoms* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-118">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-119">Die Länge des *pbrandoms* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f24a7-119">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-120">*pbcontextvalue* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-120">*pbContextValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-121">Ein Zeiger auf einen Puffer, der den Anwendungskontext enthält.</span><span class="sxs-lookup"><span data-stu-id="f24a7-121">A pointer to a buffer that contains the application context.</span></span> <span data-ttu-id="f24a7-122">Wenn *pbcontextvalue* **null** ist, muss *cbcontextvalue* gleich NULL sein.</span><span class="sxs-lookup"><span data-stu-id="f24a7-122">If *pbContextValue* is **NULL**, *cbContextValue* must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-123">*cbcontextvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-123">*cbContextValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-124">Die Länge des *pbcontextvalue* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f24a7-124">The length, in bytes, of the *pbContextValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-125">*pboutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-125">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-126">Die Adresse eines Puffers, der das exportierte Schlüsselmaterial empfängt.</span><span class="sxs-lookup"><span data-stu-id="f24a7-126">The address of a buffer that receives the exported keying material.</span></span> <span data-ttu-id="f24a7-127">Der *cboutput* -Parameter enthält die Größe dieses Puffers.</span><span class="sxs-lookup"><span data-stu-id="f24a7-127">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="f24a7-128">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="f24a7-128">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-129">*cboutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-129">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-130">Die Länge des *pboutput* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f24a7-130">The length, in bytes, of the *pbOutput* buffer.</span></span> <span data-ttu-id="f24a7-131">Muss größer sein als Null.</span><span class="sxs-lookup"><span data-stu-id="f24a7-131">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="f24a7-132">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24a7-133">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f24a7-133">Not used.</span></span> <span data-ttu-id="f24a7-134">Muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f24a7-134">Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f24a7-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f24a7-135">Return value</span></span>

<span data-ttu-id="f24a7-136">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="f24a7-136">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="f24a7-137">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f24a7-137">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="f24a7-138">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="f24a7-138">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f24a7-139">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="f24a7-139">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="f24a7-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f24a7-140">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="f24a7-141"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="f24a7-141"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="f24a7-142">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f24a7-142">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f24a7-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f24a7-143">Requirements</span></span>



| <span data-ttu-id="f24a7-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f24a7-144">Requirement</span></span> | <span data-ttu-id="f24a7-145">Wert</span><span class="sxs-lookup"><span data-stu-id="f24a7-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f24a7-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f24a7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f24a7-147">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-147">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f24a7-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f24a7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f24a7-149">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f24a7-149">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f24a7-150">Header</span><span class="sxs-lookup"><span data-stu-id="f24a7-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="f24a7-151"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="f24a7-151"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="f24a7-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f24a7-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f24a7-153"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f24a7-153"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




