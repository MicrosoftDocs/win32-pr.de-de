---
description: Ruft den Datei Titel für den angegebenen Dateipfad ab.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: psetupgetfiletitle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358251"
---
# <a name="psetupgetfiletitle-function"></a><span data-ttu-id="9951b-103">psetupgetfiletitle-Funktion</span><span class="sxs-lookup"><span data-stu-id="9951b-103">pSetupGetFileTitle function</span></span>

<span data-ttu-id="9951b-104">\[Diese Funktion ist in Windows Vista oder Windows Server 2008 nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9951b-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="9951b-105">Ruft den Datei Titel für den angegebenen Dateipfad ab.</span><span class="sxs-lookup"><span data-stu-id="9951b-105">Retrieves the file title for the specified file path.</span></span>

## <a name="syntax"></a><span data-ttu-id="9951b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9951b-106">Syntax</span></span>


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a><span data-ttu-id="9951b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9951b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9951b-108">*FilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9951b-108">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9951b-109">Der Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="9951b-109">The file path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9951b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9951b-110">Return value</span></span>

<span data-ttu-id="9951b-111">Ein Zeiger auf eine Zeichenfolge, die den Datei Titel empfängt.</span><span class="sxs-lookup"><span data-stu-id="9951b-111">A pointer to string that receives the file title.</span></span>

## <a name="remarks"></a><span data-ttu-id="9951b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9951b-112">Remarks</span></span>

<span data-ttu-id="9951b-113">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9951b-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9951b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9951b-114">Requirements</span></span>



| <span data-ttu-id="9951b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9951b-115">Requirement</span></span> | <span data-ttu-id="9951b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9951b-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9951b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="9951b-117">DLL</span></span><br/> | <dl> <span data-ttu-id="9951b-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9951b-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
