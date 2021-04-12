---
description: Der Datentyp "htapicall" stellt das nicht transparente TAPI-Handle für eine Aufrufe Datenstruktur dar.
ms.assetid: a2a17b03-5779-411e-8959-6e2de5e53c5a
title: Htapicall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abd90dc8453be5f5bec18e92b384b7ace830d14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344279"
---
# <a name="htapicall"></a><span data-ttu-id="b1a28-103">Htapicall</span><span class="sxs-lookup"><span data-stu-id="b1a28-103">HTAPICALL</span></span>

<span data-ttu-id="b1a28-104">Der Datentyp " **htapicall** " stellt das nicht transparente TAPI-Handle für eine Aufrufe Datenstruktur dar.</span><span class="sxs-lookup"><span data-stu-id="b1a28-104">The **HTAPICALL** datatype represents the TAPI opaque handle for a call data structure.</span></span> <span data-ttu-id="b1a28-105">TAPI muss einen Wert dieses Typs in einen Verweis auf die entsprechende Datenstruktur Instanz auflösen.</span><span class="sxs-lookup"><span data-stu-id="b1a28-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="b1a28-106">Der Dienstanbieter darf nicht versuchen, darauf zu verweisen, als ob es sich um einen Zeiger handelt, nehmen Annahmen über seine Werte vor oder interpretieren seine Darstellung in irgendeiner Weise, als er den Wert zu den entsprechenden Zeitpunkten an TAPI übergibt.</span><span class="sxs-lookup"><span data-stu-id="b1a28-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



