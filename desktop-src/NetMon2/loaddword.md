---
description: Die loaddword-Funktion wird vom Monitor aufgerufen, um eine DWORD-Variable mit einem Wert festzulegen, der aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen wurde.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Loaddword-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362734"
---
# <a name="loaddword-function"></a><span data-ttu-id="005de-103">Loaddword-Funktion</span><span class="sxs-lookup"><span data-stu-id="005de-103">LoadDWORD function</span></span>

<span data-ttu-id="005de-104">Die **loaddword** -Funktion wird vom Monitor aufgerufen, um eine **DWORD** -Variable mit einem Wert festzulegen, der aus einer HTML-Konfigurations Zeichenfolgen-Variablen entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="005de-104">The **LoadDWORD** function is called by the monitor to set a **DWORD** variable with a value taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="005de-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="005de-105">Syntax</span></span>


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="005de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="005de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="005de-107">*pConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="005de-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005de-108">Zeiger auf die HTML-Konfigurations Zeichenfolge, die von der [Imonitor::D oconfigure](imonitor-doconfigure.md) -Methode an den Monitor übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="005de-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="005de-109">*pvarname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="005de-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005de-110">Zeiger auf den Namen der Variablen in der Konfigurations Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="005de-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="005de-111">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="005de-111">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005de-112">Ein Zeiger auf die **DWORD** -Variable, die auf den Wert der Konfigurations Zeichen folgen Variablen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="005de-112">Pointer to the **DWORD** variable that is set to the value of the configuration string variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="005de-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="005de-113">Return value</span></span>

<span data-ttu-id="005de-114">Wenn die Funktion erfolgreich ist (wenn der Variablenname gefunden wurde und eine Zeichenfolge ungleich 0 (null) aufweist), wird das **DWORD** eingefügt, und der Rückgabewert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="005de-114">If the function is successful (if the variable name was found and had a non-zero-length string), the **DWORD** is inserted, and the return value is **TRUE**.</span></span>

<span data-ttu-id="005de-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="005de-115">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="005de-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="005de-116">Requirements</span></span>



| <span data-ttu-id="005de-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="005de-117">Requirement</span></span> | <span data-ttu-id="005de-118">Wert</span><span class="sxs-lookup"><span data-stu-id="005de-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="005de-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="005de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="005de-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="005de-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="005de-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="005de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="005de-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="005de-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="005de-123">Header</span><span class="sxs-lookup"><span data-stu-id="005de-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="005de-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="005de-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="005de-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="005de-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="005de-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="005de-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="005de-127">DLL</span><span class="sxs-lookup"><span data-stu-id="005de-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="005de-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="005de-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




