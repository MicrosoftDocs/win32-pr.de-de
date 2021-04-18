---
description: Aktiviert oder deaktiviert Debugmeldungen.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: D3DX10DebugMute-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365328"
---
# <a name="d3dx10debugmute-function"></a><span data-ttu-id="5ec78-103">D3DX10DebugMute-Funktion</span><span class="sxs-lookup"><span data-stu-id="5ec78-103">D3DX10DebugMute function</span></span>

<span data-ttu-id="5ec78-104">Aktiviert oder deaktiviert Debugmeldungen.</span><span class="sxs-lookup"><span data-stu-id="5ec78-104">Enable or disable debug messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ec78-105">Syntax</span></span>


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="5ec78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ec78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ec78-107">*Stumm schalten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ec78-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec78-108">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ec78-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ec78-109">Auf **true** festgelegt, um Debugmeldungen zu aktivieren. Legen Sie auf **false** fest, um Debugmeldungen zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="5ec78-109">Set to **TRUE** to enable debug messages; set to **FALSE** to disable debug messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ec78-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ec78-110">Return value</span></span>

<span data-ttu-id="5ec78-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ec78-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ec78-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="5ec78-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ec78-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ec78-113">Remarks</span></span>

<span data-ttu-id="5ec78-114">Verwenden Sie diese Funktion zum Deaktivieren von Fehlermeldungen für d3dx10-APIs während des Debuggens. die Verwendung dieser Funktion sollte durch den d3d10 \_ Debug-Compilerschalter geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="5ec78-114">Use this function to disable error messages for D3DX10 APIs during debug; the use of this function should be guarded by the D3D10\_DEBUG compiler switch.</span></span>


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



<span data-ttu-id="5ec78-115">Der Standardstatus ist **true** für einen Debugbuild.</span><span class="sxs-lookup"><span data-stu-id="5ec78-115">The default state is **TRUE** for a debug build.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ec78-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ec78-116">Requirements</span></span>



| <span data-ttu-id="5ec78-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ec78-117">Requirement</span></span> | <span data-ttu-id="5ec78-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5ec78-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec78-119">Header</span><span class="sxs-lookup"><span data-stu-id="5ec78-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5ec78-120"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec78-120"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="5ec78-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ec78-121">Library</span></span><br/> | <dl> <span data-ttu-id="5ec78-122"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ec78-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ec78-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ec78-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec78-124">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="5ec78-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
