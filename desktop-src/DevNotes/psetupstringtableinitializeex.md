---
description: Initialisiert eine Zeichen folgen Tabelle.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: psetupstringtableinitializeex-Funktion
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
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373630"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="a4b1a-103">psetupstringtableinitializeex-Funktion</span><span class="sxs-lookup"><span data-stu-id="a4b1a-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="a4b1a-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a4b1a-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="a4b1a-105">Initialisiert eine Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b1a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4b1a-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="a4b1a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4b1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b1a-108">*Extradatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4b1a-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b1a-109">Größe des zusätzlichen Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="a4b1a-110">*Reserviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4b1a-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4b1a-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4b1a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4b1a-112">Remarks</span></span>

<span data-ttu-id="a4b1a-113">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a4b1a-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b1a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4b1a-114">Requirements</span></span>



| <span data-ttu-id="a4b1a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4b1a-115">Requirement</span></span> | <span data-ttu-id="a4b1a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a4b1a-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b1a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b1a-117">DLL</span></span><br/> | <dl> <span data-ttu-id="a4b1a-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b1a-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
