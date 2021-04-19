---
description: Behandelt System Farbänderungen für Anwendungen, die ctl3d verwenden.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Ctl3dColorChange-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361952"
---
# <a name="ctl3dcolorchange-function"></a><span data-ttu-id="360df-103">Ctl3dColorChange-Funktion</span><span class="sxs-lookup"><span data-stu-id="360df-103">Ctl3dColorChange function</span></span>

<span data-ttu-id="360df-104">Behandelt System Farbänderungen für Anwendungen, die ctl3d verwenden.</span><span class="sxs-lookup"><span data-stu-id="360df-104">Handles system color changes for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="360df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="360df-105">Syntax</span></span>


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a><span data-ttu-id="360df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="360df-106">Parameters</span></span>

<span data-ttu-id="360df-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="360df-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="360df-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="360df-108">Return value</span></span>

<span data-ttu-id="360df-109">Gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wurde. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="360df-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="360df-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="360df-110">Remarks</span></span>

<span data-ttu-id="360df-111">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="360df-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="360df-112">Diese Funktion sollte in der Hauptfenster Prozedur der Anwendung für die WM- **\_ syscolorchange** -Meldung aufgerufen werden, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="360df-112">This function should be called in the application's main window procedure for the **WM\_SYSCOLORCHANGE** message, as shown below.</span></span>

## <a name="examples"></a><span data-ttu-id="360df-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="360df-113">Examples</span></span>

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a><span data-ttu-id="360df-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="360df-114">Requirements</span></span>



| <span data-ttu-id="360df-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="360df-115">Requirement</span></span> | <span data-ttu-id="360df-116">Wert</span><span class="sxs-lookup"><span data-stu-id="360df-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="360df-117">DLL</span><span class="sxs-lookup"><span data-stu-id="360df-117">DLL</span></span><br/> | <dl> <span data-ttu-id="360df-118"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="360df-118"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
