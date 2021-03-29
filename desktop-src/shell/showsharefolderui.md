---
description: Zeigt die Registerkarte Ordner Freigabe auf der Eigenschaften Seite für den angegebenen Ordner an.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: Showsharefolderui-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346428"
---
# <a name="showsharefolderui-function"></a><span data-ttu-id="c88db-103">Showsharefolderui-Funktion</span><span class="sxs-lookup"><span data-stu-id="c88db-103">ShowShareFolderUI function</span></span>

<span data-ttu-id="c88db-104">Zeigt die Registerkarte **Ordner Freigabe** auf der Eigenschaften Seite für den angegebenen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="c88db-104">Displays the **Folder Sharing** tab on the properties sheet for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c88db-105">Syntax</span></span>


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="c88db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c88db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c88db-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c88db-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88db-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="c88db-108">Type: **HWND**</span></span>

<span data-ttu-id="c88db-109">Ein Handle für das übergeordnete Fenster für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="c88db-109">A handle to the parent window for the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="c88db-110">*pszpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c88db-110">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c88db-111">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="c88db-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="c88db-112">Ein Zeiger auf eine Zeichenfolge, die den Pfad zum Ordner angibt, in dem die Registerkarte für die **Ordner Freigabe** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c88db-112">A pointer to a string that specifies the path to the folder that displays its **Folder Sharing** tab.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c88db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c88db-113">Return value</span></span>

<span data-ttu-id="c88db-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c88db-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c88db-115">Diese Funktion gibt immer \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="c88db-115">This function always returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88db-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c88db-116">Remarks</span></span>

<span data-ttu-id="c88db-117">Diese Funktion verfügt über keine zugehörige lib-Datei.</span><span class="sxs-lookup"><span data-stu-id="c88db-117">This function has no associated .lib file.</span></span> <span data-ttu-id="c88db-118">Sie müssen " [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) " und " [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) " verwenden, um Sie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c88db-118">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c88db-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c88db-119">Requirements</span></span>



| <span data-ttu-id="c88db-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c88db-120">Requirement</span></span> | <span data-ttu-id="c88db-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c88db-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c88db-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c88db-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c88db-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c88db-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c88db-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c88db-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c88db-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c88db-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c88db-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c88db-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c88db-127"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c88db-127"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="c88db-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c88db-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c88db-129">**Showsharefolderuiw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="c88db-129">**ShowShareFolderUIW** (Unicode)</span></span><br/>                                            |



## <a name="see-also"></a><span data-ttu-id="c88db-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c88db-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88db-131">**Cansharefolderw**</span><span class="sxs-lookup"><span data-stu-id="c88db-131">**CanShareFolderW**</span></span>](cansharefolderw.md)
</dt> </dl>

 

 
