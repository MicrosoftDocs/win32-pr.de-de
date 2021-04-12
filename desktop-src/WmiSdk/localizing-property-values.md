---
description: Das CIM-Schema Lokalisierungs Modell bietet einen Mechanismus zum Lokalisieren von Qualifizierern. Die direkte Lokalisierung von Eigenschafts Werten wird nicht unterstützt.
ms.assetid: a88bd873-7132-45b6-831e-64f9bb254c6e
ms.tgt_platform: multiple
title: Lokalisieren von Eigenschafts Werten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ccec714557934ca32a878e21fb2a75d24a211a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344898"
---
# <a name="localizing-property-values"></a><span data-ttu-id="5f1e8-104">Lokalisieren von Eigenschafts Werten</span><span class="sxs-lookup"><span data-stu-id="5f1e8-104">Localizing Property Values</span></span>

<span data-ttu-id="5f1e8-105">Das CIM-Schema Lokalisierungs Modell bietet einen Mechanismus zum Lokalisieren von Qualifizierern.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-105">The CIM schema localization model provides a mechanism for localizing qualifiers.</span></span> <span data-ttu-id="5f1e8-106">Die direkte Lokalisierung von Eigenschafts Werten wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-106">It does not support direct localization of property values.</span></span>

<span data-ttu-id="5f1e8-107">In einigen Fällen können jedoch die Zeichen folgen Eigenschaftswerte in den statischen Instanzen durch einen enumerierten ganzzahligen Typ ersetzt werden, und für die Eigenschaft in der Klassendefinition kann eine Werte Zuordnung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-107">In some cases, however, the string properties values in the static instances can be replaced by an enumerated integer type and a value map can be defined for the property in the class definition.</span></span> <span data-ttu-id="5f1e8-108">In diesen Fällen sollte der **Wert** Qualifizierer lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-108">In these cases, the **Values** qualifier should be localized.</span></span> <span data-ttu-id="5f1e8-109">Das Verwenden von enumerationsqualifizierern ist der primäre Mechanismus zum Lokalisieren von Eigenschafts Werten.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-109">Using enumeration qualifiers is the primary mechanism for localizing property values.</span></span> <span data-ttu-id="5f1e8-110">Alle anderen Formen der Lokalisierung von Eigenschafts Werten werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-110">Any other forms of property value localization are not supported.</span></span>

<span data-ttu-id="5f1e8-111">Im folgenden Beispiel wird gezeigt, wie statische Eigenschaften mithilfe von partiellen Wert Maps mit regulären Ausdrücken lokalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-111">The following example shows how static properties can be localized using partial value maps with regular expressions.</span></span> <span data-ttu-id="5f1e8-112">In diesem Beispiel wird die vordefinierte Teilmenge der Werte im Schema mithilfe statischer Instanzen initialisiert.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-112">In this example, the predefined subset of values is initialized in the schema using static instances.</span></span> <span data-ttu-id="5f1e8-113">Die restlichen Werte werden dynamisch bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5f1e8-113">The rest of the values are provided dynamically.</span></span>

``` syntax
[abstract]
class DataGroup
{
   [key] string GUID;
   [Description("data group display name"): Amended,
                     ValueMap{"Logical Disk",
                     "CPU Utilization", ".+"}]
                     string GroupDisplayName;
   [ValueMap{"Monitors percentage of disk free space",
                  "Monitors percentage CPU utilization", ".+"}] 
                   string GroupDescription;
};

[static, Description ("pre-configured parameters") :amended]
class InitialGroup : DataGroup {
};

[dynamic, provider("HMProvider"),
    Description ("user-defined parameters") :amended]
class UserDefionedGroup : DataGroup {
};

instance of InitialGroup {
   GUID = "abc";
   GroupDisplayName = "Logical Disk";
   GroupDescription = "Monitors percentage of disk free space";
};

instance of InitialGroup {
   GUID = "def";
   GroupDisplayName = "CPU Utilization";
   GroupDescription = "Monitors percentage CPU utilization";
};
```

<span data-ttu-id="5f1e8-114">Weitere Informationen finden Sie unter [lokalisieren statischer Eigenschaften](localizing-static-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5f1e8-114">For more information, see [Localizing Static Properties](localizing-static-properties.md).</span></span>

 

 



