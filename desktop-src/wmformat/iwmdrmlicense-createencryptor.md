---
title: Iwmdrmlicense-Methode "| ateverschlüsseltor" (wmdrmsdk. h)
description: Die Methode "kreateverschlüsseltor" erstellt mithilfe der Einstellungen der aktuellen Lizenz ein Verschlüsselungs Objekt.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Methode "Windows Media" der Methode "Methode"
- Kreateverschlüsseltor-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, Methode "kreateverschlüsseltor"
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361515"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a><span data-ttu-id="8018e-106">Iwmdrmlicense:: up-Verschlüsselungsmethode</span><span class="sxs-lookup"><span data-stu-id="8018e-106">IWMDRMLicense::CreateEncryptor method</span></span>

<span data-ttu-id="8018e-107">Die Methode " **kreateverschlüsseltor** " erstellt mithilfe der Einstellungen der aktuellen Lizenz ein Verschlüsselungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="8018e-107">The **CreateEncryptor** method creates an encryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="8018e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8018e-108">Syntax</span></span>


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a><span data-ttu-id="8018e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8018e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8018e-110">" *ppcryptor* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8018e-110">*ppEncryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8018e-111">Empfängt einen Zeiger auf die [**iwmdrmencrypt**](iwmdrmencrypt.md) -Schnittstelle des neu erstellten Objekts.</span><span class="sxs-lookup"><span data-stu-id="8018e-111">Receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8018e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8018e-112">Return value</span></span>

<span data-ttu-id="8018e-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="8018e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8018e-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8018e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8018e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8018e-115">Return code</span></span>                                                                                                | <span data-ttu-id="8018e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8018e-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="8018e-117"><dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="8018e-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="8018e-118">Es wird eine aktualisierte Inhalts Sperr Liste benötigt.</span><span class="sxs-lookup"><span data-stu-id="8018e-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="8018e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8018e-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="8018e-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8018e-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="8018e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8018e-121">Remarks</span></span>

<span data-ttu-id="8018e-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="8018e-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8018e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8018e-123">Requirements</span></span>



| <span data-ttu-id="8018e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8018e-124">Requirement</span></span> | <span data-ttu-id="8018e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="8018e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8018e-126">Header</span><span class="sxs-lookup"><span data-stu-id="8018e-126">Header</span></span><br/> | <dl> <span data-ttu-id="8018e-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8018e-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8018e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8018e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8018e-129">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="8018e-129">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[<span data-ttu-id="8018e-130">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8018e-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





