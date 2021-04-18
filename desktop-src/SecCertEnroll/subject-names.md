---
description: Das Feld Betreff einer PKCS \# 10-Zertifikat Anforderung enthält den Distinguished Name der Entität, die das Zertifikat anfordert.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Antragstellernamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351762"
---
# <a name="subject-names"></a><span data-ttu-id="7f922-103">Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="7f922-103">Subject Names</span></span>

<span data-ttu-id="7f922-104">Das Feld **Betreff** einer PKCS \# 10-Zertifikat Anforderung enthält den Distinguished Name der Entität, die das Zertifikat anfordert.</span><span class="sxs-lookup"><span data-stu-id="7f922-104">The **subject** field of a PKCS \#10 certificate request contains the distinguished name of the entity requesting the certificate.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

<span data-ttu-id="7f922-105">Der Distinguished Name besteht aus einer Sequenz von relativen Distinguished Names (rDNS).</span><span class="sxs-lookup"><span data-stu-id="7f922-105">The distinguished name consists of a sequence of relative distinguished names (RDNs).</span></span> <span data-ttu-id="7f922-106">Jeder RDN besteht aus einem Satz von Attributen, und jedes Attribut besteht aus einem Objekt Bezeichner und einem Wert.</span><span class="sxs-lookup"><span data-stu-id="7f922-106">Each RDN consists of a set of attributes, and each attribute consists of an object identifier and a value.</span></span> <span data-ttu-id="7f922-107">Der Datentyp des Werts wird durch die **directerystring** -Struktur identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7f922-107">The data type of the value is identified by the **DirectoryString** structure.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="7f922-108">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7f922-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="7f922-109">Erstellen eines Antragsteller namens</span><span class="sxs-lookup"><span data-stu-id="7f922-109">Creating a Subject Name</span></span>](creating-a-subject-name.md)
-   [<span data-ttu-id="7f922-110">Codieren eines Antragsteller namens</span><span class="sxs-lookup"><span data-stu-id="7f922-110">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)

## <a name="related-topics"></a><span data-ttu-id="7f922-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f922-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f922-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f922-112">Requests</span></span>](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
