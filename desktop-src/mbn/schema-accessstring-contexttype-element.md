---
description: Identifiziert die APN-oder Dial-Zeichenfolge, die zum Herstellen einer Datenverbindung verwendet werden soll.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Accessstring (ContextType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355489"
---
# <a name="accessstring-contexttype-element"></a><span data-ttu-id="a99e5-103">Accessstring (ContextType)-Element</span><span class="sxs-lookup"><span data-stu-id="a99e5-103">AccessString (contextType) Element</span></span>

<span data-ttu-id="a99e5-104">Das **accessstring-Element (ContextType)** identifiziert die APN-oder Dial-Zeichenfolge, die zum Herstellen einer Datenverbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a99e5-104">The **AccessString (contextType)** element identifies the APN or dial string to be used to establish a data connection.</span></span>

<span data-ttu-id="a99e5-105">Dieses Element kann eine maximale Länge von 100 Zeichen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a99e5-105">This element can have a maximum length of 100 characters.</span></span>

<span data-ttu-id="a99e5-106">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a99e5-106">This element is optional.</span></span>

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="a99e5-107">Das **accessstring** -Element wird durch den komplexen [**ContextType**](schema-contexttype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a99e5-107">The **AccessString** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a99e5-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a99e5-108">Requirements</span></span>



| <span data-ttu-id="a99e5-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a99e5-109">Requirement</span></span> | <span data-ttu-id="a99e5-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a99e5-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a99e5-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a99e5-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a99e5-112">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a99e5-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a99e5-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a99e5-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a99e5-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a99e5-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="a99e5-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a99e5-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="a99e5-116">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="a99e5-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a99e5-117">**contextType**</span><span class="sxs-lookup"><span data-stu-id="a99e5-117">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="a99e5-118">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="a99e5-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a99e5-119">**Kontext (mbnprofile)**</span><span class="sxs-lookup"><span data-stu-id="a99e5-119">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




