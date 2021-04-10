---
title: Simplecertselection (certselection)-Element
description: Erfahren Sie mehr über das simplecertselection (certselection)-Element. Dieses Element bestimmt, wie der Benutzer ein Zertifikat auswählt.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Simplecertselection-Element EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039619"
---
# <a name="simplecertselection-certselection-element"></a><span data-ttu-id="f2dfa-105">Simplecertselection (certselection)-Element</span><span class="sxs-lookup"><span data-stu-id="f2dfa-105">SimpleCertSelection (CertSelection) Element</span></span>

<span data-ttu-id="f2dfa-106">Das **simplecertselection (certselection)** -Element bestimmt, wie der Benutzer ein Zertifikat auswählt.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-106">The **SimpleCertSelection (CertSelection)** element determines how the user selects a certificate.</span></span>

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

<span data-ttu-id="f2dfa-107">Das **simplecertselection** -Element wird durch den komplexen [**certselection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-107">The **SimpleCertSelection** element is defined by the [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2dfa-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2dfa-108">Remarks</span></span>

<span data-ttu-id="f2dfa-109">**Simplecertselection** ist standardmäßig auf "true" fest.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-109">**SimpleCertSelection** is TRUE by default.</span></span> <span data-ttu-id="f2dfa-110">Wenn **simplecertselection** auf true festgelegt ist, führt EAP-TLS eine einfache Zertifikat Suche ohne Dropdown Listen für die Auswahl der Zertifikate durch.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-110">If **SimpleCertSelection** is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="f2dfa-111">Wenn **simplecertselection** den Wert false hat, veranschaulicht EAP-TLS dem Benutzer das geeignete Zertifikat, das ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2dfa-111">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2dfa-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2dfa-112">Requirements</span></span>



| <span data-ttu-id="f2dfa-113">Role</span><span class="sxs-lookup"><span data-stu-id="f2dfa-113">Role</span></span> | <span data-ttu-id="f2dfa-114">Mindestens unterstütztes Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f2dfa-114">Minimum supported OS</span></span> |
|------|----------------------|
| <span data-ttu-id="f2dfa-115">Client</span><span class="sxs-lookup"><span data-stu-id="f2dfa-115">Client</span></span><br/> | <span data-ttu-id="f2dfa-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2dfa-117">Server</span><span class="sxs-lookup"><span data-stu-id="f2dfa-117">Server</span></span><br/> | <span data-ttu-id="f2dfa-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2dfa-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2dfa-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2dfa-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="f2dfa-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="f2dfa-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f2dfa-121">**Certselection**</span><span class="sxs-lookup"><span data-stu-id="f2dfa-121">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

<span data-ttu-id="f2dfa-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="f2dfa-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f2dfa-123">**Certifikatestore ("kredentialssourceparameters")**</span><span class="sxs-lookup"><span data-stu-id="f2dfa-123">**CertificateStore (CredentialsSourceParameters)**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
<span data-ttu-id="f2dfa-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f2dfa-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f2dfa-125">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="f2dfa-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f2dfa-126">eaptlsconnectionpropertiesv1-Schema</span><span class="sxs-lookup"><span data-stu-id="f2dfa-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f2dfa-127">eaptlsconnectionpropertiesv1-Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="f2dfa-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





