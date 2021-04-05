---
description: Fordern Sie ein Token für den Endpunkt des Diensts mit den angegebenen Anmelde Informationen an.
ms.assetid: 2CA0F826-9A05-4385-AF1A-A8C05B3DAFE2
title: 'Iupdateendpointauthprovider:: getendpointtoken-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetEndpointToken
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 55efe38ce9782b691e1ad32f7a21f6124e1f0bf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752080"
---
# <a name="iupdateendpointauthprovidergetendpointtoken-method"></a><span data-ttu-id="6b5d6-103">Iupdateendpointauthprovider:: getendpointtoken-Methode</span><span class="sxs-lookup"><span data-stu-id="6b5d6-103">IUpdateEndpointAuthProvider::GetEndpointToken method</span></span>

<span data-ttu-id="6b5d6-104">Fordern Sie ein Token für den Endpunkt des Diensts mit den angegebenen Anmelde Informationen an.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-104">Request a token for the endpoint of the service using the specified credentials.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b5d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b5d6-105">Syntax</span></span>


```C++
HRESULT GetEndpointToken(
  [in]  GUID                        serviceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  UpdateEndpointAuthTokenType tokenType,
  [in]  BOOL                        fRefreshOnline,
  [out] IUnknown                    **ppEndpointToken
);
```



## <a name="parameters"></a><span data-ttu-id="6b5d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b5d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b5d6-107">*serviceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5d6-108">Identifiziert den zu aktualisierenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="6b5d6-109">*EndpointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5d6-110">Identifiziert den Typ des Endpunkts, der vom Dienst implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-110">Identifies the type of endpoint that is implemented by the service.</span></span>

</dd> <dt>

<span data-ttu-id="6b5d6-111">*proxysettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-111">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5d6-112">Die Einstellungen, die beim Herstellen einer Verbindung mit einem Proxy Server verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-112">The settings to be used when connecting to a proxy server.</span></span> <span data-ttu-id="6b5d6-113">Weitere Informationen finden Sie in der [**updateendpointproxysettings**](updateendpointproxysettings.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-113">See the [**UpdateEndpointProxySettings**](updateendpointproxysettings.md) structure for more details.</span></span>

</dd> <dt>

<span data-ttu-id="6b5d6-114">*husertoken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-114">*hUserToken* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="6b5d6-115"> Verzeichnis \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-115">*tokenType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5d6-116">Identifiziert den Authentifizierungstyp, der für die Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-116">Identifies the type of authentication token that is used for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="6b5d6-117">*frefreshonline* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-117">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5d6-118">Gibt an, dass Wetter WUA ein neues Token anfordert.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-118">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="6b5d6-119">True gibt an, dass ein neues Token angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-119">True indicates that a new token is requested.</span></span> <span data-ttu-id="6b5d6-120">False gibt an, dass ein neues oder zwischengespeichertes Token angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-120">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="6b5d6-121">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-121">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="6b5d6-122">*ppendpointtoken* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-122">*ppEndpointToken* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b5d6-123">Geben Sie das zu verwendende Endpunkt Token an.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-123">Specifiy the endpoint token to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b5d6-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b5d6-124">Return value</span></span>

<span data-ttu-id="6b5d6-125">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-125">Returns S\_OK if successful.</span></span> <span data-ttu-id="6b5d6-126">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-126">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b5d6-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b5d6-127">Remarks</span></span>

<span data-ttu-id="6b5d6-128">WUA legt den Parameter "frefreshonline" in der Regel auf "false" fest, wenn diese Methode erstmals aufgerufen wird. Wenn ein Verbindungsfehler auftritt, legt WUA diesen Parameter auf "true" fest, wenn die Methode erneut aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-128">WUA typically sets the fRefreshOnline parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="6b5d6-129">Die Implementierung dieser Methode kann jedoch ein neues Token von einem Sicherheitstokendienst (Security Token Service, STS) anfordern oder jederzeit ein zwischengespeichertes Token bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6b5d6-129">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b5d6-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b5d6-130">Requirements</span></span>



| <span data-ttu-id="6b5d6-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b5d6-131">Requirement</span></span> | <span data-ttu-id="6b5d6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6b5d6-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b5d6-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b5d6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6b5d6-134">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="6b5d6-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b5d6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6b5d6-136">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b5d6-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="6b5d6-137">Header</span><span class="sxs-lookup"><span data-stu-id="6b5d6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b5d6-138"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b5d6-138"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b5d6-139">IDL</span><span class="sxs-lookup"><span data-stu-id="6b5d6-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b5d6-140"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b5d6-140"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="6b5d6-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b5d6-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b5d6-142"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b5d6-142"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b5d6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6b5d6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b5d6-144"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b5d6-144"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b5d6-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b5d6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b5d6-146">**Iupdateendpointauthprovider**</span><span class="sxs-lookup"><span data-stu-id="6b5d6-146">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> </dl>

 

 




