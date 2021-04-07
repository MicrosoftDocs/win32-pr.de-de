---
description: Legt asynchron die Endpunkt Adresse fest, die zum Herstellen einer Verbindung mit einer Remote-Engine verwendet wird.
MS-HAID: vspixengine.IPixEngine7\_SetPlaybackEndpointAsync\_BOOL\_BSTR\_BSTR\_RemotingVersion\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine7:: setplaybackendpointasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4F76EFFF-F3CB-4BEA-999F-639876C7F792
api_name:
- IPixEngine7.SetPlaybackEndpointAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2e0970b1a2a786c828a24efef0ae9e4057dbe2cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747385"
---
# <a name="span-idvspixengineipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dwordspanipixengine7setplaybackendpointasync-method"></a><span data-ttu-id="977f0-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7:: setplaybackendpointasync-Methode</span><span class="sxs-lookup"><span data-stu-id="977f0-103"><span id="vspixengine.ipixengine7_setplaybackendpointasync_bool_bstr_bstr_remotingversion_iversioncallback_ptr_dword_dword"></span>IPixEngine7::SetPlaybackEndpointAsync method</span></span>

<span data-ttu-id="977f0-104">Legt asynchron die Endpunkt Adresse fest, die zum Herstellen einer Verbindung mit einer Remote-Engine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="977f0-104">Asynchronously sets the endpoint address used to connect to a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="977f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="977f0-105">Syntax</span></span>


```C++
HRESULT SetPlaybackEndpointAsync(
   BOOL              bUseAuthentication,
   BSTR              endpoint,
   BSTR              sessionKey,
   RemotingVersion   remoteVersion,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="977f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="977f0-106">Parameters</span></span>

<span data-ttu-id="977f0-107">*busauthentifizierung* </span><span class="sxs-lookup"><span data-stu-id="977f0-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="977f0-108">true, wenn Authentifizierung verwendet werden soll. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="977f0-108">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="977f0-109">*Dreher* </span><span class="sxs-lookup"><span data-stu-id="977f0-109">*endpoint* </span></span>  
<span data-ttu-id="977f0-110">Eine com-Zeichenfolge, die die Endpunkt Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="977f0-110">A COM string containing the endpoint address.</span></span>

<span data-ttu-id="977f0-111">*SessionKey* </span><span class="sxs-lookup"><span data-stu-id="977f0-111">*sessionKey* </span></span>  
<span data-ttu-id="977f0-112">Eine com-Zeichenfolge, die den für die Verschlüsselung verwendeten Sitzungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="977f0-112">A COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="977f0-113">*Remoteversion* </span><span class="sxs-lookup"><span data-stu-id="977f0-113">*remoteVersion* </span></span>  
<span data-ttu-id="977f0-114">Gibt die Version der zu verwendenden Remote-Engine an.</span><span class="sxs-lookup"><span data-stu-id="977f0-114">Specifies the version of the remote engine to use.</span></span>

<span data-ttu-id="977f0-115">*versioncallback* </span><span class="sxs-lookup"><span data-stu-id="977f0-115">*versionCallback* </span></span>  
<span data-ttu-id="977f0-116">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="977f0-116">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="977f0-117">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="977f0-117">*requestCookie* </span></span>  
<span data-ttu-id="977f0-118">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="977f0-118">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="977f0-119">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="977f0-119">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="977f0-120">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="977f0-120">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="977f0-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="977f0-121">Return value</span></span>

<span data-ttu-id="977f0-122">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="977f0-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="977f0-123">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="977f0-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="977f0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="977f0-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="977f0-125">Header</span><span class="sxs-lookup"><span data-stu-id="977f0-125">Header</span></span></p></td><td><span data-ttu-id="977f0-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="977f0-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="977f0-127"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="977f0-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="977f0-128">**IPixEngine7**</span><span class="sxs-lookup"><span data-stu-id="977f0-128">**IPixEngine7**</span></span>](/windows/desktop/direct3dtools/ipixengine7)

 

 
