---
description: MTP-Erweiterungsformate
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: MTP-Erweiterungsformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a490c29c98b454b7d563e8af46131b040f123b9de2ef689ea5ede1a2ac100ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193956"
---
# <a name="mtp-extension-formats"></a>MTP-Erweiterungsformate

Das Format einer Datei auf einem Gerät kann mit einem GUID-Wert beschrieben werden. Dieser Wert wird von der WPD \_ OBJECT \_ FORMAT-Eigenschaft angegeben.

## <a name="vendor-extended-formats"></a>Erweiterte Formate des Anbieters

Wenn ein Gerätehersteller ein vom Hersteller erweitertes Format unterstützt, kombiniert der Treiber den Formatcode des Herstellers (UINT16) mit den höchsten 16 Bits der **WPD \_ OBJECT FORMAT \_ \_ UNSPECIFIED** GUID.

Wenn der vom Hersteller erweiterte Code beispielsweise 0xB001 ist, würde die resultierende GUID wie im folgenden Beispiel gezeigt sein:


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

 



