---
description: Eine Anforderung zum Senden von debugsymbolpfaden an die lokale Engine (nicht Remote).
MS-HAID: vspixengine.ISymbolSettings\_UpdateSymbolSettings\_SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Isymbolsettings:: updatesymbolsettings-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E48E509F-8C33-49D6-B799-B16F70C1AA64
api_name:
- ISymbolSettings.UpdateSymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c60ceacbf8d11f951896979862dad6520c32837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344775"
---
# <a name="span-idvspixengineisymbolsettings_updatesymbolsettings_symbolserverinfospanisymbolsettingsupdatesymbolsettings-method"></a><span data-ttu-id="85e53-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>Isymbolsettings:: updatesymbolsettings-Methode</span><span class="sxs-lookup"><span data-stu-id="85e53-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings::UpdateSymbolSettings method</span></span>

<span data-ttu-id="85e53-104">Eine Anforderung zum Senden von debugsymbolpfaden an die lokale Engine (nicht Remote).</span><span class="sxs-lookup"><span data-stu-id="85e53-104">A request to send debug symbol paths to the local (non-remote) engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e53-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85e53-105">Syntax</span></span>


```C++
HRESULT UpdateSymbolSettings(
   SymbolServerInfo symbolServerInfo
);
```

## <a name="parameters"></a><span data-ttu-id="85e53-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85e53-106">Parameters</span></span>

<span data-ttu-id="85e53-107">*symbolserverinfo* </span><span class="sxs-lookup"><span data-stu-id="85e53-107">*symbolServerInfo* </span></span>  
<span data-ttu-id="85e53-108">Debuggen von Symbol Serverpfad-Informationen.</span><span class="sxs-lookup"><span data-stu-id="85e53-108">Debug symbol server path information.</span></span>

## <a name="return-value"></a><span data-ttu-id="85e53-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85e53-109">Return value</span></span>

<span data-ttu-id="85e53-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="85e53-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85e53-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85e53-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="85e53-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85e53-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="85e53-113">Header</span><span class="sxs-lookup"><span data-stu-id="85e53-113">Header</span></span></p></td><td><span data-ttu-id="85e53-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="85e53-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="85e53-115"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85e53-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="85e53-116">**Isymbolsettings**</span><span class="sxs-lookup"><span data-stu-id="85e53-116">**ISymbolSettings**</span></span>](/windows/desktop/direct3dtools/isymbolsettings)

 

 
