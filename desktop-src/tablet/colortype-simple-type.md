---
description: Definiert den Typ, der verwendet wird, um gültige Werte für die Farbe bestimmter Elemente in einer Journal-XML-Datei anzugeben.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: ColorType simple-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344990"
---
# <a name="colortype-simple-type"></a><span data-ttu-id="a3307-103">ColorType simple-Typ</span><span class="sxs-lookup"><span data-stu-id="a3307-103">ColorType Simple Type</span></span>

<span data-ttu-id="a3307-104">Definiert den Typ, der verwendet wird, um gültige Werte für die Farbe bestimmter Elemente in einer Journal-XML-Datei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a3307-104">Defines the type that is used to specify valid values for the color of certain elements in a Journal XML file.</span></span>

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a><span data-ttu-id="a3307-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3307-105">Remarks</span></span>

<span data-ttu-id="a3307-106">Eine Farbe kann ein Hexadezimal-RGB-Wert im Format \# RRGGBB sein.</span><span class="sxs-lookup"><span data-stu-id="a3307-106">A color can be a hexadecimal RGB value in the format \#RRGGBB.</span></span> <span data-ttu-id="a3307-107">Er muss dem folgenden regulären Ausdruck entsprechen: \# \[ 0-9a-FA-F \] {6} .</span><span class="sxs-lookup"><span data-stu-id="a3307-107">It must match the following regular expression: \#\[0-9a-fA-F\]{6}.</span></span> <span data-ttu-id="a3307-108">Beispiel: " \# 4a79b5".</span><span class="sxs-lookup"><span data-stu-id="a3307-108">For example: "\#4a79B5".</span></span>

## <a name="requirements"></a><span data-ttu-id="a3307-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3307-109">Requirements</span></span>



| <span data-ttu-id="a3307-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3307-110">Requirement</span></span> | <span data-ttu-id="a3307-111">Wert</span><span class="sxs-lookup"><span data-stu-id="a3307-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a3307-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3307-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a3307-113">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3307-113">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a3307-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3307-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a3307-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a3307-115">None supported</span></span><br/>                                     |



 

 




