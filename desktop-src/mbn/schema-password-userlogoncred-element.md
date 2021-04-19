---
description: Gibt das Kennwort an, das zum Authentifizieren eines Benutzers verwendet wird.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Password (userlogonkred)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346307"
---
# <a name="password-userlogoncred-element"></a><span data-ttu-id="41c69-103">Password (userlogonkred)-Element</span><span class="sxs-lookup"><span data-stu-id="41c69-103">Password (UserLogonCred) Element</span></span>

<span data-ttu-id="41c69-104">Das [**Kennwort (userlogonkred)-**](schema-ignorepassword-userlogoncred-element.md) Element gibt das Kennwort an, das zum Authentifizieren eines Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41c69-104">The [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) element specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="41c69-105">Das-Element ist eine Zeichenfolge mit bis zu 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="41c69-105">The element is a string of up to 255 characters.</span></span>

<span data-ttu-id="41c69-106">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="41c69-106">This element is optional.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="41c69-107">Das **Password** -Element wird durch das [**userlogonkred-**](schema-userlogoncred-contexttype-element.md) Element definiert.</span><span class="sxs-lookup"><span data-stu-id="41c69-107">The **Password** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c69-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41c69-108">Requirements</span></span>



| <span data-ttu-id="41c69-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41c69-109">Requirement</span></span> | <span data-ttu-id="41c69-110">Wert</span><span class="sxs-lookup"><span data-stu-id="41c69-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="41c69-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41c69-111">Minimum supported client</span></span><br/> | <span data-ttu-id="41c69-112">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="41c69-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="41c69-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41c69-113">Minimum supported server</span></span><br/> | <span data-ttu-id="41c69-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="41c69-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="41c69-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41c69-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="41c69-116">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="41c69-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="41c69-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="41c69-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="41c69-118">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="41c69-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="41c69-119">**Userlogonkred (ContextType)**</span><span class="sxs-lookup"><span data-stu-id="41c69-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




