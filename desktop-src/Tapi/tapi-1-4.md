---
description: TAPI 1,4 hat der 1,3-Spezifikation eine Reihe von APIs, Nachrichten, Konstanten und Strukturelementen hinzugefügt.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959709"
---
# <a name="tapi-14"></a><span data-ttu-id="d6b26-103">TAPI 1,4</span><span class="sxs-lookup"><span data-stu-id="d6b26-103">TAPI 1.4</span></span>

<span data-ttu-id="d6b26-104">TAPI 1,4 hat der 1,3-Spezifikation eine Reihe von APIs, Nachrichten, Konstanten und Strukturelementen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d6b26-104">TAPI 1.4 added a number of APIs, messages, constants, and structure elements to the 1.3 specification.</span></span> <span data-ttu-id="d6b26-105">TAPI 1,4 unterstützt nur 16-Bit-TSPS.</span><span class="sxs-lookup"><span data-stu-id="d6b26-105">TAPI 1.4 supports only 16-bit TSPs.</span></span> <span data-ttu-id="d6b26-106">Allerdings können 32-Bit-Anwendungen entwickelt werden, ohne sich Gedanken über die Einschränkungen von 16-Bit-Fenstern machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="d6b26-106">However, it does allow 32-bit applications to be developed without having to worry about the limitations of 16-bit Windows.</span></span>

<span data-ttu-id="d6b26-107">Die TAPI-und TSPI-Header Dateien werden verwendet, um beide Anwendungen sowohl für TAPI 1,4 als auch für TAPI 2. x zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="d6b26-107">The TAPI and TSPI header files are used to develop both applications for both TAPI 1.4 and TAPI 2.x.</span></span> <span data-ttu-id="d6b26-108">Es gab zwar nicht viele Änderungen an den Strukturen zwischen diesen beiden Spezifikationen, aber es gab Änderungen an der API (insbesondere Unicode-Unterstützung), die es sehr wichtig zu beachten, dass die Header in Abhängigkeit von der aktuellen TAPI-Versions Konstante anders kompiliert werden \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d6b26-108">While there were not many changes to the structures between these two specifications, there were changes to the API (specifically, Unicode support) that make it very important to note that the headers compile differently, depending on the TAPI\_CURRENT\_VERSION constant.</span></span> <span data-ttu-id="d6b26-109">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d6b26-109">For example:</span></span>

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> <span data-ttu-id="d6b26-110">Die \_ aktuelle TAPI- \_ Version muss für alle TAPI-Anwendungen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6b26-110">TAPI\_CURRENT\_VERSION should be defined for all TAPI applications.</span></span> <span data-ttu-id="d6b26-111">Obwohl es für die TAPI 2. x-Entwicklung nicht unbedingt notwendig ist, können zukünftige Änderungen auftreten, um dies zu erfordern.</span><span class="sxs-lookup"><span data-stu-id="d6b26-111">While it is not strictly necessary for TAPI 2.x development, future changes could occur to require this.</span></span>

 

 

 



