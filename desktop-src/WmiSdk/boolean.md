---
title: Boolean (WMI)
description: Ein VT-BOOL-Parameter, der den Wert von \_ VARIANT \_ TRUE (&\# 8211;1) oder VARIANT \_ FALSE (0) angibt.
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50422990a45dd59c2bedc3ac90bddcf06f7796cd3308daf03a11db0dca38f0b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051058"
---
# <a name="boolean-wmi"></a>Boolean (WMI)

Der boolesche Datentyp ist ein VT-BOOL-Parameter, der den Wert von \_ VARIANT \_ TRUE (–1) oder VARIANT \_ FALSE (0) übernimmt. In der folgenden Tabelle wird der Unterschied zwischen den programmgesteuerten Darstellungen des logischen **TRUE** in C/C++ und dem Automatisierungstyp aufgeführt.

| Sprache   | Wert         | Numerischer Wert |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automation | VARIANT \_ TRUE | –1              |

Beide Typen sind ungleich 0 (null) und daher **nicht FALSE,** verfügen jedoch über unterschiedliche Darstellungen für **TRUE.**
