---
description: Die loadipxaddress-Funktion wird vom Monitor aufgerufen, um eine von einer HTML-Konfigurations Zeichenfolgen-Variable ergriffene IPX-Adressliste auszufüllen.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Loadipxadressen-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217798"
---
# <a name="loadipxaddresses-function"></a><span data-ttu-id="b4f1a-103">Loadipxadressen-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4f1a-103">LoadIPXAddresses function</span></span>

<span data-ttu-id="b4f1a-104">Die **loadipxaddress** -Funktion wird vom Monitor aufgerufen, um eine von einer HTML-Konfigurations Zeichenfolgen-Variable ergriffene IPX-Adressliste auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="b4f1a-104">The **LoadIPXAddresses** function is called by the monitor to fill in an IPX address list taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4f1a-105">Syntax</span></span>


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="b4f1a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4f1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f1a-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4f1a-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f1a-108">Zeiger auf die HTML-Konfigurations Zeichenfolge, die von der [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode an den Monitor übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="b4f1a-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b4f1a-109">*pvarname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4f1a-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f1a-110">Zeiger auf den Namen der Variablen in der Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b4f1a-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="b4f1a-111">*ppadressen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b4f1a-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f1a-112">Zeiger auf einen Zeiger auf ein Array von Adressen.</span><span class="sxs-lookup"><span data-stu-id="b4f1a-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="b4f1a-113">Wenn die in *pvarname* angegebene Variable gefunden wird und eine nicht-Null-Länge aufweist, wird genügend Speicherplatz zugewiesen (mithilfe von **heapzucmemory**), und alle IPX-Adressen werden als Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b4f1a-113">If the variable specified in *pVarName* is found and has a non-zero-length, sufficient space is allocated (by using **HeapAllocMemory**), and all the IPX addresses are stored as an array.</span></span>

</dd> <dt>

<span data-ttu-id="b4f1a-114">*pnumadkleider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b4f1a-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f1a-115">Ein Zeiger auf die **DWORD** -Variable, die auf die Anzahl der von der Konfigurations Zeichenfolge abgelegten IPX-Adressen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b4f1a-115">Pointer to the **DWORD** variable that is set to the number of IPX addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f1a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4f1a-116">Return value</span></span>

<span data-ttu-id="b4f1a-117">Wenn die Funktion erfolgreich ist (der Variablenname wurde gefunden, und eine Zeichenfolge mit einer Länge ungleich Null war, die IPX-Adressen repräsentiert), ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="b4f1a-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IPX addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="b4f1a-118">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="b4f1a-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f1a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4f1a-119">Requirements</span></span>



| <span data-ttu-id="b4f1a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4f1a-120">Requirement</span></span> | <span data-ttu-id="b4f1a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b4f1a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f1a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4f1a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f1a-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4f1a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b4f1a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4f1a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f1a-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4f1a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b4f1a-126">Header</span><span class="sxs-lookup"><span data-stu-id="b4f1a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4f1a-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4f1a-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b4f1a-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4f1a-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4f1a-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4f1a-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4f1a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b4f1a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4f1a-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4f1a-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




