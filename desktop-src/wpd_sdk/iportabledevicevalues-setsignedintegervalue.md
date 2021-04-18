---
description: Die setsignedintegervalue-Methode fügt einen neuen Long-Wert (Type VT \_ I4) hinzu oder überschreibt eine vorhandene.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'Iportabledevicevalues:: setsignedintegervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26a5d01ec69203c39008de394e3693acc833d262
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368370"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a><span data-ttu-id="768f3-103">Iportabledevicevalues:: setsignedintegervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="768f3-103">IPortableDeviceValues::SetSignedIntegerValue method</span></span>

<span data-ttu-id="768f3-104">Die **setsignedintegervalue** -Methode fügt einen neuen **Long** -Wert (Type VT \_ I4) hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="768f3-104">The **SetSignedIntegerValue** method adds a new **LONG** value (type VT\_I4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="768f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="768f3-105">Syntax</span></span>


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a><span data-ttu-id="768f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="768f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="768f3-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="768f3-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="768f3-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="768f3-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="768f3-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="768f3-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="768f3-110">Ein **Long** -Wert, der den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="768f3-110">A **LONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="768f3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="768f3-111">Return value</span></span>

<span data-ttu-id="768f3-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="768f3-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="768f3-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="768f3-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="768f3-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="768f3-114">Return code</span></span>                                                                          | <span data-ttu-id="768f3-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="768f3-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="768f3-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="768f3-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="768f3-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="768f3-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="768f3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="768f3-118">Remarks</span></span>

<span data-ttu-id="768f3-119">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="768f3-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="768f3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="768f3-120">Requirements</span></span>



| <span data-ttu-id="768f3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="768f3-121">Requirement</span></span> | <span data-ttu-id="768f3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="768f3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="768f3-123">Header</span><span class="sxs-lookup"><span data-stu-id="768f3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="768f3-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="768f3-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="768f3-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="768f3-125">Library</span></span><br/> | <dl> <span data-ttu-id="768f3-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="768f3-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="768f3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="768f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="768f3-128">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="768f3-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="768f3-129">**Iportablede vicevalues:: getsignedintegervalue**</span><span class="sxs-lookup"><span data-stu-id="768f3-129">**IPortableDeviceValues::GetSignedIntegerValue**</span></span>](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




