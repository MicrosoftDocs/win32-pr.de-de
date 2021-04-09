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
# <a name="access-mask-format"></a><span data-ttu-id="2488b-103">Zugriffs Masken Format</span><span class="sxs-lookup"><span data-stu-id="2488b-103">Access Mask Format</span></span>

<span data-ttu-id="2488b-104">Alle Sicherungs fähigen Objekte ordnen ihre Zugriffsrechte mithilfe des [*Zugriffs Masken*](/windows/desktop/SecGloss/a-gly) Formats an, das in der folgenden Abbildung gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2488b-104">All securable objects arrange their access rights by using the [*access mask*](/windows/desktop/SecGloss/a-gly) format shown in the following illustration.</span></span>

![Zugriffs Masken Format](images/accctrl4.png)

<span data-ttu-id="2488b-106">In diesem Format gelten die nieder wertigen 16 Bits für objektspezifische Zugriffsrechte, die nächsten 8 Bits gelten für [standardmäßige Zugriffsrechte](standard-access-rights.md), die für die meisten Objekttypen gelten, und die vier allgemeinen Bits werden verwendet, um [generische Zugriffsrechte](generic-access-rights.md) anzugeben, die jeder Objekttyp einem Satz von Standard-und Objekt spezifischen rechten zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="2488b-106">In this format, the low-order 16 bits are for object-specific access rights, the next 8 bits are for [standard access rights](standard-access-rights.md), which apply to most types of objects, and the 4 high-order bits are used to specify [generic access rights](generic-access-rights.md) that each object type can map to a set of standard and object-specific rights.</span></span> <span data-ttu-id="2488b-107">Das \_ Sicherheits Bit des Zugriffs Systems \_ entspricht dem [Recht für den Zugriff auf die SACL des Objekts](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="2488b-107">The ACCESS\_SYSTEM\_SECURITY bit corresponds to the [right to access the object's SACL](sacl-access-right.md).</span></span>

 

 
