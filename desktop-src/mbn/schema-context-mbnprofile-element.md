---
description: Gibt die Parameter an, die zum Einrichten einer Datenverbindung erforderlich sind.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Context (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372841"
---
# <a name="context-mbnprofile-element"></a><span data-ttu-id="a315e-103">Context (mbnprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="a315e-103">Context (MBNProfile) Element</span></span>

<span data-ttu-id="a315e-104">Das **context (mbnprofile)** -Element gibt die Parameter an, die zum Einrichten einer Datenverbindung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a315e-104">The **Context (MBNProfile)** element specifies the parameters required to setup a data connection.</span></span>

<span data-ttu-id="a315e-105">Das-Element kann die folgenden untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a315e-105">The element can have the following child elements.</span></span>

-   [<span data-ttu-id="a315e-106">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="a315e-106">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)
-   [<span data-ttu-id="a315e-107">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="a315e-107">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
-   [<span data-ttu-id="a315e-108">**Komprimi**</span><span class="sxs-lookup"><span data-stu-id="a315e-108">**Compression**</span></span>](schema-compression-contexttype-element.md)
-   [<span data-ttu-id="a315e-109">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="a315e-109">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)

<span data-ttu-id="a315e-110">Dieses Element kann maximal ein Vorkommen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a315e-110">This element can have a maximum of one occurrence.</span></span>

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

<span data-ttu-id="a315e-111">Das **Kontext** Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="a315e-111">The **Context** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a315e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a315e-112">Requirements</span></span>



| <span data-ttu-id="a315e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a315e-113">Requirement</span></span> | <span data-ttu-id="a315e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a315e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a315e-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a315e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a315e-116">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a315e-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a315e-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a315e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a315e-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a315e-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="a315e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a315e-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="a315e-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="a315e-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a315e-121">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="a315e-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="a315e-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="a315e-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a315e-123">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="a315e-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




