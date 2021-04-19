---
description: Gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Authprotocol-Element (ContextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348768"
---
# <a name="authprotocol-contexttype-element"></a><span data-ttu-id="61211-103">Authprotocol-Element (ContextType)</span><span class="sxs-lookup"><span data-stu-id="61211-103">AuthProtocol (contextType) Element</span></span>

<span data-ttu-id="61211-104">Das **authprotocol (ContextType)** -Element gibt das Authentifizierungsprotokoll an, das zum Aktivieren eines PDP-Kontexts (Packet Data Protocol) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="61211-104">The **AuthProtocol (contextType)** element specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="61211-105">Das-Element kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="61211-105">The element can have one of the following values.</span></span>

| <span data-ttu-id="61211-106">Wert</span><span class="sxs-lookup"><span data-stu-id="61211-106">Value</span></span>      | <span data-ttu-id="61211-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="61211-107">Meaning</span></span>                                                                 |
|------------|-------------------------------------------------------------------------|
| <span data-ttu-id="61211-108">Gar</span><span class="sxs-lookup"><span data-stu-id="61211-108">"NONE"</span></span>     | <span data-ttu-id="61211-109">Kein Authentifizierungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="61211-109">No authentication protocol.</span></span>                                             |
| <span data-ttu-id="61211-110">PAP</span><span class="sxs-lookup"><span data-stu-id="61211-110">"PAP"</span></span>      | <span data-ttu-id="61211-111">Unverschlüsselte Kenn Wort Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="61211-111">Unencrypted password authentication.</span></span>                                    |
| <span data-ttu-id="61211-112">CHAP</span><span class="sxs-lookup"><span data-stu-id="61211-112">"CHAP"</span></span>     | <span data-ttu-id="61211-113">Challenge Handshake Authentication-Protokoll (CHAP).</span><span class="sxs-lookup"><span data-stu-id="61211-113">Challenge Handshake Authentication Protocol(CHAP).</span></span>                      |
|  <span data-ttu-id="61211-114">MsCHAPV2</span><span class="sxs-lookup"><span data-stu-id="61211-114">MsCHAPV2"</span></span> | <span data-ttu-id="61211-115">Verwenden Sie das Microsoft s Challenge Handshake Authentication-Protokoll (CHAP) v 2.0.</span><span class="sxs-lookup"><span data-stu-id="61211-115">Use Microsoft s Challenge Handshake Authentication Protocol(CHAP) v2.0.</span></span> |



 

<span data-ttu-id="61211-116">Dieses Element ist optional und wird nur für GSM-Profile verwendet.</span><span class="sxs-lookup"><span data-stu-id="61211-116">This element is optional and is used only for GSM profiles.</span></span> <span data-ttu-id="61211-117">Wenn das Element nicht angegeben und das Profil für ein GSM-Gerät verwendet wird, verwendet der Mobile Breitbanddienst den Wert **"None"**.</span><span class="sxs-lookup"><span data-stu-id="61211-117">If the element is not specified and the profile is for a GSM device, then the Mobile Broadband service will use **"NONE"**.</span></span>

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="61211-118">Das **authprotocol** -Element wird durch den komplexen [**ContextType**](schema-contexttype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="61211-118">The **AuthProtocol** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="61211-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61211-119">Requirements</span></span>



| <span data-ttu-id="61211-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61211-120">Requirement</span></span> | <span data-ttu-id="61211-121">Wert</span><span class="sxs-lookup"><span data-stu-id="61211-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="61211-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61211-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61211-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="61211-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="61211-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61211-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61211-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="61211-125">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="61211-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61211-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="61211-127">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="61211-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="61211-128">**contextType**</span><span class="sxs-lookup"><span data-stu-id="61211-128">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="61211-129">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="61211-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="61211-130">**Kontext (mbnprofile)**</span><span class="sxs-lookup"><span data-stu-id="61211-130">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




