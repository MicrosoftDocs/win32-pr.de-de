---
title: Anhang F Objekt-ID-Werte für OBJID_QUERYCLASSNAMEIDX
description: Wenn oleacc eine WM- \_ GetObject-Nachricht mit dem lParam-Parameter sendet, die auf objidqueryclassnameidx festgelegt ist, geben viele Standardbenutzer-oder allgemeine Steuerelemente (COMCTL) einen der folgenden Werte zurück.
ms.assetid: 2a54973c-7dfa-49af-8fd0-925fafa256ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faffd8382820aef2cd341ce54b23c9e9e7c9a59b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342364"
---
# <a name="appendix-f-object-identifier-values-for-objid_queryclassnameidx"></a><span data-ttu-id="9afdb-103">Anhang F: objektbezeichnerwerte für objID \_ queryclassnameidx</span><span class="sxs-lookup"><span data-stu-id="9afdb-103">Appendix F: Object Identifier Values for OBJID\_QUERYCLASSNAMEIDX</span></span>

<span data-ttu-id="9afdb-104">Wenn oleacc eine [**WM- \_ GetObject**](wm-getobject.md) -Nachricht mit dem *LPARAM* -Parameter sendet, die auf objidqueryclassnameidx festgelegt ist, geben viele Standardbenutzer-oder allgemeine Steuerelemente (COMCTL) einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9afdb-104">When OLEACC sends a [**WM\_GETOBJECT**](wm-getobject.md) message with the *lParam* parameter set to OBJIDQUERYCLASSNAMEIDX, many standard USER or common controls (COMCTL) return one of the following values.</span></span>



| <span data-ttu-id="9afdb-105">Benutzer-oder gängiges Steuerelement</span><span class="sxs-lookup"><span data-stu-id="9afdb-105">USER or common control</span></span> | <span data-ttu-id="9afdb-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9afdb-106">Return value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="9afdb-107">Listenfeld</span><span class="sxs-lookup"><span data-stu-id="9afdb-107">Listbox</span></span>                | <span data-ttu-id="9afdb-108">65536 + 0</span><span class="sxs-lookup"><span data-stu-id="9afdb-108">65536+0</span></span>      |
| <span data-ttu-id="9afdb-109">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="9afdb-109">Button</span></span>                 | <span data-ttu-id="9afdb-110">65536 + 2</span><span class="sxs-lookup"><span data-stu-id="9afdb-110">65536+2</span></span>      |
| <span data-ttu-id="9afdb-111">statischen</span><span class="sxs-lookup"><span data-stu-id="9afdb-111">Static</span></span>                 | <span data-ttu-id="9afdb-112">65536 + 3</span><span class="sxs-lookup"><span data-stu-id="9afdb-112">65536+3</span></span>      |
| <span data-ttu-id="9afdb-113">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="9afdb-113">Edit</span></span>                   | <span data-ttu-id="9afdb-114">65536 + 4</span><span class="sxs-lookup"><span data-stu-id="9afdb-114">65536+4</span></span>      |
| <span data-ttu-id="9afdb-115">Combobox</span><span class="sxs-lookup"><span data-stu-id="9afdb-115">Combobox</span></span>               | <span data-ttu-id="9afdb-116">65536 + 5</span><span class="sxs-lookup"><span data-stu-id="9afdb-116">65536+5</span></span>      |
| <span data-ttu-id="9afdb-117">Bildlaufleiste</span><span class="sxs-lookup"><span data-stu-id="9afdb-117">Scrollbar</span></span>              | <span data-ttu-id="9afdb-118">65536 + 10</span><span class="sxs-lookup"><span data-stu-id="9afdb-118">65536+10</span></span>     |
| <span data-ttu-id="9afdb-119">Status</span><span class="sxs-lookup"><span data-stu-id="9afdb-119">Status</span></span>                 | <span data-ttu-id="9afdb-120">65536 + 11</span><span class="sxs-lookup"><span data-stu-id="9afdb-120">65536+11</span></span>     |
| <span data-ttu-id="9afdb-121">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="9afdb-121">Toolbar</span></span>                | <span data-ttu-id="9afdb-122">65536 + 12</span><span class="sxs-lookup"><span data-stu-id="9afdb-122">65536+12</span></span>     |
| <span data-ttu-id="9afdb-123">Fortschritt</span><span class="sxs-lookup"><span data-stu-id="9afdb-123">Progress</span></span>               | <span data-ttu-id="9afdb-124">65536 + 13</span><span class="sxs-lookup"><span data-stu-id="9afdb-124">65536+13</span></span>     |
| <span data-ttu-id="9afdb-125">Belebt</span><span class="sxs-lookup"><span data-stu-id="9afdb-125">Animate</span></span>                | <span data-ttu-id="9afdb-126">65536 + 14</span><span class="sxs-lookup"><span data-stu-id="9afdb-126">65536+14</span></span>     |
| <span data-ttu-id="9afdb-127">Registerkarte</span><span class="sxs-lookup"><span data-stu-id="9afdb-127">Tab</span></span>                    | <span data-ttu-id="9afdb-128">65536 + 15</span><span class="sxs-lookup"><span data-stu-id="9afdb-128">65536+15</span></span>     |
| <span data-ttu-id="9afdb-129">Hotkey</span><span class="sxs-lookup"><span data-stu-id="9afdb-129">Hotkey</span></span>                 | <span data-ttu-id="9afdb-130">65536 + 16</span><span class="sxs-lookup"><span data-stu-id="9afdb-130">65536+16</span></span>     |
| <span data-ttu-id="9afdb-131">Header</span><span class="sxs-lookup"><span data-stu-id="9afdb-131">Header</span></span>                 | <span data-ttu-id="9afdb-132">65536 + 17</span><span class="sxs-lookup"><span data-stu-id="9afdb-132">65536+17</span></span>     |
| <span data-ttu-id="9afdb-133">TrackBar</span><span class="sxs-lookup"><span data-stu-id="9afdb-133">Trackbar</span></span>               | <span data-ttu-id="9afdb-134">65536 + 18</span><span class="sxs-lookup"><span data-stu-id="9afdb-134">65536+18</span></span>     |
| <span data-ttu-id="9afdb-135">ListView</span><span class="sxs-lookup"><span data-stu-id="9afdb-135">Listview</span></span>               | <span data-ttu-id="9afdb-136">65536 + 19</span><span class="sxs-lookup"><span data-stu-id="9afdb-136">65536+19</span></span>     |
| <span data-ttu-id="9afdb-137">UpDown</span><span class="sxs-lookup"><span data-stu-id="9afdb-137">Updown</span></span>                 | <span data-ttu-id="9afdb-138">65536 + 22</span><span class="sxs-lookup"><span data-stu-id="9afdb-138">65536+22</span></span>     |
| <span data-ttu-id="9afdb-139">Quick Infos</span><span class="sxs-lookup"><span data-stu-id="9afdb-139">ToolTips</span></span>               | <span data-ttu-id="9afdb-140">65536 + 24</span><span class="sxs-lookup"><span data-stu-id="9afdb-140">65536+24</span></span>     |
| <span data-ttu-id="9afdb-141">TreeView</span><span class="sxs-lookup"><span data-stu-id="9afdb-141">Treeview</span></span>               | <span data-ttu-id="9afdb-142">65536 + 25</span><span class="sxs-lookup"><span data-stu-id="9afdb-142">65536+25</span></span>     |
| <span data-ttu-id="9afdb-143">RichEdit</span><span class="sxs-lookup"><span data-stu-id="9afdb-143">RichEdit</span></span>               | <span data-ttu-id="9afdb-144">65536 + 28</span><span class="sxs-lookup"><span data-stu-id="9afdb-144">65536+28</span></span>     |



 

