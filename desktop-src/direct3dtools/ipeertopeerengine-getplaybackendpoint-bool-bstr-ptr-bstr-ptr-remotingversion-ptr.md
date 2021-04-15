---
description: Ruft die Endpunkt Adresse einer Remote-Engine ab.
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ietertopeerengine:: getplaybackendpoint-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6ee25dbd456086227e88fcb8bf7708a39e26eb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521144"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span data-ttu-id="0e8a6-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>Ietertopeerengine:: getplaybackendpoint-Methode</span><span class="sxs-lookup"><span data-stu-id="0e8a6-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint method</span></span>

<span data-ttu-id="0e8a6-104">Ruft die Endpunkt Adresse einer Remote-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="0e8a6-104">Gets the endpoint address of a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e8a6-105">Syntax</span></span>


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="0e8a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e8a6-106">Parameters</span></span>

<span data-ttu-id="0e8a6-107">*busauthentifizierung* </span><span class="sxs-lookup"><span data-stu-id="0e8a6-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="0e8a6-108">true, wenn die Remote-Engine die-Authentifizierung verwendet. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="0e8a6-108">true if the remote engine uses authentication; otherwise, false.</span></span>

<span data-ttu-id="0e8a6-109">*pdpoint* </span><span class="sxs-lookup"><span data-stu-id="0e8a6-109">*pEndpoint* </span></span>  
<span data-ttu-id="0e8a6-110">Bei Rückgabe eine com-Zeichenfolge, die die Endpunkt Adresse des Remote Wiedergabe Computers enthält.</span><span class="sxs-lookup"><span data-stu-id="0e8a6-110">On return, a COM string containing the endpoint address of the remote playback machine.</span></span>

<span data-ttu-id="0e8a6-111">*SessionKey* </span><span class="sxs-lookup"><span data-stu-id="0e8a6-111">*sessionKey* </span></span>  
<span data-ttu-id="0e8a6-112">Bei Rückgabe eine com-Zeichenfolge, die den für die Verschlüsselung verwendeten Sitzungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="0e8a6-112">On return, a COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="0e8a6-113">*premoteversion* </span><span class="sxs-lookup"><span data-stu-id="0e8a6-113">*pRemoteVersion* </span></span>  
<span data-ttu-id="0e8a6-114">Bei der Rückgabe die Version der Remote-Engine.</span><span class="sxs-lookup"><span data-stu-id="0e8a6-114">On return, the version of the remote engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e8a6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e8a6-115">Return value</span></span>

<span data-ttu-id="0e8a6-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e8a6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e8a6-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0e8a6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8a6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e8a6-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0e8a6-119">Header</span><span class="sxs-lookup"><span data-stu-id="0e8a6-119">Header</span></span></p></td><td><span data-ttu-id="0e8a6-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0e8a6-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0e8a6-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e8a6-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0e8a6-122">**IPeer-topeerengine**</span><span class="sxs-lookup"><span data-stu-id="0e8a6-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
