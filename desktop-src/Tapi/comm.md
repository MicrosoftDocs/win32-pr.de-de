---
description: Die comm-Geräteklasse besteht aus Kommunikationsports. Sie greifen auf diese Geräte mithilfe der Datei-und Kommunikationsfunktionen zu.
ms.assetid: c1cf4998-b752-4cfd-9dd7-c9872b62c44b
title: Komm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40136654d7e308f30e4e27467cf5e21385340841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753000"
---
# <a name="comm"></a><span data-ttu-id="e5849-104">Komm</span><span class="sxs-lookup"><span data-stu-id="e5849-104">comm</span></span>

<span data-ttu-id="e5849-105">Die comm-Geräteklasse besteht aus Kommunikationsports.</span><span class="sxs-lookup"><span data-stu-id="e5849-105">The comm device class consists of communications ports.</span></span> <span data-ttu-id="e5849-106">Sie greifen auf diese Geräte mithilfe der [Datei](/windows/desktop/FileIO/file-management-functions) -und [Kommunikationsfunktionen](/windows/desktop/DevIO/communications-functions)zu.</span><span class="sxs-lookup"><span data-stu-id="e5849-106">You access these devices by using the [file](/windows/desktop/FileIO/file-management-functions) and [communications functions](/windows/desktop/DevIO/communications-functions).</span></span>

<span data-ttu-id="e5849-107">Die [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) -Funktion füllt eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, legt den **dwstringformat** -Member auf den \_ ASCII-Wert StringFormat fest und fügt eine NULL-terminierte Zeichenfolge an, die den Namen des kommunikationsgeräts angibt (z. b. den Modem Namen).</span><span class="sxs-lookup"><span data-stu-id="e5849-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_ASCII value and appending a null-terminated string that specifies the name of the communication device (such as the modem name).</span></span>

 

 
