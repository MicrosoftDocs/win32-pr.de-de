---
title: Iwmdrmlicencmanagement | atelicenserevocationchallenge-Methode (wmdrmsdk. h)
description: Die Methode "samatelicenserevocationchallenge" generiert eine Lizenz Sperr Aufforderung.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Methode "samatelicenserevocationchallenge" Windows Media Format
- Methode "samatelicenserevocationchallenge" Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicencmanagement-Schnittstelle Windows Media-Format, Methode "kreatelicenserevocationchallenge"
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361498"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a><span data-ttu-id="7e77f-106">Iwmdrmlicenabmanagement:: samatelicenserevocationchallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="7e77f-106">IWMDRMLicenseManagement::CreateLicenseRevocationChallenge method</span></span>

<span data-ttu-id="7e77f-107">Die Methode " **samatelicenserevocationchallenge** " generiert eine Lizenz Sperr Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="7e77f-107">The **CreateLicenseRevocationChallenge** method generates a license revocation challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e77f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e77f-108">Syntax</span></span>


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a><span data-ttu-id="7e77f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e77f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e77f-110">*pbmachineid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e77f-110">*pbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e77f-111">Vom Benutzer angegebener Computer Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7e77f-111">User-specified machine identifier.</span></span> <span data-ttu-id="7e77f-112">Dieser Wert wird verwendet, um eine Lizenz auf dem Server abzufragen, und muss dem vom Lizenzserver verwendeten Format entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7e77f-112">This value is used to query for a license on the server and must conform to whatever format the license server uses.</span></span>

</dd> <dt>

<span data-ttu-id="7e77f-113">*cbmachineid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e77f-113">*cbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e77f-114">Größe (in Bytes) des Computer Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="7e77f-114">Size, in bytes, of the machine identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7e77f-115">*pbchallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e77f-115">*pbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e77f-116">Vom Benutzer angegebene Abfrage Daten.</span><span class="sxs-lookup"><span data-stu-id="7e77f-116">User-specified challenge data.</span></span> <span data-ttu-id="7e77f-117">Diese Daten werden zusätzlich zum Computer Bezeichner verwendet, um den Lizenzserver abzufragen, damit Lizenzen widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="7e77f-117">This data, in addition to the machine identifier, is used to query the license server for licenses to be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="7e77f-118">*cbchallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e77f-118">*cbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e77f-119">Größe der Abfrage Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7e77f-119">Size, in bytes, of the challenge data.</span></span>

</dd> <dt>

<span data-ttu-id="7e77f-120">*ppbherausfordergeoutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7e77f-120">*ppbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e77f-121">Adresse eines Zeigers, der die Adresse der Challenge-Ausgabe empfängt.</span><span class="sxs-lookup"><span data-stu-id="7e77f-121">Address of a pointer that receives the address of the challenge output.</span></span> <span data-ttu-id="7e77f-122">Dieser Puffer stellt die Daten dar, die an den Lizenz Sperr Dienst gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e77f-122">This buffer is the data that is sent to the license revocation service.</span></span> <span data-ttu-id="7e77f-123">Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7e77f-123">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="7e77f-124">*pcbherausfordergeoutput* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7e77f-124">*pcbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e77f-125">Adresse einer Variablen, die die Größe der zugeordneten Challenge-Ausgabedaten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="7e77f-125">Address of a variable that receives the size of the allocated challenge output data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e77f-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e77f-126">Return value</span></span>

<span data-ttu-id="7e77f-127">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="7e77f-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7e77f-128">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7e77f-128">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7e77f-129">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7e77f-129">Return code</span></span>                                                                          | <span data-ttu-id="7e77f-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e77f-130">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7e77f-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7e77f-131"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7e77f-132">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e77f-132">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7e77f-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e77f-133">Remarks</span></span>

<span data-ttu-id="7e77f-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="7e77f-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e77f-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e77f-135">Requirements</span></span>



| <span data-ttu-id="7e77f-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e77f-136">Requirement</span></span> | <span data-ttu-id="7e77f-137">Wert</span><span class="sxs-lookup"><span data-stu-id="7e77f-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e77f-138">Header</span><span class="sxs-lookup"><span data-stu-id="7e77f-138">Header</span></span><br/> | <dl> <span data-ttu-id="7e77f-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e77f-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e77f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e77f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e77f-141">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7e77f-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





