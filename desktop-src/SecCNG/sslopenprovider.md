---
description: Öffnet ein Handle für den angegebenen SSL-Protokoll Anbieter (Secure Sockets Layer Protocol).
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Sslopenprovider-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214517"
---
# <a name="sslopenprovider-function"></a><span data-ttu-id="d0a38-103">Sslopenprovider-Funktion</span><span class="sxs-lookup"><span data-stu-id="d0a38-103">SslOpenProvider function</span></span>

<span data-ttu-id="d0a38-104">Die **sslopenprovider** -Funktion öffnet ein Handle für den angegebenen SSL-Protokoll Anbieter ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="d0a38-104">The **SslOpenProvider** function opens a handle to the specified [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0a38-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0a38-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d0a38-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0a38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a38-107">*phsslprovider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d0a38-107">*phSslProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a38-108">Die Adresse eines **NCrypt- \_ Prov- \_ Handles** , in dem das Anbieter handle geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0a38-108">The address of an **NCRYPT\_PROV\_HANDLE** in which to write the provider handle.</span></span>

<span data-ttu-id="d0a38-109">Wenn Sie die Verwendung des Handles abgeschlossen haben, sollten Sie es freigeben, indem Sie die [**sslfreeobject**](sslfreeobject.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d0a38-109">When you have finished using the handle, you should free it by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d0a38-110">*pszprovidername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0a38-110">*pszProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a38-111">Ein Zeiger auf eine Unicode-Zeichenfolge, die den Anbieter Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="d0a38-111">A pointer to a Unicode string that contains the provider name.</span></span> <span data-ttu-id="d0a38-112">Wenn der Wert dieses Parameters **null** ist, wird ein Handle für den **MS \_ SChannel- \_ Anbieter** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d0a38-112">If the value of this parameter is **NULL**, a handle to the **MS\_SCHANNEL\_PROVIDER** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="d0a38-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0a38-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0a38-114">Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d0a38-114">This parameter is reserved for future use, and it must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a38-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0a38-115">Return value</span></span>

<span data-ttu-id="d0a38-116">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d0a38-116">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="d0a38-117">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d0a38-117">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="d0a38-118">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="d0a38-118">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="d0a38-119">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="d0a38-119">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="d0a38-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0a38-120">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d0a38-121"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="d0a38-121"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="d0a38-122">Eines der bereitgestellten Handles ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="d0a38-122">One of the provided handles is not valid.</span></span><br/>                      |
| <dl> <span data-ttu-id="d0a38-123"><dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt></span><span class="sxs-lookup"><span data-stu-id="d0a38-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="d0a38-124">Der Parameter " *phsslprovider* " oder " *ppproviderlist* " ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d0a38-124">The *phSslProvider* or *ppProviderList* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="d0a38-125"><dt>**Status \_ Kein Arbeits \_ Speicher**</dt> <dt>0xc0000017l</dt></span><span class="sxs-lookup"><span data-stu-id="d0a38-125"><dt>**STATUS\_NO\_MEMORY**</dt> <dt>0xC0000017L</dt></span></span> </dl>      | <span data-ttu-id="d0a38-126">Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d0a38-126">Not enough memory is available to allocate necessary buffers.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="d0a38-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0a38-127">Requirements</span></span>



| <span data-ttu-id="d0a38-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0a38-128">Requirement</span></span> | <span data-ttu-id="d0a38-129">Wert</span><span class="sxs-lookup"><span data-stu-id="d0a38-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a38-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0a38-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a38-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0a38-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d0a38-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0a38-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a38-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0a38-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d0a38-134">Header</span><span class="sxs-lookup"><span data-stu-id="d0a38-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a38-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a38-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="d0a38-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d0a38-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0a38-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0a38-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

