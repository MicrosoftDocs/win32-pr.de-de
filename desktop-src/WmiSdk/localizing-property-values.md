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
# <a name="localizing-property-values"></a>Lokalisieren von Eigenschafts Werten

Das CIM-Schema Lokalisierungs Modell bietet einen Mechanismus zum Lokalisieren von Qualifizierern. Die direkte Lokalisierung von Eigenschafts Werten wird nicht unterstützt.

In einigen Fällen können jedoch die Zeichen folgen Eigenschaftswerte in den statischen Instanzen durch einen enumerierten ganzzahligen Typ ersetzt werden, und für die Eigenschaft in der Klassendefinition kann eine Werte Zuordnung definiert werden. In diesen Fällen sollte der **Wert** Qualifizierer lokalisiert werden. Das Verwenden von enumerationsqualifizierern ist der primäre Mechanismus zum Lokalisieren von Eigenschafts Werten. Alle anderen Formen der Lokalisierung von Eigenschafts Werten werden nicht unterstützt.

Im folgenden Beispiel wird gezeigt, wie statische Eigenschaften mithilfe von partiellen Wert Maps mit regulären Ausdrücken lokalisiert werden können. In diesem Beispiel wird die vordefinierte Teilmenge der Werte im Schema mithilfe statischer Instanzen initialisiert. Die restlichen Werte werden dynamisch bereitgestellt.

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

Weitere Informationen finden Sie unter [lokalisieren statischer Eigenschaften](localizing-static-properties.md).

 

 



