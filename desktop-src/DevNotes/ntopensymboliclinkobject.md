---
description: Öffnet einen vorhandenen symbolischen Link.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: Ntopensymboliclinkobject-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357715"
---
# <a name="ntopensymboliclinkobject-function"></a><span data-ttu-id="d2050-103">Ntopensymboliclinkobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="d2050-103">NtOpenSymbolicLinkObject function</span></span>

<span data-ttu-id="d2050-104">\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="d2050-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="d2050-105">Öffnet einen vorhandenen symbolischen Link.</span><span class="sxs-lookup"><span data-stu-id="d2050-105">Opens an existing symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2050-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2050-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="d2050-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2050-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2050-108">*Linkhandle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d2050-108">*LinkHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2050-109">Ein Handle für das neu geöffnete symbolische Verknüpfungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="d2050-109">A handle to the newly opened symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="d2050-110">*DesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2050-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2050-111">Eine [**Zugriffs \_ Maske**](../secauthz/access-mask.md) , die den angeforderten Zugriff auf das Verzeichnis Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="d2050-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="d2050-112">Es ist typisch, den generischen Lesevorgang zu verwenden, \_ damit das Handle an die [**ntquerydirectoryobject**](ntquerydirectoryobject.md) -Funktion weitergeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2050-112">It is typical to use GENERIC\_READ so the handle can be passed to the [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d2050-113">*Objectattributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2050-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2050-114">Die Attribute für das Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="d2050-114">The attributes for the directory object.</span></span> <span data-ttu-id="d2050-115">Um die **Objekt \_ Attribut** Struktur zu initialisieren, verwenden Sie das **initializeobjectattributes** -Makro.</span><span class="sxs-lookup"><span data-stu-id="d2050-115">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="d2050-116">Wenn der Aufrufer nicht in einem System Thread Kontext ausgeführt wird, muss er das **obj \_ - \_ KERNELHANDLE-** Flag angeben, wenn die Struktur initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d2050-116">If the caller is not running in a system thread context, it must specify the **OBJ\_KERNEL\_HANDLE** flag when initializing the structure.</span></span> <span data-ttu-id="d2050-117">Weitere Informationen finden Sie in der Dokumentation für diese Elemente in der Dokumentation für das WDK.</span><span class="sxs-lookup"><span data-stu-id="d2050-117">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2050-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2050-118">Return value</span></span>

<span data-ttu-id="d2050-119">Die Funktion gibt **Status \_ Erfolg** oder einen Fehlerstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="d2050-119">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2050-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2050-120">Remarks</span></span>

<span data-ttu-id="d2050-121">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d2050-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2050-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2050-122">Requirements</span></span>



| <span data-ttu-id="d2050-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2050-123">Requirement</span></span> | <span data-ttu-id="d2050-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d2050-124">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2050-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d2050-125">DLL</span></span><br/> | <dl> <span data-ttu-id="d2050-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2050-126"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2050-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2050-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2050-128">**Ntquerydirectoryobject**</span><span class="sxs-lookup"><span data-stu-id="d2050-128">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
