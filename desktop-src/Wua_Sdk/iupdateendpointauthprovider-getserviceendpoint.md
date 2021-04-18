---
description: Fordert einen Endpunkt an, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'Iupdateendpointprovider:: getserviceendpoint-Methode (updateendpointauth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347792"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a><span data-ttu-id="69663-103">Iupdateendpointprovider:: getserviceendpoint-Methode</span><span class="sxs-lookup"><span data-stu-id="69663-103">IUpdateEndpointProvider::GetServiceEndpoint method</span></span>

<span data-ttu-id="69663-104">Fordert einen Endpunkt an, der zum Herstellen einer Verbindung mit einem Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69663-104">Requests an endpoint that is used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="69663-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69663-105">Syntax</span></span>


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a><span data-ttu-id="69663-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69663-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69663-107">*Serviceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69663-107">*ServiceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69663-108">Identifiziert den zu aktualisierenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="69663-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="69663-109">*EndpointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69663-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69663-110">Identifiziert den Typ des Endpunkts, der vom Dienst implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="69663-110">Identifies the type of endpoint implemented by the service.</span></span>

<span data-ttu-id="69663-111">Die [**updateendpointtype**](updateendpointtype.md) -Enumeration definiert die folgenden Konstanten.</span><span class="sxs-lookup"><span data-stu-id="69663-111">The [**UpdateEndpointType**](updateendpointtype.md) enumeration defines the following constants.</span></span>

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span data-ttu-id="69663-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetclientserver**</span><span class="sxs-lookup"><span data-stu-id="69663-112"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>


</dt> <dd>

<span data-ttu-id="69663-113">Ein Client/Server-Endpunkt, der zum Herstellen der Verbindung mit dem Aktualisierungs Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69663-113">A client-server endpoint that is used to connect to the update service.</span></span>

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span data-ttu-id="69663-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetreporting**</span><span class="sxs-lookup"><span data-stu-id="69663-114"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>


</dt> <dd>

<span data-ttu-id="69663-115">Ein Berichterstattungs Endpunkt, der verwendet wird, wenn der Client die Ergebnisse von Scans, Downloads und Installationen zurück an den Aktualisierungs Dienst meldet</span><span class="sxs-lookup"><span data-stu-id="69663-115">A Reporting endpoint that is used used when the client reports the results of scans, downloads, and installs back to the update service</span></span>

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span data-ttu-id="69663-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetwuaselfupdate**</span><span class="sxs-lookup"><span data-stu-id="69663-116"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>


</dt> <dd>

<span data-ttu-id="69663-117">Ein Self-Update Endpunkt, der verwendet wird, wenn der Client Computer einen Update Dienst kontaktiert, um festzustellen, ob eine neue Version der Windows Update Agent-Client Software vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="69663-117">A Self-Update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span data-ttu-id="69663-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetregulations**</span><span class="sxs-lookup"><span data-stu-id="69663-118"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>


</dt> <dd>

<span data-ttu-id="69663-119">Ein-Regel Endpunkt, der verwendet wird, wenn der Client Computer eine Verbindung mit dem-Verwaltungs Endpunkt hergestellt hat, um ein bestimmtes Update zu ergreifen, das auf den Zielcomputer anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="69663-119">A Regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span data-ttu-id="69663-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetsimpletargeting**</span><span class="sxs-lookup"><span data-stu-id="69663-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>


</dt> <dd>

<span data-ttu-id="69663-121">Ein Simple-Targeting endoint, das nur mit privaten Diensten (WSUS-Server in Unternehmensumgebungen) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69663-121">A Simple-Targeting endoint that is used only with private services (WSUS servers in corporate environments).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="69663-122">*proxysettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69663-122">*proxySettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69663-123">Gibt die Einstellungen an, die beim Herstellen einer Verbindung mit einem Proxy Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69663-123">Identifies the settings that are used when connecting to a proxy server.</span></span>

</dd> <dt>

<span data-ttu-id="69663-124">*husertoken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69663-124">*hUserToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69663-125">Enthält ein Tokenhandle-Objekt, das den Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="69663-125">Contains a token handle object that represents the user.</span></span> <span data-ttu-id="69663-126">Der Endpunkt Anbieter verwendet dieses Token, um zu bestimmen, welche Proxy Einstellungen und Anmelde Informationen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69663-126">The endpoint provider uses this token to determine which proxy settings and credentials to use.</span></span>

