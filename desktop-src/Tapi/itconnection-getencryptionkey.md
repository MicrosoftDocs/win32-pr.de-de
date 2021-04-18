---
description: Die getencryptionkey-Methode ruft den Verschlüsselungsschlüssel ab.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'Itconnection:: getencryptionkey-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359293"
---
# <a name="itconnectiongetencryptionkey-method"></a><span data-ttu-id="a33f5-103">Itconnection:: getencryptionkey-Methode</span><span class="sxs-lookup"><span data-stu-id="a33f5-103">ITConnection::GetEncryptionKey method</span></span>

<span data-ttu-id="a33f5-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a33f5-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a33f5-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="a33f5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a33f5-106">Die **getencryptionkey** -Methode ruft den Verschlüsselungsschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="a33f5-106">The **GetEncryptionKey** method gets the encryption key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a33f5-107">Syntax</span></span>


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="a33f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a33f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33f5-109">*ppkeytype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a33f5-109">*ppKeyType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f5-110">Zeiger auf einen **BSTR** -Wert, der den Typ des Verschlüsselungsschlüssels enthält.</span><span class="sxs-lookup"><span data-stu-id="a33f5-110">Pointer to a **BSTR** containing the type of encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="a33f5-111">*pfvalidkeydata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a33f5-111">*pfValidKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f5-112">Gibt die Gültigkeit der Verschlüsselungsschlüssel Daten an.</span><span class="sxs-lookup"><span data-stu-id="a33f5-112">Indicates validity of encryption key data.</span></span>

</dd> <dt>

<span data-ttu-id="a33f5-113">*ppkeydata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a33f5-113">*ppKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a33f5-114">Zeiger auf einen **BSTR** -Wert, der die Verschlüsselungsschlüssel Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="a33f5-114">Pointer to a **BSTR** containing the encryption key data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33f5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a33f5-115">Return value</span></span>

<span data-ttu-id="a33f5-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a33f5-116">This method can return one of these values.</span></span>



| <span data-ttu-id="a33f5-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a33f5-117">Return code</span></span>                                                                                   | <span data-ttu-id="a33f5-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a33f5-118">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a33f5-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a33f5-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a33f5-120">Method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="a33f5-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a33f5-122">Der *ppkeytype-, pfvalidkeydata* -oder *ppkeydata* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a33f5-122">The *ppKeyType, pfValidKeyData,* or *ppKeyData* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="a33f5-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a33f5-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a33f5-124">Insufficient memory exists to perform the operation.</span></span><br/>                              |
| <dl> <span data-ttu-id="a33f5-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a33f5-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a33f5-126">Unspecified error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a33f5-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a33f5-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a33f5-128">This method is not yet implemented.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="a33f5-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a33f5-129">Remarks</span></span>

<span data-ttu-id="a33f5-130">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für die Parameter *ppkeytype* und *ppkeydata* zugewiesenen Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="a33f5-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppKeyType* and *ppKeyData* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33f5-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a33f5-131">Requirements</span></span>



| <span data-ttu-id="a33f5-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a33f5-132">Requirement</span></span> | <span data-ttu-id="a33f5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a33f5-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a33f5-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="a33f5-134">TAPI version</span></span><br/> | <span data-ttu-id="a33f5-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a33f5-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a33f5-136">Header</span><span class="sxs-lookup"><span data-stu-id="a33f5-136">Header</span></span><br/>       | <dl> <span data-ttu-id="a33f5-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a33f5-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a33f5-138">Library</span></span><br/>      | <dl> <span data-ttu-id="a33f5-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a33f5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a33f5-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="a33f5-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a33f5-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33f5-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a33f5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33f5-143">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="a33f5-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

