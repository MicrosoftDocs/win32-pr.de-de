---
description: Ruft Informationen zum angegebenen Verzeichnis Objekt ab.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: Ntquerydirectoryobject-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364866"
---
# <a name="ntquerydirectoryobject-function"></a><span data-ttu-id="476e6-103">Ntquerydirectoryobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="476e6-103">NtQueryDirectoryObject function</span></span>

<span data-ttu-id="476e6-104">\[Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="476e6-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="476e6-105">Ruft Informationen zum angegebenen Verzeichnis Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="476e6-105">Retrieves information about the specified directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="476e6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="476e6-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="476e6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="476e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="476e6-108">*Directoryhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="476e6-108">*DirectoryHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="476e6-109">Ein Handle für das Verzeichnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="476e6-109">A handle to the directory object.</span></span>

</dd> <dt>

<span data-ttu-id="476e6-110">*Puffer* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="476e6-110">*Buffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="476e6-111">Ein Zeiger auf einen Puffer, der die Verzeichnisinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="476e6-111">A pointer to a buffer that receives the directory information.</span></span> <span data-ttu-id="476e6-112">Dieser Puffer empfängt mindestens eine **Objekt \_ Verzeichnis \_ Informations** Struktur, die letzte **null** ist, gefolgt von Zeichen folgen, die die Namen der Verzeichniseinträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="476e6-112">This buffer receives one or more **OBJECT\_DIRECTORY\_INFORMATION** structures, the last one being **NULL**, followed by strings that contain the names of the directory entries.</span></span> <span data-ttu-id="476e6-113">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="476e6-113">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="476e6-114">*Länge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="476e6-114">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="476e6-115">Die Größe des vom Benutzer bereitgestellten Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="476e6-115">The size of the user-supplied output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="476e6-116">*Returnsingleentry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="476e6-116">*ReturnSingleEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="476e6-117">Gibt an, ob die Funktion nur einen einzelnen Eintrag zurückgeben soll.</span><span class="sxs-lookup"><span data-stu-id="476e6-117">Indicates whether the function should return only a single entry.</span></span>

</dd> <dt>

<span data-ttu-id="476e6-118">*Restarstcan* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="476e6-118">*RestartScan* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="476e6-119">Gibt an, ob die Überprüfung neu gestartet oder die Enumeration mit den im *Kontext* Parameter übergebenen Informationen fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="476e6-119">Indicates whether to restart the scan or continue the enumeration using the information passed in the *Context* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="476e6-120">*Kontext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="476e6-120">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="476e6-121">Der enumerationskontext.</span><span class="sxs-lookup"><span data-stu-id="476e6-121">The enumeration context.</span></span>

</dd> <dt>

<span data-ttu-id="476e6-122">*Returnlength* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="476e6-122">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="476e6-123">Ein Zeiger auf eine Variable, die die Länge der im Ausgabepuffer zurückgegebenen Verzeichnisinformationen in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="476e6-123">A pointer to a variable that receives the length of the directory information returned in the output buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="476e6-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="476e6-124">Return value</span></span>

<span data-ttu-id="476e6-125">Die Funktion gibt **Status \_ Erfolg** oder einen Fehlerstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="476e6-125">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="476e6-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="476e6-126">Remarks</span></span>

<span data-ttu-id="476e6-127">Im folgenden finden Sie die Definition der **Objekt \_ Verzeichnis \_ Informations** Struktur.</span><span class="sxs-lookup"><span data-stu-id="476e6-127">The following is the definition of the **OBJECT\_DIRECTORY\_INFORMATION** structure.</span></span>

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

<span data-ttu-id="476e6-128">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="476e6-128">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="476e6-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="476e6-129">Requirements</span></span>



| <span data-ttu-id="476e6-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="476e6-130">Requirement</span></span> | <span data-ttu-id="476e6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="476e6-131">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="476e6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="476e6-132">DLL</span></span><br/> | <dl> <span data-ttu-id="476e6-133"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="476e6-133"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="476e6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="476e6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="476e6-135">**Ntopendirectoryobject**</span><span class="sxs-lookup"><span data-stu-id="476e6-135">**NtOpenDirectoryObject**</span></span>](ntopendirectoryobject.md)
</dt> </dl>

 

 
