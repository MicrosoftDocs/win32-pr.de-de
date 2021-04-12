---
description: Beschreibt die Erstellungs Parameter für ein Gerät.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: D3DDEVICE_CREATION_PARAMETERS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354476"
---
# <a name="d3ddevice_creation_parameters-structure"></a><span data-ttu-id="f5eb8-103">Struktur der D3DDEVICE- \_ Erstellungs \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="f5eb8-103">D3DDEVICE\_CREATION\_PARAMETERS structure</span></span>

<span data-ttu-id="f5eb8-104">Beschreibt die Erstellungs Parameter für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-104">Describes the creation parameters for a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5eb8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5eb8-105">Syntax</span></span>


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="f5eb8-106">Member</span><span class="sxs-lookup"><span data-stu-id="f5eb8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5eb8-107">**AdapterOrdinal**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-107">**AdapterOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="f5eb8-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5eb8-109">Die Ordinalzahl, die den Anzeige Adapter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-109">Ordinal number that denotes the display adapter.</span></span> <span data-ttu-id="f5eb8-110">D3DADAPTER \_ der Standardwert ist immer der primäre Anzeige Adapter.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-110">D3DADAPTER\_DEFAULT is always the primary display adapter.</span></span> <span data-ttu-id="f5eb8-111">Verwenden Sie diese Ordinalzahl als Adapter Parameter für jede der [**IDirect3D9**](/windows/desktop/api) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-111">Use this ordinal as the Adapter parameter for any of the [**IDirect3D9**](/windows/desktop/api) methods.</span></span> <span data-ttu-id="f5eb8-112">Beachten Sie, dass verschiedene Instanzen von Direct3D 9,0-Objekten unterschiedliche ordinale verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-112">Note that different instances of Direct3D 9.0 objects can use different ordinals.</span></span> <span data-ttu-id="f5eb8-113">Adapter können ein System eingeben oder verlassen, wenn Benutzer z. b. Monitore von einem System mit mehreren Monitoren hinzufügen oder entfernen oder wenn Sie einen Laptop mit einem anderen Laptop austauschen.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-113">Adapters can enter or leave a system when users, for example, add or remove monitors from a multiple-monitor system or when they hot-swap a laptop.</span></span> <span data-ttu-id="f5eb8-114">Folglich sollten Sie diese Ordinalzahl nur in einer Direct3D 9,0-Instanz verwenden, die bekanntermaßen gültig ist, d. h. entweder den Direct3D 9,0, der diese [**IDirect3DDevice9**](/windows/desktop/api) -Schnittstelle erstellt hat, oder Direct3D 9,0, der von [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d)zurückgegeben wurde, wie durch diese **IDirect3DDevice9** -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f5eb8-114">Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this [**IDirect3DDevice9**](/windows/desktop/api) interface or the Direct3D 9.0 returned from [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), as called through this **IDirect3DDevice9** interface.</span></span>

</dd> <dt>

<span data-ttu-id="f5eb8-115">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-115">**DeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="f5eb8-116">Typ: **[ **D3DDEVTYPE**](./d3ddevtype.md)**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-116">Type: **[**D3DDEVTYPE**](./d3ddevtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5eb8-117">Member des [**D3DDEVTYPE**](./d3ddevtype.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-117">Member of the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type.</span></span> <span data-ttu-id="f5eb8-118">Gibt den Umfang der emulierten Funktionen für dieses Gerät an.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-118">Denotes the amount of emulated functionality for this device.</span></span> <span data-ttu-id="f5eb8-119">Der Wert dieses Parameters spiegelt den Wert wider, der an den aufzurufenden Befehl "up- [**Device**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) " übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-119">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="f5eb8-120">**hfocus Window**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-120">**hFocusWindow**</span></span>
</dt> <dd>

<span data-ttu-id="f5eb8-121">Typ: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-121">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5eb8-122">Fenster Handle, zu dem der Fokus für dieses Direct3D-Gerät gehört.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-122">Window handle to which focus belongs for this Direct3D device.</span></span> <span data-ttu-id="f5eb8-123">Der Wert dieses Parameters spiegelt den Wert wider, der an den aufzurufenden Befehl "up- [**Device**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) " übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-123">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="f5eb8-124">**Verhaltflags**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-124">**BehaviorFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f5eb8-125">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5eb8-126">Eine Kombination aus einer oder mehreren [D3DCREATE](d3dcreate.md) -Konstanten, die das globale Verhalten des Geräts steuern.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-126">A combination of one or more [D3DCREATE](d3dcreate.md) constants that control global behavior of the device.</span></span> <span data-ttu-id="f5eb8-127">Diese Konstanten spiegeln die Konstanten wider, die beim Erstellen des Geräts an " [**kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) " übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="f5eb8-127">These constants mirror the constants passed to [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) when the device was created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5eb8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5eb8-128">Requirements</span></span>



| <span data-ttu-id="f5eb8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5eb8-129">Requirement</span></span> | <span data-ttu-id="f5eb8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f5eb8-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5eb8-131">Header</span><span class="sxs-lookup"><span data-stu-id="f5eb8-131">Header</span></span><br/> | <dl> <span data-ttu-id="f5eb8-132"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5eb8-132"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5eb8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5eb8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5eb8-134">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="f5eb8-134">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="f5eb8-135">**Getkreationparameters**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-135">**GetCreationParameters**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[<span data-ttu-id="f5eb8-136">**"Kreatedevice"**</span><span class="sxs-lookup"><span data-stu-id="f5eb8-136">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
