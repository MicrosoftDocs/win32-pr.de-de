---
description: Gibt die Adresse einer Rückruffunktion für Verzögerungs Ladefehler für die angegebene DLL und den Prozess zurück.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: Delta loadfailurehook-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373737"
---
# <a name="delayloadfailurehook-function"></a><span data-ttu-id="8ada6-103">Delta loadfailurehook-Funktion</span><span class="sxs-lookup"><span data-stu-id="8ada6-103">DelayLoadFailureHook function</span></span>

<span data-ttu-id="8ada6-104">Gibt die Adresse einer Rückruffunktion für Verzögerungs Ladefehler für die angegebene DLL und den Prozess zurück.</span><span class="sxs-lookup"><span data-stu-id="8ada6-104">Returns the address of a delay-load failure callback function for the specified DLL and process.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ada6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ada6-105">Syntax</span></span>


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a><span data-ttu-id="8ada6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ada6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ada6-107">*pszdllname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ada6-107">*pszDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ada6-108">Der Name der dll.</span><span class="sxs-lookup"><span data-stu-id="8ada6-108">The name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="8ada6-109">*pszProcName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ada6-109">*pszProcName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ada6-110">Der Name des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="8ada6-110">The name of the process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ada6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ada6-111">Return value</span></span>

<span data-ttu-id="8ada6-112">Die Adresse der Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="8ada6-112">The address of the callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ada6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ada6-113">Requirements</span></span>



| <span data-ttu-id="8ada6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ada6-114">Requirement</span></span> | <span data-ttu-id="8ada6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8ada6-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ada6-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ada6-116">Library</span></span><br/> | <dl> <span data-ttu-id="8ada6-117"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ada6-117"><dt>Kernel32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ada6-118">DLL</span><span class="sxs-lookup"><span data-stu-id="8ada6-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="8ada6-119"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ada6-119"><dt>Kernel32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ada6-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ada6-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ada6-121">[Fehler Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span><span class="sxs-lookup"><span data-stu-id="8ada6-121">[Failure Hooks](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)</span></span>
</dt> </dl>

 

 




