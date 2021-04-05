---
description: Diese TSPI \_ linesetcurrentlocation-Funktion ist veraltet. TAPI hat diese Funktion aufgerufen, wenn der Benutzer (im Dialogfeld Wähl Eigenschaften) oder eine Anwendung (mithilfe der linesetcurrentlocation-Funktion) den Speicherort der Adressübersetzung geändert hat.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757003"
---
# <a name="tspi_linesetcurrentlocation"></a><span data-ttu-id="e815c-104">TSPI \_ linesetcurrentlocation</span><span class="sxs-lookup"><span data-stu-id="e815c-104">TSPI\_lineSetCurrentLocation</span></span>

<span data-ttu-id="e815c-105">Diese TSPI \_ linesetcurrentlocation-Funktion ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="e815c-105">This TSPI\_lineSetCurrentLocation function is obsolete.</span></span> <span data-ttu-id="e815c-106">TAPI hat diese Funktion aufgerufen, wenn der Benutzer (im Dialogfeld **Wähl Eigenschaften** ) oder eine Anwendung (mithilfe der [**linesetcurrentlocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) -Funktion) den Speicherort der Adressübersetzung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="e815c-106">TAPI called this function when the user (using the **Dialing Properties** dialog box) or an application (using the [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) function) changed the address translation location.</span></span>

<span data-ttu-id="e815c-107">Aktuell führt eine Änderung des Übersetzungsspeicher Orts zu einer Zeile \_ DevState-Nachricht, bei der *dwParam1* auf linedevstate \_ translatechange festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e815c-107">Currently, a change in translation location results in a LINE\_DEVSTATE message with *dwParam1* set to LINEDEVSTATE\_TRANSLATECHANGE.</span></span>

 

 
