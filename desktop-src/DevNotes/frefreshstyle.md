---
description: Lädt Farbeinstellungen aus der Registrierung neu.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: Frefreshstyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357661"
---
# <a name="frefreshstyle-function"></a><span data-ttu-id="7c595-103">Frefreshstyle-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c595-103">FRefreshStyle function</span></span>

<span data-ttu-id="7c595-104">Lädt Farbeinstellungen aus der Registrierung neu.</span><span class="sxs-lookup"><span data-stu-id="7c595-104">Reloads color settings from registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c595-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c595-105">Syntax</span></span>


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a><span data-ttu-id="7c595-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c595-106">Parameters</span></span>

<span data-ttu-id="7c595-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7c595-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c595-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c595-108">Return value</span></span>

<span data-ttu-id="7c595-109">Gibt bei Erfolg TRUE zurück. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="7c595-109">Returns TRUE on success; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c595-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c595-110">Remarks</span></span>

<span data-ttu-id="7c595-111">Diese Funktion ist keiner Import Bibliothek oder Header Datei zugeordnet. Es muss mithilfe der [**LoadLibrary**](-loadlibrary.md) -Funktion und der [**GetProcAddress**](-getprocaddress-.md) -Funktion aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7c595-111">This function is not associated with an import library or header file; it must be called using the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c595-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c595-112">Requirements</span></span>



| <span data-ttu-id="7c595-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c595-113">Requirement</span></span> | <span data-ttu-id="7c595-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7c595-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c595-115">DLL</span><span class="sxs-lookup"><span data-stu-id="7c595-115">DLL</span></span><br/> | <dl> <span data-ttu-id="7c595-116"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c595-116"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c595-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c595-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c595-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="7c595-118">**GetProcAddress**</span></span>](-getprocaddress-.md)
</dt> <dt>

[<span data-ttu-id="7c595-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="7c595-119">**LoadLibrary**</span></span>](-loadlibrary.md)
</dt> </dl>

 

 




