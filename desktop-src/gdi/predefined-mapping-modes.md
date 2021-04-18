---
description: Die sechs vordefinierten Zustellungs Modi sind Geräte abhängig (mm \_ -Text) und die verbleibenden fünf (mm- \_ hienglish, mm \_ -loenglish, mm \_ HIMETRIC, mm \_ lometrisch und mm \_ Twips) Geräte unabhängig voneinander.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Vordefinierte Karten Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978384"
---
# <a name="predefined-mapping-modes"></a><span data-ttu-id="932e5-103">Vordefinierte Karten Modi</span><span class="sxs-lookup"><span data-stu-id="932e5-103">Predefined Mapping Modes</span></span>

<span data-ttu-id="932e5-104">Die sechs vordefinierten Zustellungs Modi sind Geräte abhängig (mm \_ -Text) und die verbleibenden fünf (mm- \_ hienglish, mm \_ -loenglish, mm \_ HIMETRIC, mm \_ lometrisch und mm \_ Twips) Geräte unabhängig voneinander.</span><span class="sxs-lookup"><span data-stu-id="932e5-104">Of the six predefined mapping modes, one is device dependent (MM\_TEXT) and the remaining five (MM\_HIENGLISH, MM\_LOENGLISH, MM\_HIMETRIC, MM\_LOMETRIC, and MM\_TWIPS) are device independent.</span></span>

<span data-ttu-id="932e5-105">Der standardmäßige Kartenmodus ist mm- \_ Text.</span><span class="sxs-lookup"><span data-stu-id="932e5-105">The default mapping mode is MM\_TEXT.</span></span> <span data-ttu-id="932e5-106">Eine logische Einheit ist mit einem Pixel.</span><span class="sxs-lookup"><span data-stu-id="932e5-106">One logical unit equals one pixel.</span></span> <span data-ttu-id="932e5-107">Positives x ist rechts, und das positive y ist niedrig.</span><span class="sxs-lookup"><span data-stu-id="932e5-107">Positive x is to the right, and positive y is down.</span></span> <span data-ttu-id="932e5-108">Dieser Modus wird direkt dem Koordinatensystem des Geräts zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="932e5-108">This mode maps directly to the device's coordinate system.</span></span> <span data-ttu-id="932e5-109">Die Zuordnung zwischen logischen und physischen Dateien umfasst nur einen Offset in x und y, der durch das Anwendungs gesteuerte Fenster und die viewportursprünge definiert wird.</span><span class="sxs-lookup"><span data-stu-id="932e5-109">The logical-to-physical mapping involves only an offset in x and y that is defined by the application-controlled window and viewport origins.</span></span> <span data-ttu-id="932e5-110">Die Viewport-und Fensterblöcke werden alle auf 1 festgelegt und erstellen eine eins-zu-Eins-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="932e5-110">The viewport and window extents are all set to 1, creating a one-to-one mapping.</span></span>

<span data-ttu-id="932e5-111">Anwendungen, die geometrische Formen (Kreise, Quadrate, Polygone usw.) anzeigen, nutzen einen der geräteunabhängigen Karten Modi.</span><span class="sxs-lookup"><span data-stu-id="932e5-111">Applications that display geometric shapes (circles, squares, polygons, and so on) make use of one of the device-independent mapping modes.</span></span> <span data-ttu-id="932e5-112">Wenn Sie z. b. eine Anwendung schreiben, um Diagramm Funktionen für ein Tabellen Kalkulations Programm bereitzustellen, und sicherstellen möchten, dass der Durchmesser jedes Kreis Diagramms 2 Zoll beträgt, verwenden Sie den \_ Zuordnungsmodus von mm loenglish, und führen Sie die entsprechenden Funktionen zum Zeichnen und Ausfüllen des Diagramms aus.</span><span class="sxs-lookup"><span data-stu-id="932e5-112">For example, if you are writing an application to provide charting capabilities for a spreadsheet program and want to guarantee that the diameter of each pie chart is 2 inches, use the MM\_LOENGLISH mapping mode and call the appropriate functions to draw and fill the chart.</span></span> <span data-ttu-id="932e5-113">\_Durch die Angabe von mm-loenglish wird sichergestellt, dass der Durchmesser des Diagramms auf jedem Bildschirm oder Drucker konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="932e5-113">Specifying MM\_LOENGLISH, guarantees that the diameter of the chart is consistent on any display or printer.</span></span> <span data-ttu-id="932e5-114">Wenn \_ der mm-Text anstelle von mm- \_ loenglish verwendet wird, wird ein Diagramm, das in einer VGA-Anzeige zirkulär angezeigt wird, in einem EGA-Display als elliptisch angezeigt und auf einem 300 dpi-Laserdrucker (dpi pro Zoll) sehr klein angezeigt.</span><span class="sxs-lookup"><span data-stu-id="932e5-114">If MM\_TEXT is used instead of MM\_LOENGLISH, a chart that appears circular on a VGA display would appear elliptical on an EGA display and would appear very small on a 300 dpi (dots per inch) laser printer.</span></span>

 

 



