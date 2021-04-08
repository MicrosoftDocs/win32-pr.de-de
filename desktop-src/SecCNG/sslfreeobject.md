---
description: Gibt ein Schlüssel-, Hash-oder Anbieter Objekt frei.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: Sslfreobject-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864208"
---
# <a name="sslfreeobject-function"></a><span data-ttu-id="50f8e-103">Sslfreobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="50f8e-103">SslFreeObject function</span></span>

<span data-ttu-id="50f8e-104">Die **sslfreobject** -Funktion gibt ein Schlüssel-, Hash-oder Anbieter Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="50f8e-104">The **SslFreeObject** function frees a key, hash, or provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f8e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50f8e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="50f8e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50f8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50f8e-107">*hobject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50f8e-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50f8e-108">Das Handle des-Objekts, das freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="50f8e-108">The handle of the object to free.</span></span>

</dd> <dt>

<span data-ttu-id="50f8e-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50f8e-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50f8e-110">Dieser Parameter ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="50f8e-110">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50f8e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50f8e-111">Return value</span></span>

<span data-ttu-id="50f8e-112">Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="50f8e-112">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="50f8e-113">Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50f8e-113">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="50f8e-114">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="50f8e-114">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="50f8e-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="50f8e-115">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="50f8e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50f8e-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="50f8e-117"><dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt></span><span class="sxs-lookup"><span data-stu-id="50f8e-117"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="50f8e-118">Ein internes Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="50f8e-118">An internal handle is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="50f8e-119"><dt>**Status \_ Ungültiges \_ handle**</dt> <dt>0xc0000008l</dt></span><span class="sxs-lookup"><span data-stu-id="50f8e-119"><dt>**STATUS\_INVALID\_HANDLE**</dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="50f8e-120">Das angegebene Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="50f8e-120">The provided handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50f8e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50f8e-121">Requirements</span></span>



| <span data-ttu-id="50f8e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50f8e-122">Requirement</span></span> | <span data-ttu-id="50f8e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="50f8e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f8e-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50f8e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="50f8e-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50f8e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="50f8e-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50f8e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="50f8e-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50f8e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="50f8e-128">Header</span><span class="sxs-lookup"><span data-stu-id="50f8e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="50f8e-129"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="50f8e-129"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="50f8e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="50f8e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50f8e-131"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50f8e-131"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




