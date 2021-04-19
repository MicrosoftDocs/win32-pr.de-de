---
title: Iwmdrmlicense getinclusionlist-Methode (wmdrmsdk. h)
description: Die getinclusionlist-Methode ruft die gesamte Inklusions Liste für die aktuelle Lizenz oder Lizenz Kette ab.
ms.assetid: a3cb70c5-7d20-413c-aeb8-66c9233b384e
keywords:
- Getinclusionlist-Methode, Windows Media-Format
- Getinclusionlist-Methode, Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, getinclusionlist-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetInclusionList
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f0d2837a4bb84c07214cce3e4fbc3d4d96b9583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367427"
---
# <a name="iwmdrmlicensegetinclusionlist-method"></a><span data-ttu-id="6b57e-106">Iwmdrmlicense:: getinclusionlist-Methode</span><span class="sxs-lookup"><span data-stu-id="6b57e-106">IWMDRMLicense::GetInclusionList method</span></span>

<span data-ttu-id="6b57e-107">Die **getinclusionlist** -Methode ruft die gesamte Inklusions Liste für die aktuelle Lizenz oder Lizenz Kette ab.</span><span class="sxs-lookup"><span data-stu-id="6b57e-107">The **GetInclusionList** method retrieves the entire inclusion list for the current license or license chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b57e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b57e-108">Syntax</span></span>


```C++
HRESULT GetInclusionList(
  [out] GUID  **ppGuids,
  [out] DWORD *pcGuids
);
```



## <a name="parameters"></a><span data-ttu-id="6b57e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b57e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b57e-110">*ppguids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b57e-110">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b57e-111">Empfängt ein Array von GUIDs, das die enthaltenen Technologien identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6b57e-111">Receives an array of GUIDs identifying the included technologies.</span></span>

</dd> <dt>

<span data-ttu-id="6b57e-112">*pcguids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b57e-112">*pcGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b57e-113">Empfängt die Anzahl der Elemente im *ppguids* -Array.</span><span class="sxs-lookup"><span data-stu-id="6b57e-113">Receives the number of elements in the *ppGuids* array.</span></span> <span data-ttu-id="6b57e-114">Das Array wird mithilfe von **cotaskmemzuzuordnungs** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6b57e-114">The array is allocated by using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="6b57e-115">Wenn Sie mit der Liste fertig sind, geben Sie den Arbeitsspeicher frei, indem Sie **CoTaskMemFree** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6b57e-115">When finished with the list, release the memory by calling **CoTaskMemFree**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b57e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b57e-116">Return value</span></span>

<span data-ttu-id="6b57e-117">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b57e-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6b57e-118">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6b57e-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6b57e-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b57e-119">Return code</span></span>                                                                          | <span data-ttu-id="6b57e-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b57e-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6b57e-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b57e-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6b57e-122">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b57e-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b57e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b57e-123">Remarks</span></span>

<span data-ttu-id="6b57e-124">Mit dem Lizenz Aussteller können andere Schutzsysteme angegeben werden, in die der verschlüsselte Inhalt konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b57e-124">The license issuer can specify other protection systems to which the encrypted content may be converted.</span></span> <span data-ttu-id="6b57e-125">Die Liste der von dieser Methode abgerufenen GUIDs identifiziert die zulässigen Schutzsysteme.</span><span class="sxs-lookup"><span data-stu-id="6b57e-125">The list of GUIDs retrieved by this method identifies the allowed protection systems.</span></span> <span data-ttu-id="6b57e-126">Wenn Sie in einen Lizenzvertrag von Microsoft eingeben, um die stubbibliothek zu erhalten, erhalten Sie eine Liste der derzeit unterstützten Schutzsysteme und die GUIDs, die zur Identifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b57e-126">When you enter into a license agreement with Microsoft to get the stub library, you will receive a list of currently supported protection systems and the GUIDs used to identify them.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b57e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b57e-127">Requirements</span></span>



| <span data-ttu-id="6b57e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b57e-128">Requirement</span></span> | <span data-ttu-id="6b57e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="6b57e-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b57e-130">Header</span><span class="sxs-lookup"><span data-stu-id="6b57e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6b57e-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b57e-131"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b57e-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b57e-132">Library</span></span><br/> | <dl> <span data-ttu-id="6b57e-133"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b57e-133"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b57e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b57e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b57e-135">**Explizite Autorisierungs-und Inklusions Listen**</span><span class="sxs-lookup"><span data-stu-id="6b57e-135">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="6b57e-136">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6b57e-136">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





