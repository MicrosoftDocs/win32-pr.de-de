---
description: Wird verwendet, um zu bestimmen, ob die Option diesen Ordner freigeben in der Webansicht angezeigt werden soll.
title: Cansharefolderw-Funktion
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
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525403"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="4738a-103">Cansharefolderw-Funktion</span><span class="sxs-lookup"><span data-stu-id="4738a-103">CanShareFolderW function</span></span>

<span data-ttu-id="4738a-104">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4738a-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="4738a-105">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4738a-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4738a-106">Wird verwendet, um zu bestimmen, ob die Option **diesen Ordner freigeben** in der Webansicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4738a-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="4738a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4738a-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="4738a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4738a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4738a-109">*pszpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4738a-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4738a-110">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="4738a-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="4738a-111">Ein Zeiger auf eine Zeichenfolge, die den Pfad des Ordners angibt, der getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4738a-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4738a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4738a-112">Return value</span></span>

<span data-ttu-id="4738a-113">Typ: **STDAPI**</span><span class="sxs-lookup"><span data-stu-id="4738a-113">Type: **STDAPI**</span></span>

<span data-ttu-id="4738a-114">Die Rückgabewerte umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4738a-114">Return values include the following.</span></span>



| <span data-ttu-id="4738a-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="4738a-115">Return code/value</span></span>                                                                        | <span data-ttu-id="4738a-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4738a-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4738a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4738a-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="4738a-118">Der Pfad, auf den von *pszpath* verwiesen wird, gibt einen Ordner an, der freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="4738a-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="4738a-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4738a-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="4738a-120">Der Pfad, auf den *pszpath* zeigt, gibt einen Ordner an, der nicht freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="4738a-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="4738a-121"><dt>HRESULT-Fehler</dt></span><span class="sxs-lookup"><span data-stu-id="4738a-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="4738a-122">Es ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4738a-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="4738a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4738a-123">Remarks</span></span>

<span data-ttu-id="4738a-124">Diese Funktion verfügt über keine zugehörige lib-Datei.</span><span class="sxs-lookup"><span data-stu-id="4738a-124">This function has no associated .lib file.</span></span> <span data-ttu-id="4738a-125">Sie müssen " [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) " und " [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) " verwenden, um Sie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4738a-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4738a-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4738a-126">Requirements</span></span>



| <span data-ttu-id="4738a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4738a-127">Requirement</span></span> | <span data-ttu-id="4738a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4738a-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4738a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4738a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4738a-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4738a-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4738a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4738a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4738a-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4738a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4738a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4738a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4738a-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4738a-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="4738a-135">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="4738a-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4738a-136">**Cansharefolderw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="4738a-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="4738a-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4738a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4738a-138">**Showsharefolderui**</span><span class="sxs-lookup"><span data-stu-id="4738a-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
