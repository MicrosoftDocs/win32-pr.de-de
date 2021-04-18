---
title: Strukturen (Zeiger Eingabe Meldungen und Benachrichtigungen)
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Zeiger Eingabe Meldungen und Benachrichtigungs Strukturen.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106365442"
---
# <a name="pointer-input-messages-and-notifications-structures"></a><span data-ttu-id="5f16c-103">Zeiger Eingabe Meldungen und Benachrichtigungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="5f16c-103">Pointer Input Messages and Notifications structures</span></span>

<span data-ttu-id="5f16c-104">Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Zeiger Eingabe Meldungen und Benachrichtigungs](messages-and-notifications-portal.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="5f16c-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5f16c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5f16c-105">In this section</span></span>



| <span data-ttu-id="5f16c-106">Thema</span><span class="sxs-lookup"><span data-stu-id="5f16c-106">Topic</span></span>                                                                            | <span data-ttu-id="5f16c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f16c-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f16c-108">**INPUT_TRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="5f16c-108">**INPUT_TRANSFORM**</span></span>](/previous-versions/windows/desktop/api)<br/>                           | <span data-ttu-id="5f16c-109">Definiert die Matrix, die eine Transformation für einen nachrichtenconsumer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5f16c-109">Defines the matrix that represents a transform on a message consumer.</span></span> <span data-ttu-id="5f16c-110">Diese Matrix kann verwendet werden, um Zeiger Eingabedaten von Client Koordinaten in Bildschirm Koordinaten umzuwandeln, während das Gegenteil zum Transformieren von Zeiger Eingabedaten von Bildschirm Koordinaten in Client Koordinaten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f16c-110">This matrix can be used to transform pointer input data from client coordinates to screen coordinates, while the inverse can be used to transform pointer input data from screen coordinates to client coordinates.</span></span> <br/>                                                                 |
| [<span data-ttu-id="5f16c-111">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="5f16c-111">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                          | <span data-ttu-id="5f16c-112">Enthält grundlegende Zeiger Informationen, die für alle Zeiger Typen gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="5f16c-112">Contains basic pointer information common to all pointer types.</span></span> <span data-ttu-id="5f16c-113">Anwendungen können diese Informationen mithilfe der Funktionen [**getpointerinfo**](/previous-versions/windows/desktop/api), [**getpointerframeinfo**](/previous-versions/windows/desktop/api), [**getpointerinfohistory**](/previous-versions/windows/desktop/api) und [**getpointerframeinfohistory**](/previous-versions/windows/desktop/api) abrufen.</span><span class="sxs-lookup"><span data-stu-id="5f16c-113">Applications can retrieve this information using the [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) and [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) functions.</span></span> <br/> |
| [<span data-ttu-id="5f16c-114">**POINTER_PEN_INFO**</span><span class="sxs-lookup"><span data-stu-id="5f16c-114">**POINTER_PEN_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                 | <span data-ttu-id="5f16c-115">Definiert grundlegende Stift Informationen, die für alle Zeiger Typen gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="5f16c-115">Defines basic pen information common to all pointer types.</span></span> <br/>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="5f16c-116">**POINTER_TOUCH_INFO**</span><span class="sxs-lookup"><span data-stu-id="5f16c-116">**POINTER_TOUCH_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>             | <span data-ttu-id="5f16c-117">Definiert grundlegende Berührungs Informationen, die für alle Zeiger Typen gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="5f16c-117">Defines basic touch information common to all pointer types.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="5f16c-118">**Touchvorhertionparameters**</span><span class="sxs-lookup"><span data-stu-id="5f16c-118">**TOUCHPREDICTIONPARAMETERS**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="5f16c-119">Enthält Details zu Hardware Eingaben, die verwendet werden können, um touchziele vorherzusagen und die Hardware Latenz bei der Verarbeitung von toucheingaben und Gesten Eingaben zu kompensieren, die Entfernungs-und Geschwindigkeitsdaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="5f16c-119">Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.</span></span><br/>                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="5f16c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5f16c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f16c-121">Verweis auf Zeiger-Eingabe Nachricht</span><span class="sxs-lookup"><span data-stu-id="5f16c-121">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





