---
description: Ruft die GetLastError-Funktion auf und konvertiert den Rückgabecode in ein HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: Signerror-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041793"
---
# <a name="signerror-function"></a><span data-ttu-id="30cb6-103">Signerror-Funktion</span><span class="sxs-lookup"><span data-stu-id="30cb6-103">SignError function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30cb6-104">Diese API ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="30cb6-104">This API is deprecated.</span></span> <span data-ttu-id="30cb6-105">Microsoft kann diese API in zukünftigen Versionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="30cb6-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="30cb6-106">Die **signerror** -Funktion Ruft die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion auf und konvertiert den Rückgabecode in ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="30cb6-106">The **SignError** function calls the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and converts the return code to an **HRESULT**.</span></span>

> [!Note]  
> <span data-ttu-id="30cb6-107">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="30cb6-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="30cb6-108">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="30cb6-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="30cb6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="30cb6-109">Syntax</span></span>


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a><span data-ttu-id="30cb6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="30cb6-110">Parameters</span></span>

<span data-ttu-id="30cb6-111">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="30cb6-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30cb6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30cb6-112">Return value</span></span>

<span data-ttu-id="30cb6-113">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="30cb6-113">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="30cb6-114">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="30cb6-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="30cb6-115">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="30cb6-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30cb6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30cb6-116">Requirements</span></span>



| <span data-ttu-id="30cb6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30cb6-117">Requirement</span></span> | <span data-ttu-id="30cb6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="30cb6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30cb6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30cb6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="30cb6-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30cb6-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30cb6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30cb6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="30cb6-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30cb6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30cb6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="30cb6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30cb6-124"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30cb6-124"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
