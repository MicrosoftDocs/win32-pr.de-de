---
description: Alle sicherungsfähige Objekte ordnen ihre Zugriffsrechte mithilfe des in der folgenden Abbildung gezeigten Zugriffsmaskenformats an.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Format der Zugriffsmaske
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86187f5ef69eb115bc880d2bc4df07e8b1a1f791976da2a8d24b6a0f9d7293c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914530"
---
# <a name="access-mask-format"></a>Format der Zugriffsmaske

Alle sicherungsfähige Objekte ordnen ihre [](/windows/desktop/SecGloss/a-gly) Zugriffsrechte mithilfe des in der folgenden Abbildung gezeigten Zugriffsmaskenformats an.

![Zugriffsmaskenformat](images/accctrl4.png)

In diesem Format gelten die niedrigen 16 Bits für objektspezifische Zugriffsrechte, die nächsten 8 Bits für Standardzugriffsrechte, die für die meisten [](generic-access-rights.md) Objekttypen gelten, und die vier hoch geordneten Bits werden verwendet, um generische Zugriffsrechte anzugeben, die jeder Objekttyp einem Satz von Standard- und objektspezifischen Rechten zuordnen kann. [](standard-access-rights.md) Das ACCESS \_ SYSTEM \_ SECURITY-Bit entspricht dem [Recht, auf die SACL des Objekts zu zugreifen.](sacl-access-right.md)

 

 
