---
description: Der htapiphone-Datentyp stellt ein undurchsichtiges Tapis-Handle für eine Telefondaten Struktur dar.
ms.assetid: e869cb3e-0eeb-4edf-a272-a655a236a3a2
title: Htapiphone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94706270b1148166181eda0d8df9b940c269f62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345177"
---
# <a name="htapiphone"></a><span data-ttu-id="d40de-103">Htapiphone</span><span class="sxs-lookup"><span data-stu-id="d40de-103">HTAPIPHONE</span></span>

<span data-ttu-id="d40de-104">Der **htapiphone** -Datentyp stellt den nicht transparenten Handle für eine Telefondaten Struktur dar.</span><span class="sxs-lookup"><span data-stu-id="d40de-104">The **HTAPIPHONE** datatype represents TAPI's opaque handle for a phone data structure.</span></span> <span data-ttu-id="d40de-105">TAPI muss einen Wert dieses Typs in einen Verweis auf die entsprechende Datenstruktur Instanz auflösen.</span><span class="sxs-lookup"><span data-stu-id="d40de-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="d40de-106">Der Dienstanbieter darf nicht versuchen, darauf zu verweisen, als ob es sich um einen Zeiger handelt, nehmen Annahmen über seine Werte vor oder interpretieren seine Darstellung in irgendeiner Weise, als er den Wert zu den entsprechenden Zeitpunkten an TAPI übergibt.</span><span class="sxs-lookup"><span data-stu-id="d40de-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



