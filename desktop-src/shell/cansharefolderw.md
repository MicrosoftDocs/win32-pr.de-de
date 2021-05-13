---
description: Wird verwendet, um zu bestimmen, ob die Option Diesen Ordner freigeben in der Webansicht angezeigt werden soll.
title: CanShareFolderW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 46df03208ecc468aac366fb0b4cfb33e1a68157e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841681"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="3f62f-103">CanShareFolderW-Funktion</span><span class="sxs-lookup"><span data-stu-id="3f62f-103">CanShareFolderW function</span></span>

<span data-ttu-id="3f62f-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f62f-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="3f62f-105">Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="3f62f-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3f62f-106">Wird verwendet, um zu bestimmen, ob die Option **Diesen Ordner freigeben** in der Webansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f62f-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f62f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f62f-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="3f62f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f62f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f62f-109">*pszPath* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3f62f-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f62f-110">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3f62f-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="3f62f-111">Ein Zeiger auf eine Zeichenfolge, die den Pfad des zu testden Ordners angibt.</span><span class="sxs-lookup"><span data-stu-id="3f62f-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f62f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f62f-112">Return value</span></span>

<span data-ttu-id="3f62f-113">Typ: **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="3f62f-113">Type: **STDAPI**</span></span>

<span data-ttu-id="3f62f-114">Die Rückgabewerte umfassen Folgendes.</span><span class="sxs-lookup"><span data-stu-id="3f62f-114">Return values include the following.</span></span>



| <span data-ttu-id="3f62f-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="3f62f-115">Return code/value</span></span>                                                                        | <span data-ttu-id="3f62f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f62f-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f62f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f62f-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="3f62f-118">Der Pfad, auf den *pszPath zeigt,* gibt einen Ordner an, der freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f62f-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="3f62f-119"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3f62f-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="3f62f-120">Der Pfad, auf den *pszPath zeigt,* gibt einen Ordner an, der nicht freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f62f-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="3f62f-121"><dt>HRESULT-Fehler</dt></span><span class="sxs-lookup"><span data-stu-id="3f62f-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="3f62f-122">Es ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3f62f-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="3f62f-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f62f-123">Remarks</span></span>

<span data-ttu-id="3f62f-124">Dieser Funktion ist keine LIB-Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3f62f-124">This function has no associated .lib file.</span></span> <span data-ttu-id="3f62f-125">Sie müssen [**LoadLibrary und**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**GetProcAddress verwenden,**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) um sie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f62f-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f62f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f62f-126">Requirements</span></span>



| <span data-ttu-id="3f62f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f62f-127">Requirement</span></span> | <span data-ttu-id="3f62f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3f62f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f62f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f62f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3f62f-130">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f62f-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3f62f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f62f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3f62f-132">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f62f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3f62f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3f62f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f62f-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f62f-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f62f-135">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3f62f-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3f62f-136">**CanShareFolderW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="3f62f-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="3f62f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f62f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f62f-138">**ShowShareFolderUI**</span><span class="sxs-lookup"><span data-stu-id="3f62f-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
