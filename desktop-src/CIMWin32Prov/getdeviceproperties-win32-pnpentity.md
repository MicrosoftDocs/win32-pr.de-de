---
description: Ruft die angegebenen Eigenschaften dieses Plug & Play Geräts ab.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Getdeviceproperties-Methode der Win32_PnPEntity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041397"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="56a9f-103">Getdeviceproperties-Methode der Win32 \_ pnptity-Klasse</span><span class="sxs-lookup"><span data-stu-id="56a9f-103">GetDeviceProperties method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="56a9f-104">Ruft die angegebenen Eigenschaften dieses Plug & Play Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="56a9f-104">Gets the specified properties of this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a9f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56a9f-105">Syntax</span></span>


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a><span data-ttu-id="56a9f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56a9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a9f-107">*devicepropertykeys* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="56a9f-107">*devicePropertyKeys* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="56a9f-108">Die zurück zugebende Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="56a9f-108">The properties to return.</span></span>

</dd> <dt>

<span data-ttu-id="56a9f-109">*deviceproperties* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56a9f-109">*deviceProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56a9f-110">Die angeforderten Eigenschaften in den entsprechenden Untertypen der [**Win32- \_ pnpdeviceproperty**](win32-pnpdeviceproperty.md) abstract-Klasse.</span><span class="sxs-lookup"><span data-stu-id="56a9f-110">The requested properties in appropriate subtypes of the [**Win32\_PnPDeviceProperty**](win32-pnpdeviceproperty.md) abstract class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56a9f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56a9f-111">Requirements</span></span>



| <span data-ttu-id="56a9f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56a9f-112">Requirement</span></span> | <span data-ttu-id="56a9f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="56a9f-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56a9f-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56a9f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="56a9f-115">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56a9f-115">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="56a9f-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56a9f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="56a9f-117">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="56a9f-117">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="56a9f-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="56a9f-118">Namespace</span></span><br/>                | <span data-ttu-id="56a9f-119">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="56a9f-119">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="56a9f-120">MOF</span><span class="sxs-lookup"><span data-stu-id="56a9f-120">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56a9f-121"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="56a9f-121"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="56a9f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="56a9f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56a9f-123"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56a9f-123"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56a9f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56a9f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a9f-125">**Win32- \_ pnptity**</span><span class="sxs-lookup"><span data-stu-id="56a9f-125">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




