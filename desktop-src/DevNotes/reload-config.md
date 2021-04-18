---
description: Lädt eine IME-Konfiguration erneut aus der HKCU-Registrierung in japanischer IME.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: reload_config-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354785"
---
# <a name="reload_config-function"></a><span data-ttu-id="3a1b8-103">config-Funktion erneut laden \_</span><span class="sxs-lookup"><span data-stu-id="3a1b8-103">reload\_config function</span></span>

<span data-ttu-id="3a1b8-104">Lädt eine IME-Konfiguration erneut aus der HKCU-Registrierung in japanischer IME.</span><span class="sxs-lookup"><span data-stu-id="3a1b8-104">Reloads an IME configuration from the HKCU registry, in Japanese IME only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a1b8-105">Syntax</span></span>


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a><span data-ttu-id="3a1b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a1b8-106">Parameters</span></span>

<span data-ttu-id="3a1b8-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3a1b8-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a1b8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a1b8-108">Return value</span></span>

<span data-ttu-id="3a1b8-109">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3a1b8-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a1b8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a1b8-110">Remarks</span></span>

<span data-ttu-id="3a1b8-111">Wenn in HKCU kein Registrierungs Wert vorhanden ist, schreibt die Funktion zum erneuten **Laden \_** von Daten in die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="3a1b8-111">If no registry value is present in HKCU, the **reload\_config** function writes initial data to the registry.</span></span>

<span data-ttu-id="3a1b8-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3a1b8-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1b8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a1b8-113">Requirements</span></span>



| <span data-ttu-id="3a1b8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a1b8-114">Requirement</span></span> | <span data-ttu-id="3a1b8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3a1b8-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1b8-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3a1b8-116">DLL</span></span><br/> | <dl> <span data-ttu-id="3a1b8-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a1b8-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span></span> </dl> |



 

 
