---
description: Vergleicht zwei Zugriffs Token und bestimmt, ob Sie hinsichtlich eines Aufrufens der AccessCheck-Funktion äquivalent sind.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Ntcomparetokens-Funktion (ntabapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362410"
---
# <a name="ntcomparetokens-function"></a><span data-ttu-id="8c534-103">Ntcomparetokens-Funktion</span><span class="sxs-lookup"><span data-stu-id="8c534-103">NtCompareTokens function</span></span>

<span data-ttu-id="8c534-104">Die **ntcomparetokens** -Funktion vergleicht zwei [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) und bestimmt, ob Sie hinsichtlich eines Aufrufens der [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) -Funktion äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="8c534-104">The **NtCompareTokens** function compares two [*access tokens*](/windows/desktop/SecGloss/a-gly) and determines whether they are equivalent with respect to a call to the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c534-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c534-105">Syntax</span></span>


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a><span data-ttu-id="8c534-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c534-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c534-107">*Firsttokenhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c534-107">*FirstTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c534-108">Ein Handle für das erste zu vergleichende Zugriffs Token.</span><span class="sxs-lookup"><span data-stu-id="8c534-108">A handle to the first access token to compare.</span></span> <span data-ttu-id="8c534-109">Das Token muss für den **\_ tokenabfragezugriff** geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="8c534-109">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="8c534-110">*Secondtokenhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c534-110">*SecondTokenHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c534-111">Ein Handle für das zweite zu vergleichende Zugriffs Token.</span><span class="sxs-lookup"><span data-stu-id="8c534-111">A handle to the second access token to compare.</span></span> <span data-ttu-id="8c534-112">Das Token muss für den **\_ tokenabfragezugriff** geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="8c534-112">The token must be open for **TOKEN\_QUERY** access.</span></span>

</dd> <dt>

<span data-ttu-id="8c534-113">*Gleich* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8c534-113">*Equal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c534-114">Ein Zeiger auf eine Variable, die einen Wert empfängt, der angibt, ob die von den Parametern *firsttokenhandle* und *secondtokenhandle* dargestellten Token gleichwertig sind.</span><span class="sxs-lookup"><span data-stu-id="8c534-114">A pointer to a variable that receives a value that indicates whether the tokens represented by the *FirstTokenHandle* and *SecondTokenHandle* parameters are equivalent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c534-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c534-115">Return value</span></span>

<span data-ttu-id="8c534-116">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion Status \_ Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="8c534-116">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="8c534-117">Wenn die Funktion fehlschlägt, wird ein **NTSTATUS** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c534-117">If the function fails, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c534-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c534-118">Remarks</span></span>

<span data-ttu-id="8c534-119">Zwei Zugriffs Steuerungs Token werden als äquivalent betrachtet, wenn alle der folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="8c534-119">Two access control tokens are considered to be equivalent if all of the following conditions are true:</span></span>

-   <span data-ttu-id="8c534-120">Jede [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID), die in einem der beiden Token vorhanden ist, ist auch im anderen Token vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c534-120">Every [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) that is present in either token is also present in the other token.</span></span>
-   <span data-ttu-id="8c534-121">Keines oder beide Token sind beschränkt.</span><span class="sxs-lookup"><span data-stu-id="8c534-121">Neither or both of the tokens are restricted.</span></span>
-   <span data-ttu-id="8c534-122">Wenn beide Token eingeschränkt sind, wird jede sid, die in einem Token eingeschränkt ist, auch im anderen Token eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="8c534-122">If both tokens are restricted, every SID that is restricted in one token is also restricted in the other token.</span></span>
-   <span data-ttu-id="8c534-123">Alle in beiden Token vorhandenen Berechtigungen sind ebenfalls im anderen Token vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8c534-123">Every privilege present in either token is also present in the other token.</span></span>

<span data-ttu-id="8c534-124">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8c534-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c534-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c534-125">Requirements</span></span>



| <span data-ttu-id="8c534-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c534-126">Requirement</span></span> | <span data-ttu-id="8c534-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8c534-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c534-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c534-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8c534-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c534-129">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8c534-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c534-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8c534-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c534-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8c534-132">Header</span><span class="sxs-lookup"><span data-stu-id="8c534-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c534-133"><dt>NT\*-API. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c534-133"><dt>Ntseapi.h</dt></span></span> </dl> |
| <span data-ttu-id="8c534-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8c534-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c534-135"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c534-135"><dt>Ntdll.dll</dt></span></span> </dl> |



 

