---
description: Legt den aktuellen Wiedergabe Computer für das angegebene Grafik Protokoll fest.
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2:: setplaybackmachine-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d7366da4aa999828309136900edfe725af4f622
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522715"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span data-ttu-id="9a91b-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2:: setplaybackmachine-Methode</span><span class="sxs-lookup"><span data-stu-id="9a91b-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2::SetPlaybackMachine method</span></span>

<span data-ttu-id="9a91b-104">Legt den aktuellen Wiedergabe Computer für das angegebene Grafik Protokoll fest.</span><span class="sxs-lookup"><span data-stu-id="9a91b-104">Sets the current playback machine for the specified graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a91b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a91b-105">Syntax</span></span>


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a><span data-ttu-id="9a91b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a91b-106">Parameters</span></span>

<span data-ttu-id="9a91b-107">*Protokolldatei* </span><span class="sxs-lookup"><span data-stu-id="9a91b-107">*logFile* </span></span>  
<span data-ttu-id="9a91b-108">Eine com-Zeichenfolge, die den Namen des Grafik Protokolls zusammenhängt.</span><span class="sxs-lookup"><span data-stu-id="9a91b-108">A COM string contianing the name of the graphics log.</span></span>

<span data-ttu-id="9a91b-109">*busauthentifizierung* </span><span class="sxs-lookup"><span data-stu-id="9a91b-109">*bUseAuthentication* </span></span>  
<span data-ttu-id="9a91b-110">true, wenn Authentifizierung verwendet werden soll. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="9a91b-110">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="9a91b-111">*Computer* </span><span class="sxs-lookup"><span data-stu-id="9a91b-111">*machine* </span></span>  
<span data-ttu-id="9a91b-112">Eine com-Zeichenfolge, die den Namen des Wiedergabe Computers enthält.</span><span class="sxs-lookup"><span data-stu-id="9a91b-112">A COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a91b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a91b-113">Return value</span></span>

<span data-ttu-id="9a91b-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a91b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a91b-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9a91b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a91b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a91b-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9a91b-117">Header</span><span class="sxs-lookup"><span data-stu-id="9a91b-117">Header</span></span></p></td><td><span data-ttu-id="9a91b-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9a91b-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9a91b-119"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a91b-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9a91b-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="9a91b-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
