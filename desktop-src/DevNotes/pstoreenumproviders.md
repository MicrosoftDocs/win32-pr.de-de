---
description: Ruft ein Enumeratorobjekt ab, das wiederum zum Auflisten der geschützten Speicher Anbieter verwendet werden kann, die zurzeit auf dem System installiert sind.
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: Pstoreenumproviders-Funktion (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371459"
---
# <a name="pstoreenumproviders-function"></a><span data-ttu-id="b97e4-103">Pstoreenumproviders-Funktion</span><span class="sxs-lookup"><span data-stu-id="b97e4-103">PStoreEnumProviders function</span></span>

<span data-ttu-id="b97e4-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b97e4-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b97e4-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b97e4-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b97e4-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="b97e4-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b97e4-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="b97e4-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b97e4-108">Ruft ein Enumeratorobjekt ab, das wiederum zum Auflisten der geschützten Speicher Anbieter verwendet werden kann, die zurzeit auf dem System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="b97e4-108">Gets an enumerator object that can be used in turn to enumerate the protected storage providers that are currently installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b97e4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b97e4-109">Syntax</span></span>


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="b97e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b97e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b97e4-111">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b97e4-111">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b97e4-112">Dieser Parameter wird nicht verwendet und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b97e4-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b97e4-113">*ppum*</span><span class="sxs-lookup"><span data-stu-id="b97e4-113">*ppenum*</span></span> 
</dt> <dd>

<span data-ttu-id="b97e4-114">Ein Zeiger auf einen Zeiger auf eine [**ienumpstoreproviders**](ienumpstoreproviders.md) -Schnittstelle, die zum Aufzählen installierter Anbieter verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b97e4-114">A pointer to a pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) interface that can be used to enumerate installed providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b97e4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b97e4-115">Return value</span></span>

<span data-ttu-id="b97e4-116">Diese Funktion gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="b97e4-116">This function returns an **HRESULT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b97e4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b97e4-117">Remarks</span></span>

<span data-ttu-id="b97e4-118">Die geschützte Speicherkomponente verfügt über eine Anbieter basierte Architektur.</span><span class="sxs-lookup"><span data-stu-id="b97e4-118">The protected storage component has a provider-based architecture.</span></span> <span data-ttu-id="b97e4-119">Anwendungen, die geschützten Speicher nutzen, können angeben, welche der installierten Anbieter beim Speichern und Abrufen der Daten verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b97e4-119">Applications that make use of protected storage can specify which of the installed providers to use when storing and retrieving their data.</span></span>

<span data-ttu-id="b97e4-120">Die **pstoreenumproviders** -Funktion wird zum Auflisten der installierten geschützten Speicher Anbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="b97e4-120">The **PStoreEnumProviders** function is used to enumerate the installed protected storage providers.</span></span> <span data-ttu-id="b97e4-121">Jeder Anbieter wird durch einen Globally Unique Identifier (GUID) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b97e4-121">Each provider is identified by a globally unique identifier (GUID).</span></span>

<span data-ttu-id="b97e4-122">Bis zu diesem Zeitpunkt wurde immer nur ein geschützter Speicher Anbieter geschrieben.</span><span class="sxs-lookup"><span data-stu-id="b97e4-122">Up to this time, only one protected storage provider has ever been written.</span></span> <span data-ttu-id="b97e4-123">Da der geschützte Speicherdienst zurzeit veraltet ist, ist es sehr unwahrscheinlich, dass jemals weitere Anbieter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b97e4-123">Given that the protected storage service is currently deprecated, it is very unlikely that any additional providers will ever be produced.</span></span> <span data-ttu-id="b97e4-124">Daher sollte diese Funktion nicht für beliebige Zwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b97e4-124">As a result, this function should not be used for any purpose.</span></span>

<span data-ttu-id="b97e4-125">Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b97e4-125">This function has no associated import library; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b97e4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b97e4-126">Requirements</span></span>



| <span data-ttu-id="b97e4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b97e4-127">Requirement</span></span> | <span data-ttu-id="b97e4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b97e4-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b97e4-129">Header</span><span class="sxs-lookup"><span data-stu-id="b97e4-129">Header</span></span><br/> | <dl> <span data-ttu-id="b97e4-130"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b97e4-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="b97e4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b97e4-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="b97e4-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b97e4-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b97e4-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b97e4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b97e4-134">**Ienumpstoreproviders**</span><span class="sxs-lookup"><span data-stu-id="b97e4-134">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
