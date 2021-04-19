---
title: boolescher Wert (WMI)
description: Ein VT \_ bool-Parameter, der den Wert von Variant \_ true (&\# 8211; 1) oder Variant \_ false (0) annimmt.
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369761"
---
# <a name="boolean-wmi"></a>boolescher Wert (WMI)

Der boolesche Datentyp ist ein VT \_ bool-Parameter, der den Wert von Variant \_ true (– 1) oder Variant \_ false (0) annimmt. In der folgenden Tabelle werden die Unterschiede zwischen den programmgesteuerten Darstellungen von Logical **true** in C/C++ und dem Automatisierungstyp aufgelistet.

| Sprache   | Wert         | Numerischer Wert |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automation | Variant \_ true | –1              |

Beide Typen sind ungleich 0 (null) und daher nicht " **false**", aber unterschiedliche Darstellungen für " **true**".
