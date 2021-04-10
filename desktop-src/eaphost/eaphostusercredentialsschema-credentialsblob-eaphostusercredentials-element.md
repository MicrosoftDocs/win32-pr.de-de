---
title: Das Element "kredentialsblob" (eaphustuseranmeldeinformationen)
description: Wird verwendet, wenn die Methoden Konfiguration ein binäres Blob anstelle von im XML-Textformat ist.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Kredentialsblob-Element EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103238"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a><span data-ttu-id="43dd3-104">Das Element "kredentialsblob" (eaphustuseranmeldeinformationen)</span><span class="sxs-lookup"><span data-stu-id="43dd3-104">CredentialsBlob (EapHostUserCredentials) Element</span></span>

<span data-ttu-id="43dd3-105">Das Element " **kredentialsblob" (eaptustuseranmeldeinformationen)** wird verwendet, wenn die Methoden Konfiguration ein binäres Blob anstelle von XML-Textformat ist.</span><span class="sxs-lookup"><span data-stu-id="43dd3-105">The **CredentialsBlob (EapHostUserCredentials)** element is used when the method configuration is a binary BLOB instead of in XML text format.</span></span>

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="43dd3-106">Das Element " **kredentialsblob** " wird durch das [**eaphustuseranmelde**](eaphostusercredentialsschema-eaphostusercredentials-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="43dd3-106">The **CredentialsBlob** element is defined by the [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="43dd3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43dd3-107">Remarks</span></span>

<span data-ttu-id="43dd3-108">Die Elemente "- [**Anmelde**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) Informationen" und " **kredentialsblob** " können nicht gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43dd3-108">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and **CredentialsBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="43dd3-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43dd3-109">Requirements</span></span>



| <span data-ttu-id="43dd3-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43dd3-110">Requirement</span></span> | <span data-ttu-id="43dd3-111">Wert</span><span class="sxs-lookup"><span data-stu-id="43dd3-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43dd3-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43dd3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="43dd3-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43dd3-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43dd3-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43dd3-114">Minimum supported server</span></span><br/> | <span data-ttu-id="43dd3-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43dd3-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43dd3-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43dd3-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="43dd3-117">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="43dd3-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="43dd3-118">**Eaphustuseranmeldeinformationen**</span><span class="sxs-lookup"><span data-stu-id="43dd3-118">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

<span data-ttu-id="43dd3-119">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="43dd3-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="43dd3-120">**Eaphustuseranmeldeinformationen**</span><span class="sxs-lookup"><span data-stu-id="43dd3-120">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[<span data-ttu-id="43dd3-121">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="43dd3-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="43dd3-122">eaphustuseranmelde-Schema</span><span class="sxs-lookup"><span data-stu-id="43dd3-122">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





