---
description: Multipliziert erweiterte ganze Zahlen.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: Rtlextendebug-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351275"
---
# <a name="rtlextendedintegermultiply-function"></a><span data-ttu-id="3b1e1-103">Rtlextendebug-Funktion</span><span class="sxs-lookup"><span data-stu-id="3b1e1-103">RtlExtendedIntegerMultiply function</span></span>

<span data-ttu-id="3b1e1-104">\[Die **rtlextendedintegermultiplizieren** -Funktion wird exportiert, um vorhandene Treiber Binärdateien zu unterstützen, und ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b1e1-104">\[The **RtlExtendedIntegerMultiply** function is exported to support existing driver binaries and is obsolete.</span></span> <span data-ttu-id="3b1e1-105">Um eine bessere Leistung zu erzielen, verwenden Sie die Compilerunterstützung für ganzzahlige Vorgänge mit 64 Bit.\]</span><span class="sxs-lookup"><span data-stu-id="3b1e1-105">For better performance, use the compiler support for 64-bit integer operations.\]</span></span>

<span data-ttu-id="3b1e1-106">Multipliziert erweiterte ganze Zahlen.</span><span class="sxs-lookup"><span data-stu-id="3b1e1-106">Multiplies extended integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1e1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b1e1-107">Syntax</span></span>


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a><span data-ttu-id="3b1e1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b1e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b1e1-109">*Multiplicand* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b1e1-109">*Multiplicand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b1e1-110">Multiplikand.</span><span class="sxs-lookup"><span data-stu-id="3b1e1-110">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="3b1e1-111">*Multiplikator* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b1e1-111">*Multiplier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b1e1-112">Multiplikator.</span><span class="sxs-lookup"><span data-stu-id="3b1e1-112">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b1e1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b1e1-113">Return value</span></span>

<span data-ttu-id="3b1e1-114">Gibt Multiplikations Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="3b1e1-114">Returns multiplication result.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b1e1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b1e1-115">Remarks</span></span>

<span data-ttu-id="3b1e1-116">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3b1e1-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b1e1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b1e1-117">Requirements</span></span>



| <span data-ttu-id="3b1e1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b1e1-118">Requirement</span></span> | <span data-ttu-id="3b1e1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3b1e1-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1e1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3b1e1-120">DLL</span></span><br/> | <dl> <span data-ttu-id="3b1e1-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b1e1-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
