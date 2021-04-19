---
title: Iwmdrmlicenabmanagement processlicenabdeletionmessage-Methode (wmdrmsdk. h)
description: Mit der processlicenabdelete-Methode wird eine Lizenz gelöscht, die für den ursprünglich mit einem anderen Inhalts Schutzsystem geschützten Inhalt importiert wurde.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Processlicenabdeletionmessage-Methode Windows Media-Format
- Processlicenabdeletionmessage-Methode Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, processlicenabdeletionmessage-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373738"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a><span data-ttu-id="30926-106">Iwmdrmlicensmanagement::P rocess licenabdeletionmessage-Methode</span><span class="sxs-lookup"><span data-stu-id="30926-106">IWMDRMLicenseManagement::ProcessLicenseDeletionMessage method</span></span>

<span data-ttu-id="30926-107">Mit der **processlicenabdelete** -Methode wird eine Lizenz gelöscht, die für den ursprünglich mit einem anderen Inhalts Schutzsystem geschützten Inhalt importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="30926-107">The **ProcessLicenseDeletion** method deletes a license that was imported for content originally protected with another content protection system.</span></span>

## <a name="syntax"></a><span data-ttu-id="30926-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30926-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a><span data-ttu-id="30926-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30926-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30926-110">*bstraudeletionmessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30926-110">*bstrDeletionMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30926-111">Meldung zur Identifizierung der zu löschenden Lizenz.</span><span class="sxs-lookup"><span data-stu-id="30926-111">Message identifying the license to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30926-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30926-112">Return value</span></span>

<span data-ttu-id="30926-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="30926-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="30926-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30926-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="30926-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="30926-115">Return code</span></span>                                                                          | <span data-ttu-id="30926-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30926-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="30926-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30926-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="30926-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30926-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30926-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30926-119">Remarks</span></span>

<span data-ttu-id="30926-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="30926-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="30926-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30926-121">Requirements</span></span>



| <span data-ttu-id="30926-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30926-122">Requirement</span></span> | <span data-ttu-id="30926-123">Wert</span><span class="sxs-lookup"><span data-stu-id="30926-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30926-124">Header</span><span class="sxs-lookup"><span data-stu-id="30926-124">Header</span></span><br/> | <dl> <span data-ttu-id="30926-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="30926-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30926-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30926-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30926-127">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="30926-127">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





