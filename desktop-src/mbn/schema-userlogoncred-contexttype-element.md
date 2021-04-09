---
description: Enthält Anmelde Informationen für eine Verbindung.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Userlogonkred (ContextType)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129564"
---
# <a name="userlogoncred-contexttype-element"></a><span data-ttu-id="26f10-103">Userlogonkred (ContextType)-Element</span><span class="sxs-lookup"><span data-stu-id="26f10-103">UserLogonCred (contextType) Element</span></span>

<span data-ttu-id="26f10-104">Das **userlogonkred (ContextType)-** Element enthält Anmelde Informationen für eine Verbindung.</span><span class="sxs-lookup"><span data-stu-id="26f10-104">The **UserLogonCred (contextType)** element contains logon credentials for a connection.</span></span>

<span data-ttu-id="26f10-105">Dieses Element kann die folgenden untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="26f10-105">This element can have the following child elements.</span></span>

-   [<span data-ttu-id="26f10-106">**User**</span><span class="sxs-lookup"><span data-stu-id="26f10-106">**UserName**</span></span>](schema-username-userlogoncred-element.md)
-   [<span data-ttu-id="26f10-107">**Kennwort**</span><span class="sxs-lookup"><span data-stu-id="26f10-107">**Password**</span></span>](schema-password-userlogoncred-element.md)
-   [<span data-ttu-id="26f10-108">**Ignorepassword**</span><span class="sxs-lookup"><span data-stu-id="26f10-108">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md)

<span data-ttu-id="26f10-109">Dieses Element kann maximal ein Vorkommen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="26f10-109">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="26f10-110">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="26f10-110">This element is optional.</span></span>

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="26f10-111">Das **userlogonkred-** Element wird durch den komplexen [**ContextType**](schema-contexttype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="26f10-111">The **UserLogonCred** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="26f10-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26f10-112">Child elements</span></span>



| <span data-ttu-id="26f10-113">Element</span><span class="sxs-lookup"><span data-stu-id="26f10-113">Element</span></span>                                                               | <span data-ttu-id="26f10-114">type</span><span class="sxs-lookup"><span data-stu-id="26f10-114">Type</span></span>                                           | <span data-ttu-id="26f10-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26f10-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="26f10-116">**Ignorepassword**</span><span class="sxs-lookup"><span data-stu-id="26f10-116">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="26f10-117">boolean</span><span class="sxs-lookup"><span data-stu-id="26f10-117">boolean</span></span>                                        | <span data-ttu-id="26f10-118">Behandeln von Kenn Wörtern beim Aktualisieren von Profilen</span><span class="sxs-lookup"><span data-stu-id="26f10-118">How to handle passwords when upgrading profiles.</span></span><br/> |
| [<span data-ttu-id="26f10-119">**Anmelden**</span><span class="sxs-lookup"><span data-stu-id="26f10-119">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="26f10-120">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="26f10-120">string</span></span>                                         | <span data-ttu-id="26f10-121">Benutzerkennwort.</span><span class="sxs-lookup"><span data-stu-id="26f10-121">User password.</span></span><br/>                                   |
| [<span data-ttu-id="26f10-122">**User**</span><span class="sxs-lookup"><span data-stu-id="26f10-122">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="26f10-123">**nametype**</span><span class="sxs-lookup"><span data-stu-id="26f10-123">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="26f10-124">Benutzername.</span><span class="sxs-lookup"><span data-stu-id="26f10-124">User name.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="26f10-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26f10-125">Requirements</span></span>



| <span data-ttu-id="26f10-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26f10-126">Requirement</span></span> | <span data-ttu-id="26f10-127">Wert</span><span class="sxs-lookup"><span data-stu-id="26f10-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="26f10-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26f10-128">Minimum supported client</span></span><br/> | <span data-ttu-id="26f10-129">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="26f10-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="26f10-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26f10-130">Minimum supported server</span></span><br/> | <span data-ttu-id="26f10-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="26f10-131">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="26f10-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26f10-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="26f10-133">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="26f10-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="26f10-134">**contextType**</span><span class="sxs-lookup"><span data-stu-id="26f10-134">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="26f10-135">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="26f10-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="26f10-136">**Kontext (mbnprofile)**</span><span class="sxs-lookup"><span data-stu-id="26f10-136">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




