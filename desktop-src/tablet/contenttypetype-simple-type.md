---
description: Definiert den Typ, der gültige Werte für das Type-Attribut des Inhalts Element- \[ Journal Readers definiert \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Einfacher contenttypetype-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042414"
---
# <a name="contenttypetype-simple-type"></a><span data-ttu-id="63e88-103">Einfacher contenttypetype-Typ</span><span class="sxs-lookup"><span data-stu-id="63e88-103">ContentTypeType Simple Type</span></span>

<span data-ttu-id="63e88-104">Definiert den Typ, der gültige Werte für das *Type* -Attribut des [Inhalts Element- \[ Journal \] Readers](content-element--journal-reader.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="63e88-104">Defines the type that defines valid values for the *Type* attribute of the [Content element \[Journal Reader\]](content-element--journal-reader.md).</span></span>

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="63e88-105">Muster</span><span class="sxs-lookup"><span data-stu-id="63e88-105">Patterns</span></span>

<span data-ttu-id="63e88-106">Der einfache **contenttypetype** -Typ ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="63e88-106">The **ContentTypeType** simple type is a string that is restricted by the following pattern:</span></span>

-   `Normal|Inert`

## <a name="remarks"></a><span data-ttu-id="63e88-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63e88-107">Remarks</span></span>

<span data-ttu-id="63e88-108">Gültige Werte sind "Normal" und "inert".</span><span class="sxs-lookup"><span data-stu-id="63e88-108">Valid values are "Normal" and "Inert".</span></span>

<span data-ttu-id="63e88-109">Wenn der Typ "inert" ist, ist der enthaltene Inhalt eine Journal Seite, bei der es sich um den schreibgeschützten/nicht bearbeitbaren "Hintergrund" für das Dokument handelt.</span><span class="sxs-lookup"><span data-stu-id="63e88-109">If the type is "Inert", then the content contained is a Journal page that is the read-only/non-editable "background" for the document.</span></span> <span data-ttu-id="63e88-110">Dieser Fehler tritt auf, wenn ein Dokument mithilfe des Druckertreibers für den Journal Hinweis Writer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="63e88-110">This occurs when a document is created by using the Journal Note Writer printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e88-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63e88-111">Requirements</span></span>



| <span data-ttu-id="63e88-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63e88-112">Requirement</span></span> | <span data-ttu-id="63e88-113">Wert</span><span class="sxs-lookup"><span data-stu-id="63e88-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="63e88-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63e88-114">Minimum supported client</span></span><br/> | <span data-ttu-id="63e88-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63e88-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="63e88-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63e88-116">Minimum supported server</span></span><br/> | <span data-ttu-id="63e88-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="63e88-117">None supported</span></span><br/>                                     |



 

 




