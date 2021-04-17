---
title: Benutzerdefinierter Typ
description: Verwenden Sie die folgende Syntax, um einen benutzerdefinierten Typ zu deklarieren.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388105"
---
# <a name="user-defined-type"></a><span data-ttu-id="8328e-103">Benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="8328e-103">User-Defined Type</span></span>

<span data-ttu-id="8328e-104">Verwenden Sie die folgende Syntax, um einen benutzerdefinierten Typ zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="8328e-104">Use the following syntax to declare a user-defined type.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="8328e-105">typedef konstanter **\[ \] Typname \[ \] Index**;</span><span class="sxs-lookup"><span data-stu-id="8328e-105">typedef **\[const\] Type Name\[Index\]**;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="8328e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8328e-106">Parameters</span></span>



| <span data-ttu-id="8328e-107">Element</span><span class="sxs-lookup"><span data-stu-id="8328e-107">Item</span></span>                                                                                         | <span data-ttu-id="8328e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8328e-108">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8328e-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span><span class="sxs-lookup"><span data-stu-id="8328e-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span></span><br/>                 | <span data-ttu-id="8328e-110">Optional.</span><span class="sxs-lookup"><span data-stu-id="8328e-110">Optional.</span></span> <span data-ttu-id="8328e-111">Dieses Schlüsselwort kennzeichnet den Typ explizit als Konstante.</span><span class="sxs-lookup"><span data-stu-id="8328e-111">This keyword explicitly marks the type as a constant.</span></span><br/>             |
| <span data-ttu-id="8328e-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Sorte**</span><span class="sxs-lookup"><span data-stu-id="8328e-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="8328e-113">Identifiziert den Datentyp. muss einer der systeminternen HLSL-Datentypen sein.</span><span class="sxs-lookup"><span data-stu-id="8328e-113">Identifies the data type; must be one of the HLSL intrinsic data types.</span></span><br/>     |
| <span data-ttu-id="8328e-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="8328e-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="8328e-115">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8328e-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="8328e-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Sin**</span><span class="sxs-lookup"><span data-stu-id="8328e-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**</span></span><br/> | <span data-ttu-id="8328e-117">Optionale Array Größe.</span><span class="sxs-lookup"><span data-stu-id="8328e-117">Optional array size.</span></span> <span data-ttu-id="8328e-118">Muss eine ganze Zahl ohne Vorzeichen zwischen 1 und 4 sein.</span><span class="sxs-lookup"><span data-stu-id="8328e-118">Must be an unsigned integer between 1 and 4 inclusive.</span></span><br/> |



 

<span data-ttu-id="8328e-119">Neben den integrierten systeminternen Datentypen unterstützt HLSL benutzerdefinierte oder benutzerdefinierte Typen, die dieser Syntax folgen:</span><span class="sxs-lookup"><span data-stu-id="8328e-119">In addition to the built-in intrinsic data types, HLSL supports user-defined or custom types which follow this syntax:</span></span>

## <a name="remarks"></a><span data-ttu-id="8328e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8328e-120">Remarks</span></span>

<span data-ttu-id="8328e-121">Bei benutzerdefinierten Typen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8328e-121">User-defined types are not case-sensitive.</span></span> <span data-ttu-id="8328e-122">Die folgenden Typen werden aus Gründen der Unterstützung automatisch in einem Superglobalen Gültigkeitsbereich definiert.</span><span class="sxs-lookup"><span data-stu-id="8328e-122">For convenience, the following types are automatically defined at super-global scope.</span></span>


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



<span data-ttu-id="8328e-123">Das Nummern Zeichen ( \# ) stellt eine ganzzahlige Ziffer zwischen 1 und 4 dar.</span><span class="sxs-lookup"><span data-stu-id="8328e-123">The pound sign (\#) represents an integer digit between 1 and 4.</span></span>

<span data-ttu-id="8328e-124">Aus Kompatibilitätsgründen mit DirectX 8-Effekten werden die folgenden Typen automatisch im superglobalen Bereich definiert:</span><span class="sxs-lookup"><span data-stu-id="8328e-124">For compatibility with DirectX 8 effects, the following types are automatically defined at super-global scope:</span></span>


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a><span data-ttu-id="8328e-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8328e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8328e-126">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8328e-126">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





