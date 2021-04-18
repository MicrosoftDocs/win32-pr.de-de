---
description: Beendet die Ablauf Verfolgung.
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: Termasynctrace-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360985"
---
# <a name="termasynctrace-function"></a><span data-ttu-id="86a0b-103">Termasynctrace-Funktion</span><span class="sxs-lookup"><span data-stu-id="86a0b-103">TermAsyncTrace function</span></span>

<span data-ttu-id="86a0b-104">Beendet die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="86a0b-104">Terminates the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86a0b-105">Syntax</span></span>


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="86a0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86a0b-106">Parameters</span></span>

<span data-ttu-id="86a0b-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="86a0b-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86a0b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86a0b-108">Return value</span></span>

<span data-ttu-id="86a0b-109">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="86a0b-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="86a0b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86a0b-110">Remarks</span></span>

<span data-ttu-id="86a0b-111">Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="86a0b-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="86a0b-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="86a0b-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a0b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86a0b-113">Requirements</span></span>



| <span data-ttu-id="86a0b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86a0b-114">Requirement</span></span> | <span data-ttu-id="86a0b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="86a0b-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86a0b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="86a0b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="86a0b-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86a0b-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
