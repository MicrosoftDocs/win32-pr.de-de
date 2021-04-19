---
title: DWM-Meldungen
description: Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager (DWM)-Nachrichten.
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Desktopfenster-Manager (DWM), Referenz
- Dwm (Desktopfenster-Manager), Referenz
- Desktopfenster-Manager (DWM), Nachrichten
- Dwm (Desktopfenster-Manager), Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106339865"
---
# <a name="dwm-messages"></a><span data-ttu-id="6565d-107">DWM-Meldungen</span><span class="sxs-lookup"><span data-stu-id="6565d-107">DWM Messages</span></span>

<span data-ttu-id="6565d-108">Dieser Abschnitt enthält Informationen zu den Desktopfenster-Manager (DWM)-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6565d-108">This section contains information about the Desktop Window Manager (DWM) messages.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6565d-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6565d-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6565d-110">Thema</span><span class="sxs-lookup"><span data-stu-id="6565d-110">Topic</span></span></th>
<th><span data-ttu-id="6565d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6565d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6565d-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="6565d-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="6565d-113">Informiert alle Fenster der obersten Ebene darüber, dass sich die Farbe der Farbgebung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="6565d-113">Informs all top-level windows that the colorization color has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6565d-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="6565d-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="6565d-115">Informiert alle Fenster der obersten Ebene, dass die DWM-Komposition aktiviert oder deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="6565d-115">Informs all top-level windows that DWM composition has been enabled or disabled.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6565d-116">Ab Windows 8 ist die DWM-Komposition immer aktiviert, sodass diese Nachricht unabhängig von den videomodusänderungen nicht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="6565d-116">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6565d-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="6565d-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="6565d-118">Wird gesendet, wenn sich die Renderingleistung des nicht-Client Bereichs geändert hat</span><span class="sxs-lookup"><span data-stu-id="6565d-118">Sent when the non-client area rendering policy has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6565d-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span><span class="sxs-lookup"><span data-stu-id="6565d-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span></span><br/></td>
<td><span data-ttu-id="6565d-120">Weist ein Fenster an, eine statische Bitmap bereitzustellen, die als <em>Live Vorschau</em> (auch als <em>Vorschau Vorschau</em>bezeichnet) dieses Fensters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6565d-120">Instructs a window to provide a static bitmap to use as a <em>live preview</em> (also known as a <em>Peek preview</em>) of that window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6565d-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="6565d-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span></span><br/></td>
<td><span data-ttu-id="6565d-122">Weist ein Fenster an, ein statisches Bitmap bereitzustellen, das als Miniaturansicht dieses Fensters verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6565d-122">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6565d-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="6565d-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="6565d-124">Wird gesendet, wenn ein von der DWM-Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="6565d-124">Sent when a DWM composed window is maximized.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





