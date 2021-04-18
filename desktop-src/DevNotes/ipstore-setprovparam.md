---
description: Legt die angegebenen Parameterinformationen fest.
ms.assetid: fe3fe5cf-e8b8-40ca-9e12-9d92489982a7
title: 'Ipstore:: setprovparam-Methode (pstore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.SetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: edbbb7bd2f5d889568623390d805659e1cf840f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358235"
---
# <a name="ipstoresetprovparam-method"></a><span data-ttu-id="5b841-103">Ipstore:: setprovparam-Methode</span><span class="sxs-lookup"><span data-stu-id="5b841-103">IPStore::SetProvParam method</span></span>

<span data-ttu-id="5b841-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5b841-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5b841-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5b841-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5b841-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="5b841-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5b841-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="5b841-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5b841-108">Legt die angegebenen Parameterinformationen fest.</span><span class="sxs-lookup"><span data-stu-id="5b841-108">Sets the specified parameter information.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b841-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b841-109">Syntax</span></span>


```C++
HRESULT SetProvParam(
  [in] DWORD dwParam,
  [in] DWORD cbData,
       BYTE  *pbData,
       DWORD *dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5b841-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b841-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b841-111">*dwparam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b841-111">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b841-112">Enthält den PST-ping- **\_ \_ \_ PW- \_ Cache** , um den Benutzer Kenn Wort Cache zu leeren.</span><span class="sxs-lookup"><span data-stu-id="5b841-112">Contains **PST\_PP\_FLUSH\_PW\_CACHE** to flush the user password cache.</span></span>

</dd> <dt>

<span data-ttu-id="5b841-113">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b841-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b841-114">Die Länge des Kennworts im Puffer.</span><span class="sxs-lookup"><span data-stu-id="5b841-114">The length of the password in the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b841-115">*pbData*</span><span class="sxs-lookup"><span data-stu-id="5b841-115">*pbData*</span></span> 
</dt> <dd>

<span data-ttu-id="5b841-116">Ein Zeiger auf einen Puffer, der das Kennwort des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="5b841-116">A pointer to a buffer that contains the user's password.</span></span> <span data-ttu-id="5b841-117">Diese muss auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5b841-117">This must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5b841-118">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="5b841-118">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5b841-119">Reserviert: muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5b841-119">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b841-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b841-120">Return value</span></span>

<span data-ttu-id="5b841-121">Der Rückgabewert ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="5b841-121">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="5b841-122">Der Wert **PST \_ E \_ OK** gibt an, dass die Funktion erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5b841-122">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b841-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b841-123">Requirements</span></span>



| <span data-ttu-id="5b841-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b841-124">Requirement</span></span> | <span data-ttu-id="5b841-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5b841-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b841-126">Header</span><span class="sxs-lookup"><span data-stu-id="5b841-126">Header</span></span><br/> | <dl> <span data-ttu-id="5b841-127"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b841-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="5b841-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5b841-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="5b841-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b841-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b841-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b841-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b841-131">**Ipstore**</span><span class="sxs-lookup"><span data-stu-id="5b841-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
