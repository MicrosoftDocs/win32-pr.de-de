---
description: Legt die Endpunkt Adresse fest, die zum Herstellen einer Verbindung mit einem Remote Modul verwendet wird.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ietertopeerengine:: setplaybackendpoint-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbec4826fb2659604a4b9f4388beed1829b42770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482406"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span data-ttu-id="e3b69-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>Ietertopeerengine:: setplaybackendpoint-Methode</span><span class="sxs-lookup"><span data-stu-id="e3b69-103"><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>IPeerToPeerEngine::SetPlaybackEndpoint method</span></span>

<span data-ttu-id="e3b69-104">Legt die Endpunkt Adresse fest, die zum Herstellen einer Verbindung mit einem Remote Modul verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3b69-104">Sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3b69-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="e3b69-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3b69-106">Parameters</span></span>

<span data-ttu-id="e3b69-107">*busauthentifizierung* </span><span class="sxs-lookup"><span data-stu-id="e3b69-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="e3b69-108">true, wenn Authentifizierung verwendet werden soll. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="e3b69-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="e3b69-109">*Dreher* </span><span class="sxs-lookup"><span data-stu-id="e3b69-109">*endpoint* </span></span>  
<span data-ttu-id="e3b69-110">Eine com-Zeichenfolge, die die Endpunkt Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="e3b69-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="e3b69-111">*SessionKey* </span><span class="sxs-lookup"><span data-stu-id="e3b69-111">*sessionKey* </span></span>  
<span data-ttu-id="e3b69-112">Eine com-Zeichenfolge, die den für die Verschlüsselung verwendeten Sitzungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="e3b69-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="e3b69-113">*Remoteversion* </span><span class="sxs-lookup"><span data-stu-id="e3b69-113">*remoteVersion* </span></span>  
<span data-ttu-id="e3b69-114">Gibt die Version der zu verwendenden Remote-Engine an.</span><span class="sxs-lookup"><span data-stu-id="e3b69-114">Specifies the version of the remote engine to use.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3b69-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3b69-115">Return value</span></span>

<span data-ttu-id="e3b69-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e3b69-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3b69-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e3b69-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b69-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3b69-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e3b69-119">Header</span><span class="sxs-lookup"><span data-stu-id="e3b69-119">Header</span></span></p></td><td><span data-ttu-id="e3b69-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e3b69-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e3b69-121"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3b69-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e3b69-122">**IPeer-topeerengine**</span><span class="sxs-lookup"><span data-stu-id="e3b69-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
