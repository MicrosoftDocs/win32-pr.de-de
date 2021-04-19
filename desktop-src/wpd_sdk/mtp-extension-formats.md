---
description: MTP-Erweiterungs Formate
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: MTP-Erweiterungs Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349928"
---
# <a name="mtp-extension-formats"></a>MTP-Erweiterungs Formate

Das Format einer Datei auf einem Gerät kann durch einen GUID-Wert beschrieben werden. Dieser Wert wird von der Eigenschaft WPD- \_ Objekt \_ Format angegeben.

## <a name="vendor-extended-formats"></a>Vom Hersteller erweiterte Formate

Wenn ein Gerätehersteller das vom Hersteller erweiterte Format unterstützt, kombiniert der Treiber den Format Code des Herstellers (UInt16) mit den höchsten 16 Bits des **\_ \_ \_ nicht spezifizierten GUID des WPD-Objekt Formats** .

Wenn beispielsweise der erweiterte Code des Anbieters 0xb001 ist, würde die resultierende GUID wie im folgenden Beispiel gezeigt lauten:


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

 



