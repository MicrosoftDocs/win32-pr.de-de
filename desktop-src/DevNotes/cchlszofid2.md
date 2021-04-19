---
description: Decodiert und speichert eine Zeichenfolge.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365587"
---
# <a name="cchlszofid2-function"></a><span data-ttu-id="7304f-103">CchLszOfId2-Funktion</span><span class="sxs-lookup"><span data-stu-id="7304f-103">CchLszOfId2 function</span></span>

<span data-ttu-id="7304f-104">Decodiert und speichert eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7304f-104">Decodes and stores a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7304f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7304f-105">Syntax</span></span>


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a><span data-ttu-id="7304f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7304f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7304f-107">*id*</span><span class="sxs-lookup"><span data-stu-id="7304f-107">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="7304f-108">Der Bezeichner der Zeichenfolge in der Ressourcen Datei, die decodiert und gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7304f-108">The identifier of the string in the resource file to be decoded and stored.</span></span> <span data-ttu-id="7304f-109">Die Gültigkeit der Zeichenfolge wird nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="7304f-109">The validity of the string is not verified.</span></span>

</dd> <dt>

<span data-ttu-id="7304f-110">*LSZ*</span><span class="sxs-lookup"><span data-stu-id="7304f-110">*lsz*</span></span> 
</dt> <dd>

<span data-ttu-id="7304f-111">Ein Zeiger auf einen Puffer mit einer Länge von *cbmax*.</span><span class="sxs-lookup"><span data-stu-id="7304f-111">A pointer to a buffer with a length of *cbmax*.</span></span> <span data-ttu-id="7304f-112">Zeichen folgen, die länger sind als *cbmax* , werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="7304f-112">Strings that are longer than *cbmax* are truncated.</span></span>

</dd> <dt>

<span data-ttu-id="7304f-113">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="7304f-113">*cbmax*</span></span> 
</dt> <dd>

<span data-ttu-id="7304f-114">Die maximale Länge der Zeichenfolge, die im *LSZ* -Parameter gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7304f-114">The maximum length of the string to be stored in the *lsz* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7304f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7304f-115">Return value</span></span>

<span data-ttu-id="7304f-116">Diese Funktion gibt die decodierte Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="7304f-116">This function returns the decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="7304f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7304f-117">Remarks</span></span>

<span data-ttu-id="7304f-118">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7304f-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7304f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7304f-119">Requirements</span></span>



| <span data-ttu-id="7304f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7304f-120">Requirement</span></span> | <span data-ttu-id="7304f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7304f-121">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7304f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7304f-122">DLL</span></span><br/> | <dl> <span data-ttu-id="7304f-123"><dt>Msjint40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7304f-123"><dt>Msjint40.dll</dt></span></span> </dl> |



 

 
