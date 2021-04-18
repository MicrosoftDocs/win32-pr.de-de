---
description: Die SetEncryptionKey-Methode legt den Verschlüsselungsschlüssel fest, der zum Entschlüsseln der Sitzung erforderlich ist, oder einen Indikator für einen Mechanismus, um einen verwendbaren Schlüssel auf externe Weise zu erhalten.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'Itconnection:: btencryptionkey-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357614"
---
# <a name="itconnectionsetencryptionkey-method"></a><span data-ttu-id="5f3a3-103">Itconnection:: abtencryptionkey-Methode</span><span class="sxs-lookup"><span data-stu-id="5f3a3-103">ITConnection::SetEncryptionKey method</span></span>

<span data-ttu-id="5f3a3-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5f3a3-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="5f3a3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5f3a3-106">Die **SetEncryptionKey** -Methode legt den Verschlüsselungsschlüssel fest, der zum Entschlüsseln der Sitzung erforderlich ist, oder einen Indikator für einen Mechanismus, um einen verwendbaren Schlüssel auf externe Weise zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-106">The **SetEncryptionKey** method sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f3a3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f3a3-107">Syntax</span></span>


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="5f3a3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f3a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f3a3-109">*pkeytype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f3a3-109">*pKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f3a3-110">Zeiger auf ein **BSTR** , das den Verschlüsselungs Schlüsseltyp enthält.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-110">Pointer to a **BSTR** containing the encryption key type.</span></span>

</dd> <dt>

<span data-ttu-id="5f3a3-111">*ppkeydata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f3a3-111">*ppKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f3a3-112">Zeiger auf ein **BSTR** , das Informationen zum Verschlüsselungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-112">Pointer to a **BSTR** containing encryption key information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f3a3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f3a3-113">Return value</span></span>

<span data-ttu-id="5f3a3-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-114">This method can return one of these values.</span></span>



| <span data-ttu-id="5f3a3-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5f3a3-115">Return code</span></span>                                                                          | <span data-ttu-id="5f3a3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f3a3-116">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="5f3a3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f3a3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5f3a3-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-118">Method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f3a3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f3a3-119">Remarks</span></span>

<span data-ttu-id="5f3a3-120">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Arbeitsspeicher für die Parameter " *pkeytype* " und " *ppkeydata* " zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-120">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pKeyType* and *ppKeyData* parameters.</span></span> <span data-ttu-id="5f3a3-121">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variablen nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="5f3a3-121">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f3a3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f3a3-122">Requirements</span></span>



| <span data-ttu-id="5f3a3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f3a3-123">Requirement</span></span> | <span data-ttu-id="5f3a3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5f3a3-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f3a3-125">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5f3a3-125">TAPI version</span></span><br/> | <span data-ttu-id="5f3a3-126">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5f3a3-126">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5f3a3-127">Header</span><span class="sxs-lookup"><span data-stu-id="5f3a3-127">Header</span></span><br/>       | <dl> <span data-ttu-id="5f3a3-128"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f3a3-128"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f3a3-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f3a3-129">Library</span></span><br/>      | <dl> <span data-ttu-id="5f3a3-130"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f3a3-130"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5f3a3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5f3a3-131">DLL</span></span><br/>          | <dl> <span data-ttu-id="5f3a3-132"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f3a3-132"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f3a3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f3a3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f3a3-134">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="5f3a3-134">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

