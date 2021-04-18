---
description: Gibt den bevorzugten Authentifizierungstyp für den Endpunkt des Diensts zurück.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'Iupdateendpointauthprovider:: getpreferredendpointdekentype-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214733"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a><span data-ttu-id="dec04-103">Iupdateendpointauthprovider:: getpreferredendpointdekentype-Methode</span><span class="sxs-lookup"><span data-stu-id="dec04-103">IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType method</span></span>

<span data-ttu-id="dec04-104">Gibt den bevorzugten Authentifizierungstyp für den Endpunkt des Diensts zurück.</span><span class="sxs-lookup"><span data-stu-id="dec04-104">Returns the preferred type of authentication token for the endpoint of the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec04-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dec04-105">Syntax</span></span>


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a><span data-ttu-id="dec04-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dec04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec04-107">*serviceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dec04-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec04-108">Identifiziert den zu aktualisierenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="dec04-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="dec04-109">*EndpointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dec04-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec04-110">Identifiziert den Typ des Endpunkts, der zum Herstellen einer Verbindung mit dem Dienst erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="dec04-110">Identifies the type of endpoint tneeded to connect to the service.</span></span>

</dd> <dt>

<span data-ttu-id="dec04-111">*ulrequestedtypes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dec04-111">*ulRequestedTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec04-112">Identifiziert den ORed-Satz von Token, die vom Endpunkt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dec04-112">Identifies the ORed set of tokens that are supported by the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="dec04-113">*pulpreferredykentypes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dec04-113">*pulPreferredTokenTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dec04-114">Geben Sie den bevorzugten Satz an authentifizierungstokentypen an.</span><span class="sxs-lookup"><span data-stu-id="dec04-114">Specify the ORed set of authentication token types that are preferred.</span></span> <span data-ttu-id="dec04-115">(Auf 0 festgelegt, um anzugeben, dass kein Authentifizierungs Token erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="dec04-115">(Set to 0 to indicate that no authentication token is needed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec04-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dec04-116">Return value</span></span>

<span data-ttu-id="dec04-117">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dec04-117">Returns S\_OK if successful.</span></span> <span data-ttu-id="dec04-118">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dec04-118">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec04-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dec04-119">Remarks</span></span>

<span data-ttu-id="dec04-120">Wenn diese Methode zurückgegeben wird, wählt WUA einen Tokentyp aus den bevorzugten Typen aus und übergibt ihn an den TokenType-Parameter der [**getendpointtoken**](iupdateendpointauthprovider-getendpointtoken.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dec04-120">When this method is returned, WUA chooses a token type from the preferred types and passes it to the tokenType parameter of the [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec04-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dec04-121">Requirements</span></span>



| <span data-ttu-id="dec04-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dec04-122">Requirement</span></span> | <span data-ttu-id="dec04-123">Wert</span><span class="sxs-lookup"><span data-stu-id="dec04-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec04-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dec04-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dec04-125">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dec04-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="dec04-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dec04-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dec04-127">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dec04-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="dec04-128">Header</span><span class="sxs-lookup"><span data-stu-id="dec04-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec04-129"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="dec04-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="dec04-130">IDL</span><span class="sxs-lookup"><span data-stu-id="dec04-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dec04-131"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dec04-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="dec04-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dec04-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="dec04-133"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dec04-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="dec04-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dec04-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec04-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec04-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec04-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dec04-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec04-137">**Iupdateendpointauthprovider**</span><span class="sxs-lookup"><span data-stu-id="dec04-137">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> <dt>

[<span data-ttu-id="dec04-138">**Getendpointtoken**</span><span class="sxs-lookup"><span data-stu-id="dec04-138">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




