---
description: Setzt einen Datei Suchvorgang fort.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: Cscfindnextfilew-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351352"
---
# <a name="cscfindnextfilew-function"></a><span data-ttu-id="e23bd-103">Cscfindnextfilew-Funktion</span><span class="sxs-lookup"><span data-stu-id="e23bd-103">CSCFindNextFileW function</span></span>

<span data-ttu-id="e23bd-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="e23bd-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="e23bd-105">Setzt einen Datei Suchvorgang fort.</span><span class="sxs-lookup"><span data-stu-id="e23bd-105">Continues a file search operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e23bd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e23bd-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="e23bd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e23bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e23bd-108">*hfind* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e23bd-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e23bd-109">Ein Suchhandle, das von der [**cscfindfirstfilew**](cscfindfirstfilew.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e23bd-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e23bd-110">*lpFind32* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e23bd-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e23bd-111">Ein Zeiger auf die [**Win32 \_ - \_ Daten**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) Struktur, die Informationen über die Datei oder das Unterverzeichnis empfängt.</span><span class="sxs-lookup"><span data-stu-id="e23bd-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="e23bd-112">*lpdwstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e23bd-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e23bd-113">Ein NTSTATUS-Code, der den Status des Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="e23bd-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="e23bd-114">*lpdwpincount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e23bd-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e23bd-115">Dieser Parameter ist ungleich 0 (null), wenn die Datei offline verfügbar gemacht wurde, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="e23bd-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="e23bd-116">*lpdwhintflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e23bd-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e23bd-117">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="e23bd-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e23bd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e23bd-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="e23bd-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e23bd-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="e23bd-120"><dt>**Flag \_ CSC- \_ Hinweis- \_ Pin- \_ Benutzer**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e23bd-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="e23bd-121">Ein Benutzer hat die Datei offline verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="e23bd-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="e23bd-122"><dt>**Flag \_ CSC- \_ Hinweis- \_ Pin \_ erben \_ Benutzer**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e23bd-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="e23bd-123">Ein Benutzer hat das übergeordnete Element offline verfügbar gemacht und als übergeordnetes Element gekennzeichnet, sodass die untergeordneten Elemente offline verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e23bd-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="e23bd-124"><dt>**Flag \_ CSC- \_ Hinweis- \_ Pin \_ erbt \_ System**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="e23bd-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="e23bd-125">Ein Administrator oder eine Gruppenrichtlinie hat das übergeordnete Element offline zur Verfügung gestellt und als übergeordnetes Element gekennzeichnet, sodass die untergeordneten Elemente offline verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e23bd-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="e23bd-126"><dt>**Flag \_ CSC- \_ Hinweis- \_ Pin- \_ System**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="e23bd-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="e23bd-127">Die Datei wurde von einem Administrator oder einer Gruppenrichtlinie offline verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="e23bd-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="e23bd-128">*lporgfiletime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e23bd-128">*lpOrgFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e23bd-129">Ein Zeiger auf eine [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, um die Datums-und Uhrzeit Informationen für die Datei oder das Unterverzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e23bd-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e23bd-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e23bd-130">Return value</span></span>

<span data-ttu-id="e23bd-131">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e23bd-131">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e23bd-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e23bd-132">Remarks</span></span>

<span data-ttu-id="e23bd-133">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e23bd-133">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e23bd-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e23bd-134">Requirements</span></span>



| <span data-ttu-id="e23bd-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e23bd-135">Requirement</span></span> | <span data-ttu-id="e23bd-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e23bd-136">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e23bd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e23bd-137">DLL</span></span><br/> | <dl> <span data-ttu-id="e23bd-138"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e23bd-138"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
