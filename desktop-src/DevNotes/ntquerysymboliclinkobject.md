---
description: Ruft das Ziel einer symbolischen Verknüpfung ab.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: Ntquerysymboliclinkobject-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354076"
---
# <a name="ntquerysymboliclinkobject-function"></a><span data-ttu-id="217e4-103">Ntquerysymboliclinkobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="217e4-103">NtQuerySymbolicLinkObject function</span></span>

<span data-ttu-id="217e4-104">\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="217e4-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="217e4-105">Ruft das Ziel einer symbolischen Verknüpfung ab.</span><span class="sxs-lookup"><span data-stu-id="217e4-105">Retrieves the target of a symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="217e4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="217e4-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a><span data-ttu-id="217e4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="217e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217e4-108">*Linkhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="217e4-108">*LinkHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="217e4-109">Ein Handle für das symbolische Verknüpfungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="217e4-109">A handle to the symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="217e4-110">*LinkTarget* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="217e4-110">*LinkTarget* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="217e4-111">Ein Zeiger auf eine initialisierte Unicode-Zeichenfolge, die das Ziel der symbolischen Verknüpfung empfängt.</span><span class="sxs-lookup"><span data-stu-id="217e4-111">A pointer to an initialized Unicode string that receives the target of the symbolic link.</span></span> <span data-ttu-id="217e4-112">Die **MaximumLength** -und **buffer** -Elemente müssen festgelegt werden, wenn der-Befehl fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="217e4-112">The **MaximumLength** and **Buffer** members must be set if the call fails.</span></span>

</dd> <dt>

<span data-ttu-id="217e4-113">*Rückkehrnedlength* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="217e4-113">*ReturnedLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="217e4-114">Ein Zeiger auf eine Variable, die die Länge der Unicode-Zeichenfolge empfängt, die im *LinkTarget* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="217e4-114">A pointer to a variable that receives the length of the Unicode string returned in the *LinkTarget* parameter.</span></span> <span data-ttu-id="217e4-115">Wenn die Funktion den **Status \_ Puffer \_ zu \_ klein** zurückgibt, erhält diese Variable die erforderliche Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="217e4-115">If the function returns **STATUS\_BUFFER\_TOO\_SMALL**, this variable receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217e4-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="217e4-116">Return value</span></span>

<span data-ttu-id="217e4-117">Die Funktion gibt **Status \_ Erfolg** oder einen Fehlerstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="217e4-117">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="217e4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="217e4-118">Remarks</span></span>

<span data-ttu-id="217e4-119">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="217e4-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="217e4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="217e4-120">Requirements</span></span>



| <span data-ttu-id="217e4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="217e4-121">Requirement</span></span> | <span data-ttu-id="217e4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="217e4-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="217e4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="217e4-123">DLL</span></span><br/> | <dl> <span data-ttu-id="217e4-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="217e4-124"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="217e4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="217e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="217e4-126">**Ntopensymboliclinkobject**</span><span class="sxs-lookup"><span data-stu-id="217e4-126">**NtOpenSymbolicLinkObject**</span></span>](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
