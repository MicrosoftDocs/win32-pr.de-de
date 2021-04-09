---
description: Alle Sicherungs fähigen Objekte ordnen ihre Zugriffsrechte mithilfe des Zugriffs Masken Formats an, das in der folgenden Abbildung gezeigt wird.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Zugriffs Masken Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866004"
---
# <a name="access-mask-format"></a>Zugriffs Masken Format

Alle Sicherungs fähigen Objekte ordnen ihre Zugriffsrechte mithilfe des [*Zugriffs Masken*](/windows/desktop/SecGloss/a-gly) Formats an, das in der folgenden Abbildung gezeigt wird.

![Zugriffs Masken Format](images/accctrl4.png)

In diesem Format gelten die nieder wertigen 16 Bits für objektspezifische Zugriffsrechte, die nächsten 8 Bits gelten für [standardmäßige Zugriffsrechte](standard-access-rights.md), die für die meisten Objekttypen gelten, und die vier allgemeinen Bits werden verwendet, um [generische Zugriffsrechte](generic-access-rights.md) anzugeben, die jeder Objekttyp einem Satz von Standard-und Objekt spezifischen rechten zuordnen kann. Das \_ Sicherheits Bit des Zugriffs Systems \_ entspricht dem [Recht für den Zugriff auf die SACL des Objekts](sacl-access-right.md).

 

 
