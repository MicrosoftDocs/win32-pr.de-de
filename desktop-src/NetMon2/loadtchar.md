---
description: Die loadtchar-Funktion wird von Monitoren aufgerufen, um eine Zeichen folgen Variable auf eine Zeichenfolge festzulegen, die aus einer HTML-Konfigurations Zeichenfolge stammt
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Loadtchar-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343706"
---
# <a name="loadtchar-function"></a><span data-ttu-id="00733-103">Loadtchar-Funktion</span><span class="sxs-lookup"><span data-stu-id="00733-103">LoadTCHAR function</span></span>

<span data-ttu-id="00733-104">Die **loadtchar** -Funktion wird von Monitoren aufgerufen, um eine Zeichen folgen Variable auf eine Zeichenfolge festzulegen, die aus einer HTML-Konfigurations Zeichenfolge stammt</span><span class="sxs-lookup"><span data-stu-id="00733-104">The **LoadTCHAR** function is called by monitors to set a string variable to a string taken from an HTML configuration string.</span></span>

## <a name="syntax"></a><span data-ttu-id="00733-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00733-105">Syntax</span></span>


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a><span data-ttu-id="00733-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00733-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00733-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00733-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00733-108">Zeiger auf die HTML-Konfigurations Zeichenfolge, die von der [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode an den Monitor übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="00733-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="00733-109">*pvarname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00733-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00733-110">Zeiger auf den Namen der Variablen in der Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="00733-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="00733-111">*ppszstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="00733-111">*ppszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00733-112">Zeiger auf einen Zeichen folgen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="00733-112">Pointer to a string pointer.</span></span> <span data-ttu-id="00733-113">Wenn der angeforderte Variablenname gefunden wird, wird die Zeichenfolge zugeordnet und diesem Zeiger zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="00733-113">If the requested variable name is found, the string is allocated and assigned to this pointer.</span></span> <span data-ttu-id="00733-114">Der Benutzer kann den Arbeitsspeicher, der der Zeichenfolge zugeordnet ist, verantwortungsvoll freigeben.</span><span class="sxs-lookup"><span data-stu-id="00733-114">It is the user's responsibly to free the memory associated with the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00733-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00733-115">Return value</span></span>

<span data-ttu-id="00733-116">Wenn die Funktion erfolgreich ist (wenn der Variablenname gefunden wurde und eine Zeichenfolge ungleich 0 (null) aufweist), ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="00733-116">If the function is successful (if the variable name was found and had a non-zero-length string), the return value is **TRUE**.</span></span>

<span data-ttu-id="00733-117">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="00733-117">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="00733-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00733-118">Requirements</span></span>



| <span data-ttu-id="00733-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00733-119">Requirement</span></span> | <span data-ttu-id="00733-120">Wert</span><span class="sxs-lookup"><span data-stu-id="00733-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00733-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00733-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00733-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00733-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="00733-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00733-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00733-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00733-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="00733-125">Header</span><span class="sxs-lookup"><span data-stu-id="00733-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00733-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="00733-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="00733-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="00733-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="00733-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00733-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="00733-129">DLL</span><span class="sxs-lookup"><span data-stu-id="00733-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00733-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00733-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




