---
description: Die loadmacaddress-Funktion wird vom Monitor aufgerufen, um eine Mac-Adressliste mit Adressen auszufüllen, die aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen werden.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Loadmacadressen-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526768"
---
# <a name="loadmacaddresses-function"></a><span data-ttu-id="f444a-103">Loadmacadressen-Funktion</span><span class="sxs-lookup"><span data-stu-id="f444a-103">LoadMACAddresses function</span></span>

<span data-ttu-id="f444a-104">Die **loadmacaddress** -Funktion wird vom Monitor aufgerufen, um eine Mac-Adressliste mit Adressen auszufüllen, die aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="f444a-104">The **LoadMACAddresses** function is called by the monitor to fill in a MAC address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f444a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f444a-105">Syntax</span></span>


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="f444a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f444a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f444a-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f444a-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f444a-108">Zeiger auf die HTML-Konfigurations Zeichenfolge, die von der [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode an den Monitor übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f444a-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f444a-109">*pvarname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f444a-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f444a-110">Zeiger auf den Namen der Variablen in der Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f444a-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="f444a-111">*ppadressen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f444a-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f444a-112">Zeiger auf einen Zeiger auf ein Array von Adressen.</span><span class="sxs-lookup"><span data-stu-id="f444a-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="f444a-113">Wenn die in *pvarname* angegebene Variable gefunden wird und eine nicht-Null-Länge aufweist, ordnet die Funktion ausreichenden Speicherplatz zu (mithilfe von **heapzucmemory**) und speichert alle Mac-Adressen als Array.</span><span class="sxs-lookup"><span data-stu-id="f444a-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space (by using **HeapAllocMemory**) and stores all the MAC addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="f444a-114">*pnumadkleider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f444a-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f444a-115">Zeiger auf die **DWORD** -Variable, die auf die Anzahl der Mac-Adressen der Konfigurations Zeichenfolge festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f444a-115">Pointer to the **DWORD** variable that is set to the number of MAC addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f444a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f444a-116">Return value</span></span>

<span data-ttu-id="f444a-117">Wenn die Funktion erfolgreich ist, ist der Rückgabewert **true**, wenn der Variablenname gefunden wurde und eine Zeichenfolge ungleich 0 (null) aufweist, die Mac-Adressen darstellt).</span><span class="sxs-lookup"><span data-stu-id="f444a-117">If the function is successful, (the variable name was found and had a non-zero-length string that represented MAC addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="f444a-118">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="f444a-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f444a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f444a-119">Requirements</span></span>



| <span data-ttu-id="f444a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f444a-120">Requirement</span></span> | <span data-ttu-id="f444a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f444a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f444a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f444a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f444a-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f444a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f444a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f444a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f444a-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f444a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f444a-126">Header</span><span class="sxs-lookup"><span data-stu-id="f444a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f444a-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f444a-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f444a-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f444a-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f444a-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f444a-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f444a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f444a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f444a-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f444a-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




