---
description: 'pSetupStringTableInitializeEx-Funktion: Initialisiert eine Zeichenfolgentabelle.'
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096648"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="3e742-103">pSetupStringTableInitializeEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="3e742-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="3e742-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3e742-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="3e742-105">Initialisiert eine Zeichenfolgentabelle.</span><span class="sxs-lookup"><span data-stu-id="3e742-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e742-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e742-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="3e742-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e742-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e742-108">*ExtraDataSize* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e742-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e742-109">Größe des zusätzlichen Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="3e742-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="3e742-110">*Reserviert* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3e742-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e742-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3e742-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e742-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e742-112">Remarks</span></span>

<span data-ttu-id="3e742-113">Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3e742-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e742-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e742-114">Requirements</span></span>



| <span data-ttu-id="3e742-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e742-115">Requirement</span></span> | <span data-ttu-id="3e742-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3e742-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e742-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3e742-117">DLL</span></span><br/> | <dl> <span data-ttu-id="3e742-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e742-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
