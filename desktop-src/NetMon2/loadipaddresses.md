---
description: Die loadipaddress-Funktion wird vom Monitor aufgerufen, um eine IP-Adressliste mit Adressen auszufüllen, die aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen werden.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Loadipadressen-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362791"
---
# <a name="loadipaddresses-function"></a><span data-ttu-id="929b5-103">Loadipadressen-Funktion</span><span class="sxs-lookup"><span data-stu-id="929b5-103">LoadIPAddresses function</span></span>

<span data-ttu-id="929b5-104">Die **loadipaddress** -Funktion wird vom Monitor aufgerufen, um eine IP-Adressliste mit Adressen auszufüllen, die aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="929b5-104">The **LoadIPAddresses** function is called by the monitor to fill in an IP address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="929b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="929b5-105">Syntax</span></span>


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="929b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="929b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="929b5-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="929b5-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="929b5-108">Zeiger auf die HTML-Konfigurations Zeichenfolge, die von der [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode an den Monitor übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="929b5-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="929b5-109">*pvarname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="929b5-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="929b5-110">Zeiger auf den Namen der Variablen in der Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="929b5-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="929b5-111">*ppadressen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="929b5-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="929b5-112">Zeiger auf einen Zeiger auf ein Array von Adressen.</span><span class="sxs-lookup"><span data-stu-id="929b5-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="929b5-113">Wenn die in *pvarname* angegebene Variable gefunden wird und eine nicht-Null-Länge aufweist, ordnet die Funktion ausreichenden Speicherplatz zu und speichert alle IP-Adressen als Array.</span><span class="sxs-lookup"><span data-stu-id="929b5-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space and stores all the IP addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="929b5-114">*pnumadkleider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="929b5-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="929b5-115">Ein Zeiger auf die **DWORD** -Variable, die auf die Anzahl der IP-Adressen aus der Konfigurations Zeichenfolge festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="929b5-115">Pointer to the **DWORD** variable that is set to the number of IP addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="929b5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="929b5-116">Return value</span></span>

<span data-ttu-id="929b5-117">Wenn die Funktion erfolgreich ist (der Variablenname wurde gefunden, und eine Zeichenfolge mit einer Länge ungleich Null war, die IP-Adressen repräsentiert), ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="929b5-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IP addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="929b5-118">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="929b5-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="929b5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="929b5-119">Remarks</span></span>

<span data-ttu-id="929b5-120">Die IP-Adressen müssen das Format x. x. x. x aufweisen (z. b. 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="929b5-120">The IP addresses must be in x.x.x.x format (for example, 127.0.0.1).</span></span>

## <a name="requirements"></a><span data-ttu-id="929b5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="929b5-121">Requirements</span></span>



| <span data-ttu-id="929b5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="929b5-122">Requirement</span></span> | <span data-ttu-id="929b5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="929b5-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="929b5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="929b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="929b5-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="929b5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="929b5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="929b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="929b5-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="929b5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="929b5-128">Header</span><span class="sxs-lookup"><span data-stu-id="929b5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="929b5-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="929b5-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="929b5-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="929b5-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="929b5-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="929b5-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="929b5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="929b5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="929b5-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="929b5-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




