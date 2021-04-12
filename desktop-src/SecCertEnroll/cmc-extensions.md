---
description: Erweiterungen sind in einer CMC-Anforderung enthalten, indem Sie der taggedattributes-Struktur hinzugefügt werden, wie im folgenden ASN. 1-Syntax Beispiel gezeigt. Weitere Informationen finden Sie im Thema Attribute.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: CMC-Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217157"
---
# <a name="cmc-extensions"></a><span data-ttu-id="43dba-104">CMC-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="43dba-104">CMC Extensions</span></span>

<span data-ttu-id="43dba-105">Erweiterungen sind in einer CMC-Anforderung enthalten, indem Sie der **taggedattributes** -Struktur hinzugefügt werden, wie im folgenden ASN. 1-Syntax Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="43dba-105">Extensions are included in a CMC request by adding them to the **TaggedAttributes** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="43dba-106">Weitere Informationen finden Sie im Thema [Attribute](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="43dba-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

<span data-ttu-id="43dba-107">Jede Struktur in der **taggedattributes-Auflistung** enthält eine ganzzahlige ID, eine ASN. 1-Objekt Kennung (OID) und einen Satz von Werten.</span><span class="sxs-lookup"><span data-stu-id="43dba-107">Each structure in the **TaggedAttributes** collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="43dba-108">Erweiterungen werden in eine Anforderung eingefügt, indem dem Feld **Werte** eine **cmcaddextensions** -Struktur hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="43dba-108">Extensions are incorporated into a request by adding a **CmcAddExtensions** structure to the **values** field.</span></span> <span data-ttu-id="43dba-109">Die ASN. 1-Struktur Syntax wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="43dba-109">The ASN.1 structure syntax is shown in the following example.</span></span> <span data-ttu-id="43dba-110">Der Objekt Bezeichner ist **XCN \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).</span><span class="sxs-lookup"><span data-stu-id="43dba-110">The object identifier is **XCN\_OID\_CMC\_ADD\_EXTENSIONS** (1.3.6.1.5.5.7.7.8).</span></span>

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

<span data-ttu-id="43dba-111">Im folgenden Verfahren wird erläutert, wie Sie die Zertifikatregistrierungs-API verwenden, um einer CMC-Zertifikat Anforderung Erweiterungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="43dba-111">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a CMC certificate request.</span></span>

<span data-ttu-id="43dba-112">**So verwenden Sie die Zertifikatregistrierungs-API zum Hinzufügen von Erweiterungen zu einer CMC-Zertifikat Anforderung**</span><span class="sxs-lookup"><span data-stu-id="43dba-112">**To use the Certificate Enrollment API to add extensions to a CMC certificate request**</span></span>

1.  <span data-ttu-id="43dba-113">Erstellen Sie eine Erweiterung mithilfe einer der verfügbaren Schnittstellen, die von der [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) -Schnittstelle abgeleitet werden, oder verwenden Sie das **IX509Extension** -Objekt direkt zum Erstellen benutzerdefinierter Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="43dba-113">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface or use the **IX509Extension** object directly to create custom extensions.</span></span>
2.  <span data-ttu-id="43dba-114">Rufen Sie die [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) -Eigenschaft des [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekts auf, um eine [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="43dba-114">Call the [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) property on the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object to retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
3.  <span data-ttu-id="43dba-115">Fügen Sie die in Schritt 1 erstellten Erweiterungen der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung hinzu.</span><span class="sxs-lookup"><span data-stu-id="43dba-115">Add the extensions created in step 1 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
4.  <span data-ttu-id="43dba-116">Melden [**Sie sich**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) an, um automatisch die folgenden Aktionen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="43dba-116">Call [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) to automatically perform the following actions:</span></span>
    -   <span data-ttu-id="43dba-117">Rufen Sie ein [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Objekt aus dem [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="43dba-117">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
    -   <span data-ttu-id="43dba-118">Erstellen und initialisieren Sie ein [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Objekt mithilfe der [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) -Auflistung, die Sie in Schritt 2 abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="43dba-118">Create and initialize an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object by using the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 2.</span></span>
    -   <span data-ttu-id="43dba-119">Erstellen Sie eine [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Sammlung, und fügen Sie Ihr das [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) -Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="43dba-119">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object to it.</span></span>
    -   <span data-ttu-id="43dba-120">Verwenden Sie die [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) -Auflistung, um ein [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="43dba-120">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
    -   <span data-ttu-id="43dba-121">Fügen Sie das [**icryptattribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) -Objekt der [**icryptattributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) -Auflistung hinzu.</span><span class="sxs-lookup"><span data-stu-id="43dba-121">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43dba-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43dba-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43dba-123">Attribute</span><span class="sxs-lookup"><span data-stu-id="43dba-123">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="43dba-124">Attribut Architektur</span><span class="sxs-lookup"><span data-stu-id="43dba-124">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="43dba-125">CMC-Attribute</span><span class="sxs-lookup"><span data-stu-id="43dba-125">CMC Attributes</span></span>](cmc-attributes.md)
</dt> <dt>

[<span data-ttu-id="43dba-126">Extensions (Erweiterungen)</span><span class="sxs-lookup"><span data-stu-id="43dba-126">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



