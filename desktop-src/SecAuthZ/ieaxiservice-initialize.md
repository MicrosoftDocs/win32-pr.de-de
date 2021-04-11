---
description: Hiermit wird ein ActiveX-Objekt überprüft und heruntergeladen.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'Ieaxiservice:: Initialize-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218190"
---
# <a name="ieaxiserviceinitialize-method"></a><span data-ttu-id="ce2a8-103">Ieaxiservice:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="ce2a8-103">IeAxiService::Initialize method</span></span>

<span data-ttu-id="ce2a8-104">Mit der **Initialize** -Methode wird ein ActiveX-Objekt überprüft und heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-104">The **Initialize** method checks and downloads an ActiveX object.</span></span> <span data-ttu-id="ce2a8-105">Wenn das-Objekt die Richtlinien Anforderungen erfüllt, initialisiert diese Methode ein Systemobjekt, das das ActiveX-Objekt installiert.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-105">If the object meets policy requirements, this method initializes a system object that installs the ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce2a8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce2a8-106">Syntax</span></span>


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a><span data-ttu-id="ce2a8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce2a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce2a8-108">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce2a8-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2a8-109">Ein Handle für das übergeordnete Fenster des Fensters, das versucht, das ActiveX-Steuerelement zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-109">A handle to the parent window of the window that is attempting to install the ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="ce2a8-110">*dwclientpid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce2a8-110">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2a8-111">Die Prozess-ID des aufrufenden Prozesses.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-111">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="ce2a8-112">*bstraudesktop* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce2a8-112">*bstrDesktop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2a8-113">Der Desktop für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-113">The desktop for the object.</span></span>

</dd> <dt>

<span data-ttu-id="ce2a8-114">*bstrinclsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce2a8-114">*bstrClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2a8-115">Die Klassen-ID des zu installierenden ActiveX-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-115">The class ID of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="ce2a8-116">*bstrinurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce2a8-116">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2a8-117">Die URL des zu installierenden ActiveX-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-117">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="ce2a8-118">*pbstrinnonce* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce2a8-118">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2a8-119">Ein Kontext, der zum Freigeben von Zustandsinformationen in Aufrufen anderer Methoden verwendet werden kann, die zum Überprüfen und Herunterladen des ActiveX-Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-119">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> <dt>

<span data-ttu-id="ce2a8-120">*ppisyncbrokerinterface* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ce2a8-120">*ppISyncBrokerInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2a8-121">Ein Zeiger auf die Instanz der [**ieaxisysteminstaller**](ieaxisysteminstaller.md) -Schnittstelle, mit der das ActiveX-Steuerelement installiert wird.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-121">A pointer to the instance of the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface that installs the ActiveX control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce2a8-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce2a8-122">Return value</span></span>

<span data-ttu-id="ce2a8-123">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-123">If the function succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="ce2a8-124">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Fehlercodes sein.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-124">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="ce2a8-125">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ce2a8-125">Return code/value</span></span>                                                                                                                                                              | <span data-ttu-id="ce2a8-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce2a8-126">Description</span></span>                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="ce2a8-127"><dt>**Vertrauens \_ Stellung E \_ Betreff \_ nicht \_ vertrauenswürdig**</dt> <dt>0x800b0004</dt></span><span class="sxs-lookup"><span data-stu-id="ce2a8-127"><dt>**TRUST\_E\_SUBJECT\_NOT\_TRUSTED**</dt> <dt>0x800B0004</dt></span></span> </dl> | <span data-ttu-id="ce2a8-128">Das ActiveX-Objekt sollte nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ce2a8-128">The ActiveX object should not be installed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ce2a8-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce2a8-129">Requirements</span></span>



| <span data-ttu-id="ce2a8-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce2a8-130">Requirement</span></span> | <span data-ttu-id="ce2a8-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ce2a8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2a8-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce2a8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2a8-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce2a8-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ce2a8-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce2a8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2a8-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ce2a8-135">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="ce2a8-136">IID</span><span class="sxs-lookup"><span data-stu-id="ce2a8-136">IID</span></span><br/>                      | <span data-ttu-id="ce2a8-137">IID \_ ieaxiservice ist definiert als E9E92380-9ecd-4982-A0EB-6815a56ccb27</span><span class="sxs-lookup"><span data-stu-id="ce2a8-137">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ce2a8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce2a8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2a8-139">**Ieaxiservice**</span><span class="sxs-lookup"><span data-stu-id="ce2a8-139">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

 




