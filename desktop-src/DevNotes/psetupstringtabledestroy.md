---
description: Löscht eine Zeichen folgen Tabelle.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: psetupstringtabledestroy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364822"
---
# <a name="psetupstringtabledestroy-function"></a><span data-ttu-id="ea16e-103">psetupstringtabledestroy-Funktion</span><span class="sxs-lookup"><span data-stu-id="ea16e-103">pSetupStringTableDestroy function</span></span>

<span data-ttu-id="ea16e-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="ea16e-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="ea16e-105">Löscht eine Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ea16e-105">Deletes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea16e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea16e-106">Syntax</span></span>


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a><span data-ttu-id="ea16e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea16e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea16e-108">*STRINGTABLE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea16e-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea16e-109">Ein Zeiger auf die Zeichen folgen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ea16e-109">A pointer to the string table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea16e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea16e-110">Return value</span></span>

<span data-ttu-id="ea16e-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ea16e-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea16e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea16e-112">Remarks</span></span>

<span data-ttu-id="ea16e-113">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ea16e-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea16e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea16e-114">Requirements</span></span>



| <span data-ttu-id="ea16e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea16e-115">Requirement</span></span> | <span data-ttu-id="ea16e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ea16e-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea16e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ea16e-117">DLL</span></span><br/> | <dl> <span data-ttu-id="ea16e-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea16e-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
