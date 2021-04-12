---
description: Die TAPI/Phone-Geräteklasse besteht aus allen Telefongeräten. Sie greifen auf diese Geräte mithilfe der TAPI-Telefonfunktionen zu.
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: TAPI/Telefon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960230"
---
# <a name="tapiphone"></a><span data-ttu-id="3f204-104">TAPI/Telefon</span><span class="sxs-lookup"><span data-stu-id="3f204-104">tapi/phone</span></span>

<span data-ttu-id="3f204-105">Die TAPI/Phone-Geräteklasse besteht aus allen Telefongeräten.</span><span class="sxs-lookup"><span data-stu-id="3f204-105">The tapi/phone device class consists of all phone devices.</span></span> <span data-ttu-id="3f204-106">Sie greifen auf diese Geräte mithilfe der TAPI-Telefonfunktionen zu.</span><span class="sxs-lookup"><span data-stu-id="3f204-106">You access these devices by using the TAPI phone functions.</span></span>

<span data-ttu-id="3f204-107">Die [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt den **dwstringformat** -Member auf den "StringFormat" \_ -Binärwert fest und fügt diesen zusätzlichen Member an:</span><span class="sxs-lookup"><span data-stu-id="3f204-107">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

<span data-ttu-id="3f204-108">Der **dwenviceid** -Member ist der Bezeichner des Telefon Geräts, das dem durch [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)angegebenen Telefon Handle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3f204-108">The **dwDeviceId** member is the identifier of the phone device associated with the phone handle given by [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span>

<span data-ttu-id="3f204-109">Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt auch eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur, wobei **dwstringformat** auf die Binärdatei StringFormat festgelegt \_ und dieses zusätzliche Mitglied angehängt wird:</span><span class="sxs-lookup"><span data-stu-id="3f204-109">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

<span data-ttu-id="3f204-110">Der **adwenviceids** -Member ist ein Array mit den Geräte bezeichdern aller Telefongeräte, die mit dem angegebenen liniengerät verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="3f204-110">The **adwDeviceIds** member is an array containing the device identifiers of all phone devices that are associated with the given line device.</span></span> <span data-ttu-id="3f204-111">Wenn keine zugeordneten Telefongeräte vorhanden sind, gibt [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) den lineerr- \_ Wert "invalendviceclass" zurück.</span><span class="sxs-lookup"><span data-stu-id="3f204-111">If there are no associated phone devices, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) returns the LINEERR\_INVALDEVICECLASS value.</span></span>

 

 



