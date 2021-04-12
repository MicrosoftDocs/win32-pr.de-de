---
title: der einfache Typ "strautableref"
description: Definiert eine Zeichenfolge, die auf eine Meldungs Zeichenfolge verweist, die in einer Zeichen folgen Tabelle im Manifest oder in einer Nachrichtendatei (. MC) definiert ist.
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- "\"\" \"\"."
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517999"
---
# <a name="strtableref-simple-type"></a><span data-ttu-id="ab82b-104">der einfache Typ "strautableref"</span><span class="sxs-lookup"><span data-stu-id="ab82b-104">strTableRef Simple Type</span></span>

<span data-ttu-id="ab82b-105">Definiert eine Zeichenfolge, die auf eine Meldungs Zeichenfolge verweist, die in einer Zeichen folgen Tabelle im Manifest oder in einer Nachrichtendatei (. MC) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab82b-105">Defines a string that references a message string that is defined in a string table in the manifest or in a message (.mc) file.</span></span>

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="ab82b-106">Muster</span><span class="sxs-lookup"><span data-stu-id="ab82b-106">Patterns</span></span>

<span data-ttu-id="ab82b-107">Der einfache Typ " **strautableref** " ist eine " **xs: String** ", die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="ab82b-107">The **strTableRef** simple type is a **xs:string** that is restricted by the following pattern:</span></span>

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    <span data-ttu-id="ab82b-108">Die Zeichenfolge muss das Format haben, $String. *stringID* oder $MC.*symbolid*.</span><span class="sxs-lookup"><span data-stu-id="ab82b-108">The string must be of the form, $string.*stringid* or $mc.*symbolid*.</span></span> <span data-ttu-id="ab82b-109">Wenn die Zeichenfolge das Formular ist, $String. *stringID* muss im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests auf eine Zeichenfolge verweisen.</span><span class="sxs-lookup"><span data-stu-id="ab82b-109">If the string is of the form, $string.*stringid*, it must reference a string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <span data-ttu-id="ab82b-110">Wenn die Zeichenfolge das Format $MC.*symbolid* hat, muss Sie auf ein Symbol verweisen, das in der Nachrichtendatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab82b-110">If the string is of the form, $mc.*symbolid*, it must reference a symbol defined in the message file.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab82b-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab82b-111">Requirements</span></span>



| <span data-ttu-id="ab82b-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab82b-112">Requirement</span></span> | <span data-ttu-id="ab82b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ab82b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ab82b-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab82b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ab82b-115">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab82b-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ab82b-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab82b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ab82b-117">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab82b-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





