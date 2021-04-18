---
description: Sucht im Offlinedateien Cache nach einer Datei, die die angegebenen Kriterien erfüllt.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: Cscfindfirstfilew-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358693"
---
# <a name="cscfindfirstfilew-function"></a><span data-ttu-id="3c821-103">Cscfindfirstfilew-Funktion</span><span class="sxs-lookup"><span data-stu-id="3c821-103">CSCFindFirstFileW function</span></span>

<span data-ttu-id="3c821-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="3c821-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="3c821-105">Sucht im Offlinedateien Cache nach einer Datei, die die angegebenen Kriterien erfüllt.</span><span class="sxs-lookup"><span data-stu-id="3c821-105">Searches for a file in the Offline Files cache that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c821-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c821-106">Syntax</span></span>


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="3c821-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c821-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c821-108">*lpszfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c821-108">*lpszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c821-109">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die ein gültiges UNC-Verzeichnis oder einen gültigen Pfad angibt.</span><span class="sxs-lookup"><span data-stu-id="3c821-109">A pointer to a null-terminated string that specifies a valid UNC directory or path.</span></span>

</dd> <dt>

<span data-ttu-id="3c821-110">*lpFind32* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c821-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c821-111">Ein Zeiger auf die [**Win32 \_ - \_ Daten**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) Struktur, die Informationen über die Datei oder das Unterverzeichnis empfängt.</span><span class="sxs-lookup"><span data-stu-id="3c821-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="3c821-112">*lpdwstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c821-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c821-113">Ein NTSTATUS-Code, der den Status des Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="3c821-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="3c821-114">*lpdwpincount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c821-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c821-115">Dieser Parameter ist ungleich 0 (null), wenn die Datei offline verfügbar gemacht wurde, andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="3c821-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="3c821-116">*lpdwhintflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c821-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c821-117">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="3c821-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3c821-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3c821-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="3c821-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3c821-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="3c821-120"><dt>**Flag \_ CSC- \_ Hinweis- \_ Pin- \_ Benutzer**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="3c821-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="3c821-121">Ein Benutzer hat die Datei offline verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="3c821-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="3c821-122"><dt>**Flag \_ CSC- \_ Hinweis- \_ Pin \_ erben \_ Benutzer**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="3c821-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="3c821-123">Ein Benutzer hat das übergeordnete Element offline verfügbar gemacht und als übergeordnetes Element gekennzeichnet, sodass die untergeordneten Elemente offline verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3c821-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="3c821-124"><dt>**Flag \_ CSC- \_ Hinweis- \_ Pin \_ erbt \_ System**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="3c821-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="3c821-125">Ein Administrator oder eine Gruppenrichtlinie hat das übergeordnete Element offline zur Verfügung gestellt und als übergeordnetes Element gekennzeichnet, sodass die untergeordneten Elemente offline verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3c821-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="3c821-126"><dt>**Flag \_ CSC- \_ Hinweis- \_ Pin- \_ System**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="3c821-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="3c821-127">Die Datei wurde von einem Administrator oder einer Gruppenrichtlinie offline verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="3c821-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="3c821-128">*lporgfiletime* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3c821-128">*lpOrgFileTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c821-129">Ein Zeiger auf eine [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, um die Datums-und Uhrzeit Informationen für die Datei oder das Unterverzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3c821-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c821-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c821-130">Return value</span></span>

<span data-ttu-id="3c821-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Such handle, das in einem nachfolgenden [**cscfindnextfilew**](cscfindnextfilew.md) -oder [**cscfindclose**](cscfindclose.md)-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c821-131">If the function succeeds, the return value is a search handle used in a subsequent call to [**CSCFindNextFileW**](cscfindnextfilew.md) or [**CSCFindClose**](cscfindclose.md).</span></span>

<span data-ttu-id="3c821-132">Wenn bei der Ausführung der Funktion ein Fehler auftritt, lautet der Rückgabewert **INVALID\_HANDLE\_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="3c821-132">If the function fails, the return value is **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c821-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c821-133">Remarks</span></span>

<span data-ttu-id="3c821-134">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3c821-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c821-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c821-135">Requirements</span></span>



| <span data-ttu-id="3c821-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c821-136">Requirement</span></span> | <span data-ttu-id="3c821-137">Wert</span><span class="sxs-lookup"><span data-stu-id="3c821-137">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c821-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3c821-138">DLL</span></span><br/> | <dl> <span data-ttu-id="3c821-139"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c821-139"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
