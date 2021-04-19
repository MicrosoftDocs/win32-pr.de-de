---
description: Speichern und Wiederherstellen von dvdstate-Objekten
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Speichern und Wiederherstellen von dvdstate-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346595"
---
# <a name="saving-and-restoring-dvdstate-objects"></a><span data-ttu-id="e0ab3-103">Speichern und Wiederherstellen von dvdstate-Objekten</span><span class="sxs-lookup"><span data-stu-id="e0ab3-103">Saving and Restoring DvdState Objects</span></span>

<span data-ttu-id="e0ab3-104">[**Idvdstate**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) -Objekte ermöglichen es Anwendungen, eine Momentaufnahme der Benutzersitzung zu speichern, einschließlich Informationen wie dem aktuellen Speicherort auf der Festplatte, der Jugendebene der Person, die die Anzeige durchsucht, der ausgewählten Audiodaten und der teilbildstreams usw.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-104">[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) objects enable applications to save a snapshot of the user session, including information such as the current location on the disc, the parental level of the person who is viewing, the selected audio and subpicture streams, and so on.</span></span> <span data-ttu-id="e0ab3-105">Dies bedeutet, dass Benutzer ihren Speicherort auf einem DVD-Video-CD speichern und ihn zu einem späteren Zeitpunkt ansehen können.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-105">This means that users can save their place on a DVD-Video disc and watch it at a later time.</span></span>

<span data-ttu-id="e0ab3-106">Anwendungen können keine dvdstate-Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-106">Applications cannot create DvdState objects.</span></span> <span data-ttu-id="e0ab3-107">Diese Objekte werden intern vom DVD-Navigator erstellt, wenn eine Anwendung [**IDvdInfo2:: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate)aufruft.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-107">These objects are created internally by the DVD Navigator when an application calls [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span></span> <span data-ttu-id="e0ab3-108">Dvdstate-Objekte machen die [**idvdstate**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) -Schnittstelle verfügbar, damit Anwendungen bestimmte Informationen Abfragen können.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-108">DvdState objects expose the [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) interface to allow applications to query for certain information.</span></span>

<span data-ttu-id="e0ab3-109">In der DVD-Beispielanwendung zeigen die **cdvdcore:: restorebookmark** -und **cdvdcore:: savebookmark** -Funktionen, wie dvdstate-Objekte gespeichert und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-109">In the DVD sample application, the **CDvdCore::RestoreBookmark** and **CDvdCore::SaveBookmark** functions show how to save and retrieve DvdState objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0ab3-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0ab3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ab3-111">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e0ab3-111">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



