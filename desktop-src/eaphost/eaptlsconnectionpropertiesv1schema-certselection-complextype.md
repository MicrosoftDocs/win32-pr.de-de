---
title: Komplexer certselection-Typ
description: Erfahren Sie mehr über den komplexen certselection-Typ. Dieser Typ bestimmt, wie der Benutzer ein Zertifikat auswählt.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- Komplexer certselection-Typ EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316473"
---
# <a name="certselection-complex-type"></a><span data-ttu-id="68fa0-105">Komplexer certselection-Typ</span><span class="sxs-lookup"><span data-stu-id="68fa0-105">CertSelection Complex Type</span></span>

<span data-ttu-id="68fa0-106">Der komplexe Typ " **certselection** " legt fest, wie der Benutzer ein Zertifikat auswählt.</span><span class="sxs-lookup"><span data-stu-id="68fa0-106">The **CertSelection** complex type determines how the user selects a certificate.</span></span>

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="68fa0-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68fa0-107">Child elements</span></span>



| <span data-ttu-id="68fa0-108">Element</span><span class="sxs-lookup"><span data-stu-id="68fa0-108">Element</span></span>                                                                                                     | <span data-ttu-id="68fa0-109">type</span><span class="sxs-lookup"><span data-stu-id="68fa0-109">Type</span></span>    | <span data-ttu-id="68fa0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68fa0-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68fa0-111">**Simplecertselection**</span><span class="sxs-lookup"><span data-stu-id="68fa0-111">**SimpleCertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | <span data-ttu-id="68fa0-112">boolean</span><span class="sxs-lookup"><span data-stu-id="68fa0-112">boolean</span></span> | <span data-ttu-id="68fa0-113">Ist standardmäßig "true".</span><span class="sxs-lookup"><span data-stu-id="68fa0-113">Is TRUE by default.</span></span> <span data-ttu-id="68fa0-114">Wenn [**simplecertselection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) auf true festgelegt ist, führt EAP-TLS eine einfache Zertifikat Suche ohne Dropdown Listen für die Auswahl der Zertifikate durch.</span><span class="sxs-lookup"><span data-stu-id="68fa0-114">If [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="68fa0-115">Wenn **simplecertselection** den Wert false hat, veranschaulicht EAP-TLS dem Benutzer das geeignete Zertifikat, das ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="68fa0-115">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="68fa0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68fa0-116">Requirements</span></span>



| <span data-ttu-id="68fa0-117">Role</span><span class="sxs-lookup"><span data-stu-id="68fa0-117">Role</span></span> | <span data-ttu-id="68fa0-118">Mindestens unterstützte Betriebssystemversion</span><span class="sxs-lookup"><span data-stu-id="68fa0-118">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="68fa0-119">Client</span><span class="sxs-lookup"><span data-stu-id="68fa0-119">Client</span></span><br/> | <span data-ttu-id="68fa0-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68fa0-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68fa0-121">Server</span><span class="sxs-lookup"><span data-stu-id="68fa0-121">Server</span></span><br/> | <span data-ttu-id="68fa0-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68fa0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68fa0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68fa0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68fa0-124">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="68fa0-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="68fa0-125">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="68fa0-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="68fa0-126">komplexe eaptlsconnectionpropertiesv1-Schema Typen</span><span class="sxs-lookup"><span data-stu-id="68fa0-126">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





