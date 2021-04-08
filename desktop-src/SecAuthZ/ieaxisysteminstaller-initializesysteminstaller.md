---
description: Installiert das angegebene ActiveX-Objekt.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'Ieaxisysteminstaller:: initializesysteminstaller-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867812"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a><span data-ttu-id="7b4c7-103">Ieaxisysteminstaller:: initializesysteminstaller-Methode</span><span class="sxs-lookup"><span data-stu-id="7b4c7-103">IeAxiSystemInstaller::InitializeSystemInstaller method</span></span>

<span data-ttu-id="7b4c7-104">Die **initializesysteminstaller** -Methode installiert das angegebene ActiveX-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-104">The **InitializeSystemInstaller** method installs the specified ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b4c7-105">Syntax</span></span>


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a><span data-ttu-id="7b4c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b4c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4c7-107">*bstrinurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4c7-107">*bstrUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4c7-108">Die URL des zu installierenden ActiveX-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-108">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="7b4c7-109">*dwclientpid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4c7-109">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4c7-110">Die Prozess-ID des aufrufenden Prozesses.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-110">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="7b4c7-111">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b4c7-111">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4c7-112">Ein Zeiger auf eine Instanz der [**ieaxiservicecallback**](ieaxiservicecallback.md) -Schnittstelle, die überprüft, ob das ActiveX-Objekt installiert werden darf.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-112">A pointer to an instance of the [**IeAxiServiceCallback**](ieaxiservicecallback.md) interface that verifies whether the ActiveX object is allowed to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="7b4c7-113">*pbstrinnonce* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7b4c7-113">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4c7-114">Ein Kontext, der zum Freigeben von Zustandsinformationen in Aufrufen anderer Methoden verwendet werden kann, die zum Überprüfen und Herunterladen des ActiveX-Objekts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-114">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4c7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b4c7-115">Return value</span></span>

<span data-ttu-id="7b4c7-116">Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="7b4c7-117">Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="7b4c7-118">Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="7b4c7-118">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4c7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b4c7-119">Requirements</span></span>



| <span data-ttu-id="7b4c7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b4c7-120">Requirement</span></span> | <span data-ttu-id="7b4c7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7b4c7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4c7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b4c7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4c7-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b4c7-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7b4c7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b4c7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4c7-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7b4c7-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="7b4c7-126">IID</span><span class="sxs-lookup"><span data-stu-id="7b4c7-126">IID</span></span><br/>                      | <span data-ttu-id="7b4c7-127">IID \_ ieaxisysteminstaller ist als a50ea6f8-4764-4299-b309-022b2a8b4d8d definiert.</span><span class="sxs-lookup"><span data-stu-id="7b4c7-127">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="7b4c7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b4c7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4c7-129">**Ieaxisysteminstaller**</span><span class="sxs-lookup"><span data-stu-id="7b4c7-129">**IeAxiSystemInstaller**</span></span>](ieaxisysteminstaller.md)
</dt> </dl>

 

