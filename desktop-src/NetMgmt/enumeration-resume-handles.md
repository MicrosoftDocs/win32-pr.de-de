---
title: Enumerationshandles wieder aufnehmen
description: Enumerationshandles sind Bezeichner für den tatsächlichen Fortsetzungs Schlüssel, der in den Instanzdaten für die Funktion enthalten ist. Dies ist für Sicherheit, Interoperabilität und zur Vereinfachung des aufrufercodes für die Funktion erforderlich.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947745"
---
# <a name="enumeration-resume-handles"></a><span data-ttu-id="1713c-104">Enumerationshandles wieder aufnehmen</span><span class="sxs-lookup"><span data-stu-id="1713c-104">Enumeration Resume Handles</span></span>

<span data-ttu-id="1713c-105">Enumerationshandles sind Bezeichner für den tatsächlichen Fortsetzungs Schlüssel, der in den Instanzdaten für die Funktion enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1713c-105">Enumeration resume handles are identifiers for the actual resume key contained in the instance data for the function.</span></span> <span data-ttu-id="1713c-106">Dies ist für Sicherheit, Interoperabilität und zur Vereinfachung des aufrufercodes für die Funktion erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1713c-106">This is required for security, interoperability, and to simplify the caller code for the function.</span></span>

<span data-ttu-id="1713c-107">Wenn ein **null** -Wert für den Zeiger auf das Fortsetzungs handle übermittelt wird, wird kein Handle gespeichert, und die enumerationssuche kann nicht fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1713c-107">If a **NULL** is passed for the pointer to the resume handle, no handle is stored and the enumeration search cannot be continued.</span></span> <span data-ttu-id="1713c-108">Dies ist hilfreich in Fällen, in denen die Anwendung nicht alle Elemente auflisten möchte.</span><span class="sxs-lookup"><span data-stu-id="1713c-108">This is useful in cases where the application does not want to enumerate all the items.</span></span>

<span data-ttu-id="1713c-109">Wenn ein-enumerationsaufruf einen Fehler zurückgibt, muss der Fortsetzungs Handle als ungültig behandelt und nicht für nachfolgende enumerationsaufrufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1713c-109">If an error is returned from an enumeration call, the resume handle must be treated as invalid and not used for any subsequent enumeration calls.</span></span> <span data-ttu-id="1713c-110">Wenn dies auftritt, müssen Sie die Enumeration von Anfang an neu starten.</span><span class="sxs-lookup"><span data-stu-id="1713c-110">When this occurs you must restart the enumeration from the beginning.</span></span>

 

 




