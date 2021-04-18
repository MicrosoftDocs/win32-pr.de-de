---
description: Gibt Java-Klassen Lade Programme frei, die möglicherweise beim Durchsuchen der Applets genutzt wurden.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: Notifybrowsershutdown-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351313"
---
# <a name="notifybrowsershutdown-function"></a><span data-ttu-id="8599a-103">Notifybrowsershutdown-Funktion</span><span class="sxs-lookup"><span data-stu-id="8599a-103">NotifyBrowserShutdown function</span></span>

<span data-ttu-id="8599a-104">Gibt Java-Klassen Lade Programme frei, die möglicherweise beim Durchsuchen der Applets genutzt wurden.</span><span class="sxs-lookup"><span data-stu-id="8599a-104">Frees Java class loaders that may have been consumed while browsing the applets.</span></span>

## <a name="syntax"></a><span data-ttu-id="8599a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8599a-105">Syntax</span></span>


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="8599a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8599a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8599a-107">*lpvreserved*</span><span class="sxs-lookup"><span data-stu-id="8599a-107">*lpvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="8599a-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8599a-108">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8599a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8599a-109">Return value</span></span>

<span data-ttu-id="8599a-110">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8599a-110">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="8599a-111">Andernfalls ist der Rückgabewert ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8599a-111">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8599a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8599a-112">Remarks</span></span>

<span data-ttu-id="8599a-113">Wenn die Anzahl der Browserfenster im integrierten Webmodus Null erreicht, gibt diese Funktion die Java-Klassen Lade Programme frei.</span><span class="sxs-lookup"><span data-stu-id="8599a-113">When the count of browser windows reaches zero in integrated Web mode, this function frees the Java class loaders.</span></span> <span data-ttu-id="8599a-114">Wenn der Benutzer das Durchsuchen von Applets erneut startet, lädt die Java-VM die neuesten Klassendateien herunter.</span><span class="sxs-lookup"><span data-stu-id="8599a-114">When the user starts browsing applets again, the Java VM will download the latest class files.</span></span>

<span data-ttu-id="8599a-115">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8599a-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8599a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8599a-116">Requirements</span></span>



| <span data-ttu-id="8599a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8599a-117">Requirement</span></span> | <span data-ttu-id="8599a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8599a-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8599a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8599a-119">DLL</span></span><br/> | <dl> <span data-ttu-id="8599a-120"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8599a-120"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
