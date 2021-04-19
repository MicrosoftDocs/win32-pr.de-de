---
description: Die inetgetautodial-Funktion gibt die AutoDial-Einstellungen aus der Registrierung zurück.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: Inetgetautodial-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359710"
---
# <a name="inetgetautodial-function"></a><span data-ttu-id="4048a-103">Inetgetautodial-Funktion</span><span class="sxs-lookup"><span data-stu-id="4048a-103">InetGetAutodial function</span></span>

<span data-ttu-id="4048a-104">\[Diese Funktion wird nicht unterstützt und kann in zukünftigen Windows-Versionen geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="4048a-104">\[This function is unsupported and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="4048a-105">\]</span><span class="sxs-lookup"><span data-stu-id="4048a-105">\]</span></span>

<span data-ttu-id="4048a-106">Die **inetgetautodial** -Funktion gibt die AutoDial-Einstellungen aus der Registrierung zurück.</span><span class="sxs-lookup"><span data-stu-id="4048a-106">The **InetGetAutodial** function returns the autodial settings from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="4048a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4048a-107">Syntax</span></span>


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a><span data-ttu-id="4048a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4048a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4048a-109">*lpfenable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4048a-109">*lpfEnable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4048a-110">Gibt an, ob AutoDial aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4048a-110">Indicates whether autodial is enabled.</span></span> <span data-ttu-id="4048a-111">Der Wert **true** bei Return gibt an, dass AutoDial aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4048a-111">A value of **TRUE** upon return indicates autodial is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="4048a-112">*lpszentryname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4048a-112">*lpszEntryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4048a-113">Enthält bei der Rückgabe den Namen des Telefonbucheintrags, der für AutoDial festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4048a-113">On return, contains the name of the phone book entry that is set for autodial.</span></span>

</dd> <dt>

<span data-ttu-id="4048a-114">*cbentrynamesize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4048a-114">*cbEntryNameSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4048a-115">Größe des Puffers, der vom Aufrufer für den Namen des Telefonbucheintrags zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4048a-115">Size of the buffer allocated by the caller for the phone book entry name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4048a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4048a-116">Return value</span></span>

<span data-ttu-id="4048a-117">Diese Funktion kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4048a-117">This function can return one of these values.</span></span>



| <span data-ttu-id="4048a-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4048a-118">Return code</span></span>                                                                                                | <span data-ttu-id="4048a-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4048a-119">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4048a-120"><dt>**Fehler \_ erfolgreich**</dt></span><span class="sxs-lookup"><span data-stu-id="4048a-120"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="4048a-121">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4048a-121">The call was successful.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="4048a-122"><dt>**Ungültige Argumente für Fehler \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4048a-122"><dt>**ERROR\_BAD\_ARGUMENTS**</dt></span></span> </dl>       | <span data-ttu-id="4048a-123">*lpfenable* oder *lpszentryname* enthält einen **null** -Zeiger, oder der Wert von *cbentrynamesize* ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4048a-123">*lpfEnable* or *lpszEntryName* contains a **NULL** pointer, or the value of *cbEntryNameSize* is zero.</span></span><br/>                                         |
| <dl> <span data-ttu-id="4048a-124"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="4048a-124"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>  | <span data-ttu-id="4048a-125">Es war nicht genügend Arbeitsspeicher zum Zuordnen interner Puffer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4048a-125">There was insufficient memory to allocate internal buffers.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="4048a-126"><dt>**Fehler \_ beim \_ Puffer.**</dt></span><span class="sxs-lookup"><span data-stu-id="4048a-126"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="4048a-127">*cbentrynamesize* gibt nicht an, dass der Puffer, auf den von *lpszentryname* verwiesen wird, groß genug ist, um den Namen des Telefonbucheintrags zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4048a-127">*cbEntryNameSize* does not indicate that the buffer pointed to by *lpszEntryName* is large enough to receive the name of the phone book entry.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4048a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4048a-128">Remarks</span></span>

<span data-ttu-id="4048a-129">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4048a-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4048a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4048a-130">Requirements</span></span>



| <span data-ttu-id="4048a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4048a-131">Requirement</span></span> | <span data-ttu-id="4048a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4048a-132">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4048a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4048a-133">DLL</span></span><br/> | <dl> <span data-ttu-id="4048a-134"><dt>Inetcfg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4048a-134"><dt>Inetcfg.dll</dt></span></span> </dl> |



 

 
