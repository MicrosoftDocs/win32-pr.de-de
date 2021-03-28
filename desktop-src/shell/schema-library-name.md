---
description: Das- <name> Element gibt den Namen dieser Bibliothek an. Dieses Element ist erforderlich und besitzt keine Attribute oder untergeordneten Elemente.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Name-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995175"
---
# <a name="name-element-library-schema"></a><span data-ttu-id="a5990-104">Name-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="a5990-104">name Element (Library Schema)</span></span>

<span data-ttu-id="a5990-105">Das- <name> Element gibt den Namen dieser Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="a5990-105">The <name> element specifies the name of this library.</span></span> <span data-ttu-id="a5990-106">Dieses Element ist erforderlich und besitzt keine Attribute oder untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="a5990-106">This element is required and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5990-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5990-107">Syntax</span></span>

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a><span data-ttu-id="a5990-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="a5990-108">Element Information</span></span>



| <span data-ttu-id="a5990-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a5990-109">Parent Element</span></span>                                                               | <span data-ttu-id="a5990-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5990-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a5990-111">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="a5990-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="a5990-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5990-112">Remarks</span></span>

<span data-ttu-id="a5990-113">Der Name ist der Anzeige Name der Bibliothek, der in Windows-Explorer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a5990-113">The name is the friendly library name that is displayed in Windows Explorer.</span></span> <span data-ttu-id="a5990-114">Der Name kann <dllname> <index> wie im folgenden Beispiel in einem Format wie im folgenden Beispiel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a5990-114">The name can be specified in a <dllname>,<index> format, as in the following example.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="a5990-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5990-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5990-116">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="a5990-116">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="a5990-117">Suchdienst-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="a5990-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