<span data-ttu-id="9afdb-145">Nur Benutzer und allgemeine Windows-Steuerelemente (COMCTL) geben einen der Werte aus der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="9afdb-145">Only USER and Windows common controls (COMCTL) will return one of the values from the table.</span></span> <span data-ttu-id="9afdb-146">Wenn ein Fenster als Antwort auf diese Meldung 0 zurückgibt, kann das Fenster eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="9afdb-146">If a window returns 0 in response to this message, the window may be one of the following:</span></span>

-   <span data-ttu-id="9afdb-147">Benutzerdefiniertes Steuerelement</span><span class="sxs-lookup"><span data-stu-id="9afdb-147">A custom control</span></span>
-   <span data-ttu-id="9afdb-148">Ein anderes Steuerelement als eines der Steuerelemente in der vorherigen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9afdb-148">A control other than one of the controls in the previous table</span></span>
-   <span data-ttu-id="9afdb-149">Eine alte Version eines System Steuer Elements, das die WM- [**\_ GetObject**](wm-getobject.md) -Nachricht nicht erkennt</span><span class="sxs-lookup"><span data-stu-id="9afdb-149">An old version of a system control that does not recognize the [**WM\_GETOBJECT**](wm-getobject.md) message</span></span>

<span data-ttu-id="9afdb-150">Wenn ein Fenster 0 zurückgibt, müssen die Clients möglicherweise " [**realgetwindowclass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) " oder " [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)" verwenden.</span><span class="sxs-lookup"><span data-stu-id="9afdb-150">If a window returns 0, clients may need to use [**RealGetWindowClass**](/windows/win32/api/winuser/nf-winuser-realgetwindowclassw) or [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname).</span></span> <span data-ttu-id="9afdb-151">Sie können diese Funktionen verwenden, um den Typ des Steuer Elements basierend auf dem Klassennamen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9afdb-151">You can use these functions to determine the type of control based on class name.</span></span>

<span data-ttu-id="9afdb-152">Im Allgemeinen können Clients die von oleacc bereitgestellten Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9afdb-152">In general, clients can use the information provided by OLEACC.</span></span>

 

 