---
description: Erstellt ein Benutzerzertifikat für die Verwendung mit NetMeeting-Konferenzen.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: Nmmakecert-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359646"
---
# <a name="nmmakecert-function"></a><span data-ttu-id="4204e-103">Nmmakecert-Funktion</span><span class="sxs-lookup"><span data-stu-id="4204e-103">NmMakeCert function</span></span>

<span data-ttu-id="4204e-104">Erstellt ein Benutzerzertifikat für die Verwendung mit NetMeeting-Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="4204e-104">Creates a user certificate for use with NetMeeting conferencing.</span></span>

## <a name="syntax"></a><span data-ttu-id="4204e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4204e-105">Syntax</span></span>


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4204e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4204e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4204e-107">*szfirstname*</span><span class="sxs-lookup"><span data-stu-id="4204e-107">*szFirstName*</span></span> 
</dt> <dd>

<span data-ttu-id="4204e-108">Dies ist der Vorname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="4204e-108">The user's first name.</span></span>

</dd> <dt>

<span data-ttu-id="4204e-109">*szlastname*</span><span class="sxs-lookup"><span data-stu-id="4204e-109">*szLastName*</span></span> 
</dt> <dd>

<span data-ttu-id="4204e-110">Dies ist der Nachname des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="4204e-110">The user's last name.</span></span>

</dd> <dt>

<span data-ttu-id="4204e-111">*szemailname*</span><span class="sxs-lookup"><span data-stu-id="4204e-111">*szEmailName*</span></span> 
</dt> <dd>

<span data-ttu-id="4204e-112">Der e-Mail-Name des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="4204e-112">The user's email name.</span></span>

</dd> <dt>

<span data-ttu-id="4204e-113">*szcity*</span><span class="sxs-lookup"><span data-stu-id="4204e-113">*szCity*</span></span> 
</dt> <dd>

<span data-ttu-id="4204e-114">Die Stadt des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="4204e-114">The user's city.</span></span>

</dd> <dt>

<span data-ttu-id="4204e-115">*szcountry*</span><span class="sxs-lookup"><span data-stu-id="4204e-115">*szCountry*</span></span> 
</dt> <dd>

<span data-ttu-id="4204e-116">Das Land/die Region des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="4204e-116">The user's country/region.</span></span>

</dd> <dt>

<span data-ttu-id="4204e-117">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4204e-117">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="4204e-118">Ein Wert, der angibt, wie das Zertifikat erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4204e-118">A value that indicates how the certificate should be created.</span></span> <span data-ttu-id="4204e-119">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="4204e-119">Values can be any of the following.</span></span>



| <span data-ttu-id="4204e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4204e-120">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="4204e-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4204e-121">Meaning</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <span data-ttu-id="4204e-122"><dt>**Nmmkcert \_ F \_ \_ nur**</dt> " <dt>0x00000004</dt> " bereinigen</span><span class="sxs-lookup"><span data-stu-id="4204e-122"><dt>**NMMKCERT\_F\_CLEANUP\_ONLY**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="4204e-123">Löschen Sie das alte Zertifikat, ohne eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4204e-123">Delete the old certificate without creating a new one.</span></span> <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <span data-ttu-id="4204e-124"><dt>**Nmmkcert \_ F \_ deleteoldcert**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4204e-124"><dt>**NMMKCERT\_F\_DELETEOLDCERT**</dt> <dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="4204e-125">Löschen Sie das alte Zertifikat, das zuvor mit dieser Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4204e-125">Delete the old certificate previously created with this function.</span></span> <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <span data-ttu-id="4204e-126"><dt>**Nmmkcert \_ F \_ lokaler \_ Computer**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="4204e-126"><dt>**NMMKCERT\_F\_LOCAL\_MACHINE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="4204e-127">Erstellen Sie das Zertifikat im Zertifikat Speicher des lokalen Computers.</span><span class="sxs-lookup"><span data-stu-id="4204e-127">Create the certificate in the local machine certificate store.</span></span> <br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4204e-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4204e-128">Return value</span></span>

<span data-ttu-id="4204e-129">Gibt 1 zurück, wenn die Funktion erfolgreich ist, und – 1, wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="4204e-129">Returns 1 if the function succeeds and –1 if the function fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="4204e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4204e-130">Remarks</span></span>

<span data-ttu-id="4204e-131">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4204e-131">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4204e-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4204e-132">Requirements</span></span>



| <span data-ttu-id="4204e-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4204e-133">Requirement</span></span> | <span data-ttu-id="4204e-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4204e-134">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4204e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4204e-135">DLL</span></span><br/> | <dl> <span data-ttu-id="4204e-136"><dt>Nmmkcert.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4204e-136"><dt>Nmmkcert.dll</dt></span></span> </dl> |



 

 
