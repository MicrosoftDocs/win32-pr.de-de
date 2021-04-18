---
description: In diesem Abschnitt wird die Typdefinition für die Nummer der aufrufenden Partei aufgelistet.
ms.assetid: eb930123-28cf-4857-b7ad-f3c1786da7cc
title: Nummer der aufrufenden Partei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8fe232386448ba2fcffc38b285d7190c8192e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345107"
---
# <a name="calling-party-number"></a><span data-ttu-id="90a8c-103">Nummer der aufrufenden Partei</span><span class="sxs-lookup"><span data-stu-id="90a8c-103">Calling Party Number</span></span>

<span data-ttu-id="90a8c-104">In diesem Abschnitt wird die Typdefinition für die Nummer der aufrufenden Partei aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="90a8c-104">This section lists the type definition for the calling party number.</span></span>

``` syntax
#include <windows.h>

/* 
 *  values used for the Presentation_Indication field in 
 *  struct ATM_CALLING_PARTY_NUMBER_IE
 */
#define PI_ALLOWED                  0x00
#define PI_RESTRICTED               0x40
#define PI_NUMBER_NOT_AVAILABLE     0x80

/* 
 *  values used for the Screening_Indicator field in 
 *  struct ATM_CALLING_PARTY_NUMBER_IE
 */
#define SI_USER_NOT_SCREENED        0x00
#define SI_USER_PASSED              0x01
#define SI_USER_FAILED              0x02
#define SI_NETWORK                  0x03

typedef struct {
    ATM_ADDRESS ATM_Number;
    UCHAR       Presentation_Indication;
    UCHAR       Screening_Indicator;
} ATM_CALLING_PARTY_NUMBER_IE;
```

 

 



