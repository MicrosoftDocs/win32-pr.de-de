---
description: Die TAPI/Line-Geräteklasse besteht aus allen Linien Geräten. Sie greifen auf diese Geräte mithilfe der TAPI-Linienfunktionen zu.
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: TAPI/Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373218"
---
# <a name="tapiline"></a><span data-ttu-id="2e3b2-104">TAPI/Linie</span><span class="sxs-lookup"><span data-stu-id="2e3b2-104">tapi/line</span></span>

<span data-ttu-id="2e3b2-105">Die TAPI/Line-Geräteklasse besteht aus allen Linien Geräten.</span><span class="sxs-lookup"><span data-stu-id="2e3b2-105">The tapi/line device class consists of all line devices.</span></span> <span data-ttu-id="2e3b2-106">Sie greifen auf diese Geräte mithilfe der TAPI-Linienfunktionen zu.</span><span class="sxs-lookup"><span data-stu-id="2e3b2-106">You access these devices using the TAPI line functions.</span></span>

<span data-ttu-id="2e3b2-107">Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt den **dwstringformat** -Member auf den "StringFormat" \_ -Binärwert fest und fügt diesen zusätzlichen Member an.</span><span class="sxs-lookup"><span data-stu-id="2e3b2-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member.</span></span>

``` syntax
DWORD dwDeviceI;  // line device identifier
```

<span data-ttu-id="2e3b2-108">Der **dwenviceid** -Member ist der Bezeichner des Linien Geräts, das dem von [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)angegebenen Zeilen Handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2e3b2-108">The **dwDeviceId** member is the identifier of the line device associated with the line handle given by [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="2e3b2-109">Die [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) -Funktion füllt auch eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur, wobei **dwstringformat** auf die Binärdatei StringFormat festgelegt \_ und dieses zusätzliche Mitglied angehängt wird:</span><span class="sxs-lookup"><span data-stu-id="2e3b2-109">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

<span data-ttu-id="2e3b2-110">Der **adwenviceids** -Member ist ein Array, das die Geräte Bezeichner aller Linien Geräte enthält, die dem Telefongerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2e3b2-110">The **adwDeviceIds** member is an array containing the device identifiers of all line devices that are associated with the phone device.</span></span> <span data-ttu-id="2e3b2-111">Wenn keine zugeordneten Zeilen Geräte vorhanden sind, gibt [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) den Wert phoneerr \_ invalendviceclass zurück.</span><span class="sxs-lookup"><span data-stu-id="2e3b2-111">If there are no associated line devices, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) returns the PHONEERR\_INVALDEVICECLASS value.</span></span>

 

 