</dd> <dt>

<span data-ttu-id="69663-127">*frefreshonline* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69663-127">*fRefreshOnline* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69663-128">Gibt an, dass Wetter WUA ein neues Token anfordert.</span><span class="sxs-lookup"><span data-stu-id="69663-128">Indicates weather WUA requests a new token.</span></span> <span data-ttu-id="69663-129">True gibt an, dass ein neues Token angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="69663-129">True indicates that a new token is requested.</span></span> <span data-ttu-id="69663-130">False gibt an, dass ein neues oder zwischengespeichertes Token angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="69663-130">False indicates that a new or cached token is requested.</span></span> <span data-ttu-id="69663-131">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="69663-131">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="69663-132">*pbstrauendpointloc* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="69663-132">*pbstrEndpointLoc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69663-133">Geben Sie die URL an, die zur Kommunikation mit dem Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69663-133">Specify the URL used to communicate with the service.</span></span> <span data-ttu-id="69663-134">Für einen Cleint-Server-Endpunkt wäre dies z. b. die URL zum Client Server Dienst.</span><span class="sxs-lookup"><span data-stu-id="69663-134">For example, for a cleint-server endpoint this would be the URL to the client server service.</span></span> <span data-ttu-id="69663-135">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="69663-135">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69663-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69663-136">Return value</span></span>

<span data-ttu-id="69663-137">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="69663-137">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="69663-138">Andernfalls wird ein com-oder Windows-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="69663-138">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="69663-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69663-139">Remarks</span></span>

<span data-ttu-id="69663-140">WUA legt den Parameter " *frefreshonline* " in der Regel auf "false" fest, wenn diese Methode erstmals aufgerufen wird. Wenn ein Verbindungsfehler auftritt, legt WUA diesen Parameter auf "true" fest, wenn die Methode erneut aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="69663-140">WUA typically sets the *fRefreshOnline* parameter to false when this method is first called, then if a connection error occures WUA sets that parameter to true when the method is called again.</span></span> <span data-ttu-id="69663-141">Die Implementierung dieser Methode kann jedoch ein neues Token von einem Sicherheitstokendienst (Security Token Service, STS) anfordern oder jederzeit ein zwischengespeichertes Token bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69663-141">However, the implementation of this method can request a new token from a Security Token Service (STS) or provide a cached token at any time.</span></span>

<span data-ttu-id="69663-142">Wenn für den Endpunkt keine Authentifizierung erforderlich ist, kann der Aufrufer nur mit der URL, die vom *pbstrauendpointloc* -Parameter angegeben wird, eine Verbindung mit dem Dienst herstellen.</span><span class="sxs-lookup"><span data-stu-id="69663-142">If the endpoint does not need authentication, then the caller can connect to the service using only the URL specified by the *pbstrEndpointLoc* parameter.</span></span>

<span data-ttu-id="69663-143">Wenn für den Endpunkt eine Authentifizierung erforderlich ist, kann der Aufrufer die vom *pbstrinendpointloc* -Parameter angegebene URL und die von den anderen Parametern bereitgestellten Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="69663-143">If the endpoint does need authentication, then the caller can use the URL specified by the *pbstrEndpointLoc* parameter and the data provided by the other parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="69663-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69663-144">Requirements</span></span>



| <span data-ttu-id="69663-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69663-145">Requirement</span></span> | <span data-ttu-id="69663-146">Wert</span><span class="sxs-lookup"><span data-stu-id="69663-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69663-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69663-147">Minimum supported client</span></span><br/> | <span data-ttu-id="69663-148">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69663-148">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="69663-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69663-149">Minimum supported server</span></span><br/> | <span data-ttu-id="69663-150">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69663-150">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="69663-151">Header</span><span class="sxs-lookup"><span data-stu-id="69663-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="69663-152"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="69663-152"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="69663-153">IDL</span><span class="sxs-lookup"><span data-stu-id="69663-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="69663-154"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="69663-154"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="69663-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="69663-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="69663-156"><dt>Updateendpointauth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69663-156"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="69663-157">DLL</span><span class="sxs-lookup"><span data-stu-id="69663-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69663-158"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69663-158"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69663-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69663-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69663-160">**Iupdateendpointprovider**</span><span class="sxs-lookup"><span data-stu-id="69663-160">**IUpdateEndpointProvider**</span></span>](iupdateendpointprovider.md)
</dt> </dl>

 

 




