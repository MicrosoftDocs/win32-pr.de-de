---
title: D3DX11_EFFECT_TYPE_DESC-Struktur (D3dx11effect. h)
description: Beschreibt einen Effekt Variablen-Typ.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- D3DX11_EFFECT_TYPE_DESC Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f4e8af391fed5717f47bb4b80398129cb98ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870180"
---
# <a name="d3dx11_effect_type_desc-structure"></a><span data-ttu-id="0e948-104">Bibliothek d3dx11 \_ Effect- \_ Typ ( \_ DESC-Struktur)</span><span class="sxs-lookup"><span data-stu-id="0e948-104">D3DX11\_EFFECT\_TYPE\_DESC structure</span></span>

<span data-ttu-id="0e948-105">Beschreibt einen Effekt Variablen-Typ.</span><span class="sxs-lookup"><span data-stu-id="0e948-105">Describes an effect-variable type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e948-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e948-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a><span data-ttu-id="0e948-107">Member</span><span class="sxs-lookup"><span data-stu-id="0e948-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0e948-108">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="0e948-108">**TypeName**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-109">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e948-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-110">Der Name des Typs, z. b. "float4" oder "MyStruct".</span><span class="sxs-lookup"><span data-stu-id="0e948-110">Name of the type, for example "float4" or "MyStruct".</span></span>

</dd> <dt>

<span data-ttu-id="0e948-111">**Klasse**</span><span class="sxs-lookup"><span data-stu-id="0e948-111">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-112">Type: **[ **d3d10 \_ Shader- \_ Variablen \_ Klasse**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span><span class="sxs-lookup"><span data-stu-id="0e948-112">Type: **[**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-113">Die Variablen Klasse (siehe [**d3d10 \_ Shader \_ Variable \_ Class**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span><span class="sxs-lookup"><span data-stu-id="0e948-113">The variable class (see [**D3D10\_SHADER\_VARIABLE\_CLASS**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).</span></span>

</dd> <dt>

<span data-ttu-id="0e948-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0e948-114">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-115">Type: **[ **d3d10 \_ Shader \_ - \_ Variablentyp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span><span class="sxs-lookup"><span data-stu-id="0e948-115">Type: **[**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-116">Der Variablentyp (siehe [**d3d10 \_ Shader- \_ \_ Variablentyp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span><span class="sxs-lookup"><span data-stu-id="0e948-116">The variable type (see [**D3D10\_SHADER\_VARIABLE\_TYPE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).</span></span>

</dd> <dt>

<span data-ttu-id="0e948-117">**Elemente**</span><span class="sxs-lookup"><span data-stu-id="0e948-117">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e948-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-119">Anzahl der Elemente in diesem Typ (0, wenn kein Array ist).</span><span class="sxs-lookup"><span data-stu-id="0e948-119">Number of elements in this type (0 if not an array).</span></span>

</dd> <dt>

<span data-ttu-id="0e948-120">**Mitglieder**</span><span class="sxs-lookup"><span data-stu-id="0e948-120">**Members**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-121">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e948-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-122">Anzahl der Elemente (0, wenn keine Struktur ist).</span><span class="sxs-lookup"><span data-stu-id="0e948-122">Number of members (0 if not a structure).</span></span>

</dd> <dt>

<span data-ttu-id="0e948-123">**Zeilen**</span><span class="sxs-lookup"><span data-stu-id="0e948-123">**Rows**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-124">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e948-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-125">Anzahl der Zeilen in diesem Typ (0, wenn kein numerischer primitiver Wert).</span><span class="sxs-lookup"><span data-stu-id="0e948-125">Number of rows in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="0e948-126">**Spalten**</span><span class="sxs-lookup"><span data-stu-id="0e948-126">**Columns**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-127">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e948-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-128">Anzahl der Spalten in diesem Typ (0, wenn kein numerischer primitiver Wert).</span><span class="sxs-lookup"><span data-stu-id="0e948-128">Number of columns in this type (0 if not a numeric primitive).</span></span>

</dd> <dt>

<span data-ttu-id="0e948-129">**Packedsize**</span><span class="sxs-lookup"><span data-stu-id="0e948-129">**PackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-130">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e948-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-131">Anzahl der Bytes, die für die Darstellung dieses Datentyps erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="0e948-131">Number of bytes required to represent this data type, when tightly packed.</span></span>

</dd> <dt>

<span data-ttu-id="0e948-132">**Unpackedsize**</span><span class="sxs-lookup"><span data-stu-id="0e948-132">**UnpackedSize**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-133">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e948-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-134">Anzahl von Bytes, die von diesem Datentyp belegt werden, wenn Sie in einem konstanten Puffer angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0e948-134">Number of bytes occupied by this data type, when laid out in a constant buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0e948-135">**Schritt**</span><span class="sxs-lookup"><span data-stu-id="0e948-135">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="0e948-136">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e948-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0e948-137">Anzahl von Bytes, die zwischen Elementen gesucht werden sollen, wenn Sie in einem konstanten Puffer angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0e948-137">Number of bytes to seek between elements, when laid out in a constant buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e948-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e948-138">Remarks</span></span>

<span data-ttu-id="0e948-139">Bibliothek d3dx11 \_ Effect \_ Type \_ DESC wird mit [ **ID3DX11EffectType:: getdesc** verwendet.](id3dx11effecttype-getdesc.md)</span><span class="sxs-lookup"><span data-stu-id="0e948-139">D3DX11\_EFFECT\_TYPE\_DESC is used with [**ID3DX11EffectType::GetDesc**](id3dx11effecttype-getdesc.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="0e948-140">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0e948-140">Requirements</span></span>



| <span data-ttu-id="0e948-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e948-141">Requirement</span></span> | <span data-ttu-id="0e948-142">Wert</span><span class="sxs-lookup"><span data-stu-id="0e948-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e948-143">Header</span><span class="sxs-lookup"><span data-stu-id="0e948-143">Header</span></span><br/> | <dl> <span data-ttu-id="0e948-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e948-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e948-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0e948-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e948-146">Effekte 11-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0e948-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

