---
title: Mrmplatformversion-Enumeration (mrmresourceingedexer. h)
description: Definiert Konstanten, die eine Platt Form Version angeben. Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme.
ms.assetid: 7BA30B8F-FB23-4DCA-930D-099C7F8476E9
keywords:
- Mrmplatformversion-enumerationsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MrmPlatformVersion
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8127d3e6e99d974315327cf89ae9e82add7bc628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957111"
---
# <a name="mrmplatformversion-enumeration"></a><span data-ttu-id="b610c-105">Mrmplatformversion-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b610c-105">MrmPlatformVersion enumeration</span></span>

<span data-ttu-id="b610c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="b610c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b610c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="b610c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b610c-108">Definiert Konstanten, die eine Platt Form Version angeben.</span><span class="sxs-lookup"><span data-stu-id="b610c-108">Defines constants that specify a platform version.</span></span> <span data-ttu-id="b610c-109">Weitere Informationen und szenariobasierte Exemplarische Vorgehensweisen zur Verwendung dieser APIs finden Sie unter API für [Paket Ressourcen Indizierung (PRI) und benutzerdefinierte Buildsysteme](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="b610c-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="b610c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b610c-110">Syntax</span></span>


```C++
typedef enum _MrmPlatformVersion { 
  MrmPlatformVersion_Default          = 0,
  MrmPlatformVersion_Windows10_0_0_0  = 0x010A0000,
  MrmPlatformVersion_Windows10_0_0_5  = 0x010A0005
} MrmPlatformVersion;
```



## <a name="constants"></a><span data-ttu-id="b610c-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b610c-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b610c-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**Mrmplatformversion ( \_ Standard)**</span><span class="sxs-lookup"><span data-stu-id="b610c-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="b610c-113">Gibt an, dass die Platt Form Version die Standardversion ist.</span><span class="sxs-lookup"><span data-stu-id="b610c-113">Specifies that the platform version is the default.</span></span>

</dd> <dt>

<span data-ttu-id="b610c-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**Mrmplatformversion \_ Windows 10 \_ 0 \_ 0 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="b610c-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion\_Windows10\_0\_0\_0**</span></span>
</dt> <dd>

<span data-ttu-id="b610c-115">Gibt eine Platt Form Version von Windows 10.0.0.0 an.</span><span class="sxs-lookup"><span data-stu-id="b610c-115">Specifies a platform version of Windows 10.0.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="b610c-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**Mrmplatformversion \_ Windows 10 \_ 0 \_ 0 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="b610c-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion\_Windows10\_0\_0\_5**</span></span>
</dt> <dd>

<span data-ttu-id="b610c-117">Gibt eine Platt Form Version von Windows 10.0.0.5 an.</span><span class="sxs-lookup"><span data-stu-id="b610c-117">Specifies a platform version of Windows 10.0.0.5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b610c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b610c-118">Requirements</span></span>



| <span data-ttu-id="b610c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b610c-119">Requirement</span></span> | <span data-ttu-id="b610c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b610c-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b610c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b610c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b610c-122">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b610c-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b610c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b610c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b610c-124">Nur Windows Server \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b610c-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b610c-125">Header</span><span class="sxs-lookup"><span data-stu-id="b610c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b610c-126"><dt>Mrmresourceingedexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b610c-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b610c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b610c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b610c-128">APIs für die Paketressourcenindizierung (PRI) und benutzerdefinierte Buildsysteme</span><span class="sxs-lookup"><span data-stu-id="b610c-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

