---
description: Beschreibt die von einem Effekt Objekt verwendeten Präprozessordefinitionen.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: D3DXMACRO-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363995"
---
# <a name="d3dxmacro-structure"></a><span data-ttu-id="90ff0-103">D3DXMACRO-Struktur</span><span class="sxs-lookup"><span data-stu-id="90ff0-103">D3DXMACRO structure</span></span>

<span data-ttu-id="90ff0-104">Beschreibt die von einem Effekt Objekt verwendeten Präprozessordefinitionen.</span><span class="sxs-lookup"><span data-stu-id="90ff0-104">Describes preprocessor definitions used by an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ff0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="90ff0-105">Syntax</span></span>


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a><span data-ttu-id="90ff0-106">Member</span><span class="sxs-lookup"><span data-stu-id="90ff0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="90ff0-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="90ff0-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="90ff0-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90ff0-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90ff0-109">Der präprozessorname.</span><span class="sxs-lookup"><span data-stu-id="90ff0-109">Preprocessor name.</span></span>

</dd> <dt>

<span data-ttu-id="90ff0-110">**Definition**</span><span class="sxs-lookup"><span data-stu-id="90ff0-110">**Definition**</span></span>
</dt> <dd>

<span data-ttu-id="90ff0-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="90ff0-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90ff0-112">Definitions Name.</span><span class="sxs-lookup"><span data-stu-id="90ff0-112">Definition name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90ff0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90ff0-113">Remarks</span></span>

<span data-ttu-id="90ff0-114">Um **D3DXMACRO** s in mehr als einer Zeile zu verwenden, stellen Sie jedem neuen Zeilenzeichen einen umgekehrten Schrägstrich (wie z \# . b. eine Definition in der Programmiersprache C) voran.</span><span class="sxs-lookup"><span data-stu-id="90ff0-114">To use **D3DXMACRO** s in more than one line, prefix each new line character with a backslash (like a \#define in the C language).</span></span> <span data-ttu-id="90ff0-115">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="90ff0-115">For example:</span></span>


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



<span data-ttu-id="90ff0-116">Beachten Sie die drei umgekehrten Schrägstriche am Ende der Zeile.</span><span class="sxs-lookup"><span data-stu-id="90ff0-116">Notice the 3 backslash characters at the end of the line.</span></span> <span data-ttu-id="90ff0-117">Die ersten beiden sind erforderlich, um ein einzelnes ' \\ ', gefolgt vom Zeilen vorzeilenzeichen " \\ n" auszugeben.</span><span class="sxs-lookup"><span data-stu-id="90ff0-117">The first two are required to output a single '\\', followed by the newline character "\\n".</span></span> <span data-ttu-id="90ff0-118">Optional können Sie auch Ihre Zeilen mit " \\ \\ \\ r \\ n" beenden.</span><span class="sxs-lookup"><span data-stu-id="90ff0-118">Optionally, you may also want to terminate your lines using "\\\\\\r\\n".</span></span>

## <a name="requirements"></a><span data-ttu-id="90ff0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90ff0-119">Requirements</span></span>



| <span data-ttu-id="90ff0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90ff0-120">Requirement</span></span> | <span data-ttu-id="90ff0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="90ff0-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ff0-122">Header</span><span class="sxs-lookup"><span data-stu-id="90ff0-122">Header</span></span><br/> | <dl> <span data-ttu-id="90ff0-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ff0-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ff0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90ff0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ff0-125">Effekt Strukturen</span><span class="sxs-lookup"><span data-stu-id="90ff0-125">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="90ff0-126">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="90ff0-126">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
