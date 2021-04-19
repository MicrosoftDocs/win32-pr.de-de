---
description: Gibt an, wie Kenn Wörter beim Aktualisieren von Profilen behandelt werden.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Ignorepassword (userlogonkred)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350461"
---
# <a name="ignorepassword-userlogoncred-element"></a><span data-ttu-id="eda0a-103">Ignorepassword (userlogonkred)-Element</span><span class="sxs-lookup"><span data-stu-id="eda0a-103">IgnorePassword (UserLogonCred) Element</span></span>

<span data-ttu-id="eda0a-104">Das **ignorepassword (userlogonkred)-** Element gibt an, wie Kenn Wörter beim Aktualisieren von Profilen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="eda0a-104">The **IgnorePassword (UserLogonCred)** element specifies how to handle passwords when upgrading profiles.</span></span>

<span data-ttu-id="eda0a-105">Wenn diese Einstellung auf " **true** " festgelegt ist und zum Zeitpunkt des Aktualisierungs Vorgangs ein Profil mit demselben Namen vorhanden ist, wird das Kennwort aus diesem Profil übernommen und in einem neuen Profil gespeichert.</span><span class="sxs-lookup"><span data-stu-id="eda0a-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in new profile.</span></span>

<span data-ttu-id="eda0a-106">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="eda0a-106">This element is optional.</span></span>

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

<span data-ttu-id="eda0a-107">Das **ignorepassword** -Element wird durch das [**userlogonkred-**](schema-userlogoncred-contexttype-element.md) Element definiert.</span><span class="sxs-lookup"><span data-stu-id="eda0a-107">The **IgnorePassword** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="eda0a-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eda0a-108">Requirements</span></span>



| <span data-ttu-id="eda0a-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eda0a-109">Requirement</span></span> | <span data-ttu-id="eda0a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="eda0a-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="eda0a-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eda0a-111">Minimum supported client</span></span><br/> | <span data-ttu-id="eda0a-112">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="eda0a-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="eda0a-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eda0a-113">Minimum supported server</span></span><br/> | <span data-ttu-id="eda0a-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eda0a-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="eda0a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eda0a-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="eda0a-116">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="eda0a-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="eda0a-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="eda0a-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="eda0a-118">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="eda0a-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="eda0a-119">**Userlogonkred (ContextType)**</span><span class="sxs-lookup"><span data-stu-id="eda0a-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




