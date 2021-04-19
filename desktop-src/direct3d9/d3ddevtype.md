---
description: Definiert Gerätetypen.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: D3DDEVTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361852"
---
# <a name="d3ddevtype-enumeration"></a><span data-ttu-id="1f3ac-103">D3DDEVTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1f3ac-103">D3DDEVTYPE enumeration</span></span>

<span data-ttu-id="1f3ac-104">Definiert Gerätetypen.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-104">Defines device types.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f3ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f3ac-105">Syntax</span></span>


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a><span data-ttu-id="1f3ac-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1f3ac-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1f3ac-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAL**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE\_HAL**</span></span>
</dt> <dd>

<span data-ttu-id="1f3ac-108">Hardware-rasterisierung.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-108">Hardware rasterization.</span></span> <span data-ttu-id="1f3ac-109">Schattierung erfolgt mit Software, Hardware oder gemischter Transformation und Beleuchtung.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-109">Shading is done with software, hardware, or mixed transform and lighting.</span></span>

</dd> <dt>

<span data-ttu-id="1f3ac-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NullRef**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE\_NULLREF**</span></span>
</dt> <dd>

<span data-ttu-id="1f3ac-111">Initialisieren Sie Direct3D auf einem Computer, auf dem weder Hardware noch Verweis-rasterisierung verfügbar ist, und aktivieren Sie Ressourcen für die Erstellung von 3D-Inhalten.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-111">Initialize Direct3D on a computer that has neither hardware nor reference rasterization available, and enable resources for 3D content creation.</span></span> <span data-ttu-id="1f3ac-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1f3ac-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ Ref**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE\_REF**</span></span>
</dt> <dd>

<span data-ttu-id="1f3ac-114">Direct3D-Funktionen sind in Software implementiert. der verweisrasterizer verwendet jedoch bestimmte CPU-Anweisungen, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-114">Direct3D features are implemented in software; however, the reference rasterizer does make use of special CPU instructions whenever it can.</span></span>

<span data-ttu-id="1f3ac-115">Das Referenzgerät wird vom Windows SDK 8,0 oder höher installiert und ist als Hilfe beim Debuggen nur für die Entwicklung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-115">The reference device is installed by the Windows SDK 8.0 or later and is intended as an aid in debugging for development only.</span></span>

</dd> <dt>

<span data-ttu-id="1f3ac-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE\_SW**</span></span>
</dt> <dd>

<span data-ttu-id="1f3ac-117">Ein austauschbares Software Gerät, das bei [**IDirect3D9:: registersoftwaredevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice)registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-117">A pluggable software device that has been registered with [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span></span>

</dd> <dt>

<span data-ttu-id="1f3ac-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1f3ac-119">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1f3ac-120">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1f3ac-121">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f3ac-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f3ac-122">Remarks</span></span>

<span data-ttu-id="1f3ac-123">Alle Methoden der [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) -Schnittstelle, die einen **D3DDEVTYPE** -Gerätetyp annehmen, schlagen fehl, wenn D3DDEVTYPE \_ NullRef angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-123">All methods of the [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) interface that take a **D3DDEVTYPE** device type will fail if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="1f3ac-124">Um diese Methoden zu verwenden, ersetzen Sie D3DDEVTYPE \_ ref im-Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-124">To use these methods, substitute D3DDEVTYPE\_REF in the method call.</span></span>

<span data-ttu-id="1f3ac-125">Ein D3DDEVTYPE \_ ref-Gerät sollte in D3DPOOL \_ Scratch-Speicher erstellt werden, es sei denn, es sind Scheitelpunkt-und Index Puffer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-125">A D3DDEVTYPE\_REF device should be created in D3DPOOL\_SCRATCH memory, unless vertex and index buffers are required.</span></span> <span data-ttu-id="1f3ac-126">Um Vertex-und Index Puffer zu unterstützen, erstellen Sie das Gerät im D3DPOOL \_ systemarbeits Speicher.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-126">To support vertex and index buffers, create the device in D3DPOOL\_SYSTEMMEM memory.</span></span>

<span data-ttu-id="1f3ac-127">Wenn D3dref9.dll installiert ist, verwendet Direct3D den verweisrasterizer zum Erstellen eines D3DDEVTYPE \_ ref-Gerätetyps, auch wenn D3DDEVTYPE \_ NullRef angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-127">If D3dref9.dll is installed, Direct3D will use the reference rasterizer to create a D3DDEVTYPE\_REF device type, even if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="1f3ac-128">Wenn D3dref9.dll nicht verfügbar ist und D3DDEVTYPE \_ NullRef angegeben ist, wird die Szene weder von Direct3D gerbt noch präsentiert.</span><span class="sxs-lookup"><span data-stu-id="1f3ac-128">If D3dref9.dll is not available and D3DDEVTYPE\_NULLREF is specified, Direct3D will neither render nor present the scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f3ac-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f3ac-129">Requirements</span></span>



| <span data-ttu-id="1f3ac-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f3ac-130">Requirement</span></span> | <span data-ttu-id="1f3ac-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1f3ac-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3ac-132">Header</span><span class="sxs-lookup"><span data-stu-id="1f3ac-132">Header</span></span><br/> | <dl> <span data-ttu-id="1f3ac-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f3ac-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f3ac-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f3ac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f3ac-135">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="1f3ac-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="1f3ac-136">**IDirect3D9:: CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-136">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[<span data-ttu-id="1f3ac-137">**IDirect3D9:: checkdevicemultisampletype**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-137">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[<span data-ttu-id="1f3ac-138">**IDirect3D9:: checkabvicetype**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-138">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[<span data-ttu-id="1f3ac-139">**IDirect3D9:: kreatedevice**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-139">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="1f3ac-140">**IDirect3D9:: getde vicecaps**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-140">**IDirect3D9::GetDeviceCaps**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[<span data-ttu-id="1f3ac-141">**D3DDEVICE- \_ Erstellungs \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="1f3ac-141">**D3DDEVICE\_CREATION\_PARAMETERS**</span></span>](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
