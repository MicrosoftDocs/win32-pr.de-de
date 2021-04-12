---
description: Enthält Einstellungen für medienspezifische Module (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: MSM-Element (lanprofile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216924"
---
# <a name="msm-lanprofile-element"></a><span data-ttu-id="eb6e6-103">MSM-Element (lanprofile)</span><span class="sxs-lookup"><span data-stu-id="eb6e6-103">MSM (LANProfile) Element</span></span>

<span data-ttu-id="eb6e6-104">Das MSM-Element (lanprofile) enthält Einstellungen für medienspezifische Module (MSM).</span><span class="sxs-lookup"><span data-stu-id="eb6e6-104">The MSM (LANProfile) element contains media-specific module (MSM) settings.</span></span>

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="security">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OneXEnforced"
                            type="boolean"
                         />
                        <xs:element name="OneXEnabled"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="eb6e6-105">Das **MSM** -Element wird durch das [**lanprofile**](lan-profileschema-lanprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="eb6e6-105">The **MSM** element is defined by the [**LANProfile**](lan-profileschema-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="eb6e6-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb6e6-106">Child elements</span></span>



| <span data-ttu-id="eb6e6-107">Element</span><span class="sxs-lookup"><span data-stu-id="eb6e6-107">Element</span></span>                                                                 | <span data-ttu-id="eb6e6-108">type</span><span class="sxs-lookup"><span data-stu-id="eb6e6-108">Type</span></span>    | <span data-ttu-id="eb6e6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb6e6-109">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb6e6-110">**Onexaktiviert**</span><span class="sxs-lookup"><span data-stu-id="eb6e6-110">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="eb6e6-111">boolean</span><span class="sxs-lookup"><span data-stu-id="eb6e6-111">boolean</span></span> | <span data-ttu-id="eb6e6-112">Gibt an, ob der Dienst für die automatische Konfiguration von Kabel Netzwerken mithilfe von 802.1 x eine Port Authentifizierung durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="eb6e6-112">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span><br/>       |
| [<span data-ttu-id="eb6e6-113">**Onexerzwungen**</span><span class="sxs-lookup"><span data-stu-id="eb6e6-113">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="eb6e6-114">boolean</span><span class="sxs-lookup"><span data-stu-id="eb6e6-114">boolean</span></span> | <span data-ttu-id="eb6e6-115">Gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="eb6e6-115">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="eb6e6-116">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="eb6e6-116">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="eb6e6-117">Enthält Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="eb6e6-117">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="eb6e6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb6e6-118">Requirements</span></span>



| <span data-ttu-id="eb6e6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb6e6-119">Requirement</span></span> | <span data-ttu-id="eb6e6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="eb6e6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eb6e6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb6e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eb6e6-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb6e6-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eb6e6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb6e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eb6e6-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb6e6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb6e6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb6e6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb6e6-126">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="eb6e6-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="eb6e6-127">**Lanprofile**</span><span class="sxs-lookup"><span data-stu-id="eb6e6-127">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="eb6e6-128">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="eb6e6-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="eb6e6-129">**Lanprofile**</span><span class="sxs-lookup"><span data-stu-id="eb6e6-129">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




