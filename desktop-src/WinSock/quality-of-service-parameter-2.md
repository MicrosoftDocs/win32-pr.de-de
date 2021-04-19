---
description: In diesem Abschnitt werden die Parameter aufgeführt, die für Quality of Service (QoS) verwendet werden.
ms.assetid: befbcf01-ecd2-4316-8e5e-889e918272cc
title: Quality of Service-Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700b44f054f8a23631ac51fe96b06eff21645101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348921"
---
# <a name="quality-of-service-parameter"></a><span data-ttu-id="9a699-103">Quality of Service-Parameter</span><span class="sxs-lookup"><span data-stu-id="9a699-103">Quality of Service Parameter</span></span>

<span data-ttu-id="9a699-104">In diesem Abschnitt werden die Parameter aufgeführt, die für Quality of Service (QoS) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a699-104">This section lists the parameters used for quality of service (QoS).</span></span>

``` syntax
#include <windows.h>
/* 
 *  values used for the QOSClassForward and QOSClassBackward
 *  field in struct ATM_QOS_CLASS_IE
 */
#define QOS_CLASS0                  0x00
#define QOS_CLASS1                  0x01
#define QOS_CLASS2                  0x02
#define QOS_CLASS3                  0x03
#define QOS_CLASS4                  0x04

typedef struct {
    UCHAR QOSClassForward;
    UCHAR QOSClassBackward;
} ATM_QOS_CLASS_IE;
```

 

 



