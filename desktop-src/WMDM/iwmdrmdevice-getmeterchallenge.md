---
title: Methode ' iwmdrmdevice getmeterchallenge '
description: Die getmeterchallenge-Methode ruft die Messungs Herausforderung ab.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Getmeterchallenge-Methode, Windows Media Device Manager
- Getmeterchallenge-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, getmeterchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364034"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a><span data-ttu-id="de3d7-106">Iwmdrmdevice:: getmeterchallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="de3d7-106">IWMDRMDevice::GetMeterChallenge method</span></span>

<span data-ttu-id="de3d7-107">Die **getmeterchallenge** -Methode ruft die Messungs Herausforderung ab.</span><span class="sxs-lookup"><span data-stu-id="de3d7-107">The **GetMeterChallenge** method retrieves the metering challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3d7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="de3d7-108">Syntax</span></span>


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="de3d7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="de3d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3d7-110">*bstrinmetercert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de3d7-110">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3d7-111">Das Messungs Zertifikat, das der Inhalts Besitzer zum Erfassen der zugeordneten Messungs Daten auf dem Gerät an den Host Computer sendet.</span><span class="sxs-lookup"><span data-stu-id="de3d7-111">Metering certificate that the content owner sends to the host computer for collecting the associated metering data on the device</span></span>

</dd> <dt>

<span data-ttu-id="de3d7-112">*ppbmeterchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de3d7-112">*ppbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de3d7-113">Ergebnis der abgerufenen Messungs Abfrage.</span><span class="sxs-lookup"><span data-stu-id="de3d7-113">Retrieved metering challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="de3d7-114">*pcbmeterchallenge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de3d7-114">*pcbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de3d7-115">Die Größe der Messungs Herausforderung in Bytes.</span><span class="sxs-lookup"><span data-stu-id="de3d7-115">The size of the metering challenge, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3d7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de3d7-116">Return value</span></span>

<span data-ttu-id="de3d7-117">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="de3d7-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="de3d7-118">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="de3d7-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="de3d7-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="de3d7-119">Return code</span></span>                                                                          | <span data-ttu-id="de3d7-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de3d7-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="de3d7-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de3d7-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="de3d7-122">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de3d7-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de3d7-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de3d7-123">Remarks</span></span>

<span data-ttu-id="de3d7-124">Messungs Daten werden im DRM-Datenspeicher auf dem Gerät für Inhalte mit aktivierter Messung gesammelt und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="de3d7-124">Metering data is collected and stored in the DRM data store on the device for content with metering enabled.</span></span> <span data-ttu-id="de3d7-125">Aktionen wie z. b. Play werden aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="de3d7-125">Actions such as play will be recorded.</span></span> <span data-ttu-id="de3d7-126">Wenn diese Funktion aufgerufen wird, sammelt das Gerät die Messungs Daten im DRM-Datenspeicher in Form eines XML-Dokuments und sendet Sie an den Host Computer.</span><span class="sxs-lookup"><span data-stu-id="de3d7-126">When this function is called, the device collects the metering data in the DRM data store in the form of an XML document and sends it to the hostcomputer.</span></span> <span data-ttu-id="de3d7-127">Wenn zu viele Daten vorhanden sind, werden Sie in Phasen gesendet.</span><span class="sxs-lookup"><span data-stu-id="de3d7-127">If there is too much data, it is sent in phases.</span></span>

<span data-ttu-id="de3d7-128">Wenn der Host Computer die Messungs Daten empfängt, sendet er die Daten über das Internet an die im Messungs Zertifikat angegebene URL.</span><span class="sxs-lookup"><span data-stu-id="de3d7-128">When the host computer receives the metering data, it sends the data over the Internet to the URL specified in the metering certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="de3d7-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de3d7-129">Requirements</span></span>



| <span data-ttu-id="de3d7-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de3d7-130">Requirement</span></span> | <span data-ttu-id="de3d7-131">Wert</span><span class="sxs-lookup"><span data-stu-id="de3d7-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de3d7-132">Header</span><span class="sxs-lookup"><span data-stu-id="de3d7-132">Header</span></span><br/>  | <dl> <span data-ttu-id="de3d7-133"><dt>Wmddrmsp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de3d7-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="de3d7-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de3d7-134">Library</span></span><br/> | <dl> <span data-ttu-id="de3d7-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de3d7-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3d7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de3d7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3d7-137">**Iwmdrmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="de3d7-137">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





