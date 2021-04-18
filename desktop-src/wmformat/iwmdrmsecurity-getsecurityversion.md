---
title: Iwmdrmsecurity getsecurityversion-Methode (wmdrmsdk. h)
description: Die getsecurityversion-Methode ruft die Version des DRM-Subsystems auf dem Client Computer ab.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Getsecurityversion-Methode Windows Media-Format
- Getsecurityversion-Methode Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getsecurityversion-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368489"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a><span data-ttu-id="22b63-106">Iwmdrmsecurity:: getsecurityversion-Methode</span><span class="sxs-lookup"><span data-stu-id="22b63-106">IWMDRMSecurity::GetSecurityVersion method</span></span>

<span data-ttu-id="22b63-107">Die **getsecurityversion** -Methode ruft die Version des DRM-Subsystems auf dem Client Computer ab.</span><span class="sxs-lookup"><span data-stu-id="22b63-107">The **GetSecurityVersion** method retrieves the version of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="22b63-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="22b63-108">Syntax</span></span>


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a><span data-ttu-id="22b63-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="22b63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22b63-110">*pbstrauversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="22b63-110">*pbstrVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22b63-111">Adresse einer Variablen, die die Versionsnummer des DRM-Subsystems empfängt.</span><span class="sxs-lookup"><span data-stu-id="22b63-111">Address of a variable that receives the DRM subsystem version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22b63-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22b63-112">Return value</span></span>

<span data-ttu-id="22b63-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="22b63-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="22b63-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="22b63-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="22b63-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="22b63-115">Return code</span></span>                                                                          | <span data-ttu-id="22b63-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22b63-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="22b63-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22b63-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="22b63-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22b63-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="22b63-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22b63-119">Remarks</span></span>

<span data-ttu-id="22b63-120">Die Versionsnummer wird als Zeichenfolge ausgedrückt, die aus vier Zahlen besteht, die durch Punkte getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="22b63-120">The version number is expressed as a string consisting of four numbers separated by periods.</span></span> <span data-ttu-id="22b63-121">Die erste Zahl ist die Hauptversionsnummer, die normalerweise auf 2 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="22b63-121">The first number is the major version number, which is usually set to 2.</span></span> <span data-ttu-id="22b63-122">Die zweite Zahl ist die neben Versionsnummer von 2 bis 10.</span><span class="sxs-lookup"><span data-stu-id="22b63-122">The second number is the minor version number, ranging from 2 to 10.</span></span> <span data-ttu-id="22b63-123">Die dritte Zahl wird immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22b63-123">The third number is always set to 0.</span></span> <span data-ttu-id="22b63-124">Die vierte Zahl ist auf 0 oder 1 festgelegt, und ist ein boolescher Wert, der angibt, ob das Subsystem individualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="22b63-124">The fourth number is set to 0 or 1, and is a Boolean value indicating whether the subsystem has been individualized.</span></span> <span data-ttu-id="22b63-125">Die Versionsnummer "2.4.0.1" gibt z. b. die individualisierte vierte neben Version der zweiten Hauptversion an.</span><span class="sxs-lookup"><span data-stu-id="22b63-125">For example, a version number of "2.4.0.1" indicates the individualized fourth minor version of the second major version.</span></span>

## <a name="requirements"></a><span data-ttu-id="22b63-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22b63-126">Requirements</span></span>



| <span data-ttu-id="22b63-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22b63-127">Requirement</span></span> | <span data-ttu-id="22b63-128">Wert</span><span class="sxs-lookup"><span data-stu-id="22b63-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22b63-129">Header</span><span class="sxs-lookup"><span data-stu-id="22b63-129">Header</span></span><br/>  | <dl> <span data-ttu-id="22b63-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="22b63-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="22b63-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22b63-131">Library</span></span><br/> | <dl> <span data-ttu-id="22b63-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22b63-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22b63-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22b63-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b63-134">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="22b63-134">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





