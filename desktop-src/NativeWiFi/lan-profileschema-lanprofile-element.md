---
description: Enthält ein kabelgebundenes Netzwerk Profil.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Lanprofile-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216926"
---
# <a name="lanprofile-element"></a><span data-ttu-id="226c6-103">Lanprofile-Element</span><span class="sxs-lookup"><span data-stu-id="226c6-103">LANProfile Element</span></span>

<span data-ttu-id="226c6-104">Das lanprofile-Element enthält ein kabelgebundenes Netzwerk Profil.</span><span class="sxs-lookup"><span data-stu-id="226c6-104">The LANProfile element contains a wired network profile.</span></span> <span data-ttu-id="226c6-105">Dieses Element ist das eindeutige root-Element für ein Kabelnetzwerk Profil.</span><span class="sxs-lookup"><span data-stu-id="226c6-105">This element is the unique root element for a wired network profile.</span></span>

<span data-ttu-id="226c6-106">Der Ziel Namespace für das lanprofile-Element ist `https://www.microsoft.com/networking/LAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="226c6-106">The target namespace for the LANProfile element is `https://www.microsoft.com/networking/LAN/profile/v1`.</span></span>

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
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

## <a name="child-elements"></a><span data-ttu-id="226c6-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="226c6-107">Child elements</span></span>



| <span data-ttu-id="226c6-108">Element</span><span class="sxs-lookup"><span data-stu-id="226c6-108">Element</span></span>                                                                 | <span data-ttu-id="226c6-109">type</span><span class="sxs-lookup"><span data-stu-id="226c6-109">Type</span></span>    | <span data-ttu-id="226c6-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="226c6-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="226c6-111">**MSM**</span><span class="sxs-lookup"><span data-stu-id="226c6-111">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)                 |         | <span data-ttu-id="226c6-112">Enthält Einstellungen für medienspezifische Module (MSM).</span><span class="sxs-lookup"><span data-stu-id="226c6-112">Contains media-specific module (MSM) settings.</span></span> <br/>                                                                               |
| [<span data-ttu-id="226c6-113">**Onexaktiviert**</span><span class="sxs-lookup"><span data-stu-id="226c6-113">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="226c6-114">boolean</span><span class="sxs-lookup"><span data-stu-id="226c6-114">boolean</span></span> | <span data-ttu-id="226c6-115">Gibt an, ob der Dienst für die automatische Konfiguration von Kabel Netzwerken mithilfe von 802.1 x eine Port Authentifizierung durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="226c6-115">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="226c6-116">**Onexerzwungen**</span><span class="sxs-lookup"><span data-stu-id="226c6-116">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="226c6-117">boolean</span><span class="sxs-lookup"><span data-stu-id="226c6-117">boolean</span></span> | <span data-ttu-id="226c6-118">Gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="226c6-118">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="226c6-119">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="226c6-119">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="226c6-120">Enthält Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="226c6-120">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="226c6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="226c6-121">Remarks</span></span>

<span data-ttu-id="226c6-122">Informationen zum Anzeigen der Liste der untergeordneten Elemente in einer Struktur ähnlichen Struktur finden Sie unter [LAN- \_ Profil Schema Elemente](lan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="226c6-122">To view the list of child elements in a tree-like structure, see [LAN\_profile Schema Elements](lan-profileschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="226c6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="226c6-123">Requirements</span></span>



| <span data-ttu-id="226c6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="226c6-124">Requirement</span></span> | <span data-ttu-id="226c6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="226c6-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="226c6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="226c6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="226c6-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="226c6-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="226c6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="226c6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="226c6-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="226c6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




