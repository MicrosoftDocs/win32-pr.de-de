---
description: Datenobjekte enthalten die eigentlichen Daten oder einen Verweis auf diese Daten. Jedes Datenobjekt verfügt über eine entsprechende Vorlage, die den Datentyp angibt. In den folgenden Abschnitten werden das Formular und Teile von Datenobjekten erläutert.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Daten (X-Dateiformat, Text Codierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392698"
---
# <a name="data-x-file-format-text-encoding"></a><span data-ttu-id="128db-105">Daten (X-Dateiformat, Text Codierung)</span><span class="sxs-lookup"><span data-stu-id="128db-105">Data (X file format, text encoding)</span></span>

<span data-ttu-id="128db-106">Datenobjekte enthalten die eigentlichen Daten oder einen Verweis auf diese Daten.</span><span class="sxs-lookup"><span data-stu-id="128db-106">Data objects contain the actual data or a reference to that data.</span></span> <span data-ttu-id="128db-107">Jedes Datenobjekt verfügt über eine entsprechende Vorlage, die den Datentyp angibt.</span><span class="sxs-lookup"><span data-stu-id="128db-107">Each data object has a corresponding template that specifies the data type.</span></span> <span data-ttu-id="128db-108">In den folgenden Abschnitten werden das Formular und Teile von Datenobjekten erläutert.</span><span class="sxs-lookup"><span data-stu-id="128db-108">The following sections discuss the form and parts of data objects.</span></span>

## <a name="form-identifier-and-name"></a><span data-ttu-id="128db-109">Formular, Bezeichner und Name</span><span class="sxs-lookup"><span data-stu-id="128db-109">Form, Identifier, and Name</span></span>

<span data-ttu-id="128db-110">Datenobjekte weisen die folgende Form auf:</span><span class="sxs-lookup"><span data-stu-id="128db-110">Data objects have the following form.</span></span>


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



<span data-ttu-id="128db-111">Der Bezeichner ist obligatorisch und muss mit einem zuvor definierten Datentyp oder primitiven identisch sein.</span><span class="sxs-lookup"><span data-stu-id="128db-111">The identifier is compulsory and must match a previously defined data type or primitive.</span></span> <span data-ttu-id="128db-112">Der Name ist jedoch optional.</span><span class="sxs-lookup"><span data-stu-id="128db-112">However, the name is optional.</span></span>

## <a name="data-members"></a><span data-ttu-id="128db-113">Datenelemente</span><span class="sxs-lookup"><span data-stu-id="128db-113">Data Members</span></span>

<span data-ttu-id="128db-114">Datenmember können eines der folgenden sein: Datenobjekt, Daten Verweis, ganzzahlige Liste, float-Liste oder Zeichen folgen Liste.</span><span class="sxs-lookup"><span data-stu-id="128db-114">Data members can be one of the following: data object, data reference, integer list, float list, or string list.</span></span>

<span data-ttu-id="128db-115">Bei einem Datenobjekt handelt es sich um ein Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="128db-115">A data object is a nested data object.</span></span> <span data-ttu-id="128db-116">Dadurch kann die hierarchische Natur des Datei Formats ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="128db-116">This enables the hierarchical nature of the file format to be expressed.</span></span> <span data-ttu-id="128db-117">Die in der Hierarchie zulässigen Typen von in der-Hierarchie zulässigen Datenobjekten sind möglicherweise eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="128db-117">The types of nested data objects allowed in the hierarchy may be restricted.</span></span>

<span data-ttu-id="128db-118">Ein Daten Verweis ist ein Verweis auf ein zuvor angetretene Datenobjekt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="128db-118">A data reference is a reference to a previously encountered data object as shown in the following example.</span></span>


```
{
  name |
  UUID |
  name UUID
}
```



<span data-ttu-id="128db-119">Eine ganzzahlige Liste ist eine durch Semikolons getrennte Liste mit ganzen Zahlen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="128db-119">An integer list is a semicolon-separated list of integers, as shown in the following example.</span></span>


```
1; 2; 3;
```



<span data-ttu-id="128db-120">Eine float-Liste ist eine durch Semikolons getrennte Liste von Gleit Komma Zahlen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="128db-120">A float list is a semicolon-separated list of floats, as shown in the following example.</span></span>


```
1.0; 2.0; 3.0;
```



<span data-ttu-id="128db-121">Eine Zeichen folgen Liste ist eine durch Semikolons getrennte Liste von Zeichen folgen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="128db-121">A string list is a semicolon-separated list of strings, as shown in the following example.</span></span>


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a><span data-ttu-id="128db-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="128db-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="128db-123">Text Codierung</span><span class="sxs-lookup"><span data-stu-id="128db-123">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



