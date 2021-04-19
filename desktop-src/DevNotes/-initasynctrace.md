---
description: Initialisiert die Ablauf Verfolgung.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: Initasynctrace-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: f79137fe4e832a193bafa59a573e5eb541884a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367584"
---
# <a name="initasynctrace-function"></a><span data-ttu-id="97fdf-103">Initasynctrace-Funktion</span><span class="sxs-lookup"><span data-stu-id="97fdf-103">InitAsyncTrace function</span></span>

<span data-ttu-id="97fdf-104">Initialisiert die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="97fdf-104">Initializes the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="97fdf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="97fdf-105">Syntax</span></span>


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="97fdf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97fdf-106">Parameters</span></span>

<span data-ttu-id="97fdf-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="97fdf-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97fdf-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97fdf-108">Return value</span></span>

<span data-ttu-id="97fdf-109">Diese Funktion gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="97fdf-109">This function returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97fdf-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97fdf-110">Remarks</span></span>

<span data-ttu-id="97fdf-111">Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="97fdf-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="97fdf-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="97fdf-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="97fdf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97fdf-113">Requirements</span></span>



| <span data-ttu-id="97fdf-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97fdf-114">Requirement</span></span> | <span data-ttu-id="97fdf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="97fdf-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97fdf-116">DLL</span><span class="sxs-lookup"><span data-stu-id="97fdf-116">DLL</span></span><br/> | <dl> <span data-ttu-id="97fdf-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97fdf-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
