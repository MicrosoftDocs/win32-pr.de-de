---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- MCI-Geräte, MCIAVI-Treiber
- MCI-Befehle, MCIAVI-Treiber
- MCIAVI-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471469"
---
# <a name="mciavi"></a><span data-ttu-id="e9ba2-106">MCIAVI</span><span class="sxs-lookup"><span data-stu-id="e9ba2-106">MCIAVI</span></span>

<span data-ttu-id="e9ba2-107">Eine AVI-Datei kann mehr als zwei Streams enthalten – z. b. eine Videosequenz, einen englischen Sound Sound und einen französischen Sound.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-107">An AVI file can contain more than two streams — for example, a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="e9ba2-108">Die Anwendung kann einen Stream unabhängig von den anderen Datenströmen in der Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-108">Your application can use a stream independently of the other streams in the file.</span></span>

<span data-ttu-id="e9ba2-109">Der **Digitalvideo** -Gerätetyp steuert Videodateien.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-109">The **digitalvideo** device type controls video files.</span></span> <span data-ttu-id="e9ba2-110">Eine Liste der von Digital-Video-Geräten erkannten MCI-Befehle finden Sie unter [Digital-Video Command Set](digital-video-command-set.md).</span><span class="sxs-lookup"><span data-stu-id="e9ba2-110">For a list of the MCI commands recognized by digital-video devices, see [Digital-Video Command Set](digital-video-command-set.md).</span></span>

<span data-ttu-id="e9ba2-111">Der MCIAVI-Treiber gibt Videosequenzen und andere Datenströme unter der Kontrolle über MCI-Befehle wieder.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-111">The MCIAVI driver plays video sequences and other data streams under the control of MCI commands.</span></span> <span data-ttu-id="e9ba2-112">Datenströme können Bilder, Audiodaten und Paletten enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-112">Data streams can contain images, audio, and palettes.</span></span> <span data-ttu-id="e9ba2-113">Die Bilddaten können aus Bildern mit Farbpaletten oder echten Farbinformationen bestehen.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-113">The image data can consist of images with either color palettes or true-color information.</span></span>

<span data-ttu-id="e9ba2-114">Audiodaten werden mit dem Video innerhalb von einem Drittel einer Sekunde synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-114">Audio is synchronized with the video within one-thirtieth of a second.</span></span> <span data-ttu-id="e9ba2-115">Wenn keine Audiohardware verfügbar ist, gibt der Treiber jedoch nur den Videostream aus.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-115">If audio hardware is not available, however, the driver plays only the video stream.</span></span> <span data-ttu-id="e9ba2-116">Der MCIAVI-Treiber kann bei Bedarf Video Frames ablegen, um einen Stream ohne audiounterbrechung wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-116">The MCIAVI driver can drop video frames, if necessary, to play a stream without audio interruption.</span></span>

<span data-ttu-id="e9ba2-117">Die Anwendung kann die mciwnd-Fenster Klassen Dienste anstelle der MCI-Befehlsschnittstelle verwenden, um einen beliebigen MCI-Treiber zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-117">Your application can use the MCIWnd window class services instead of the MCI command interface to control any MCI driver.</span></span> <span data-ttu-id="e9ba2-118">Diese Fenster Klasse behandelt viele der Details der Verwaltung des Fensters, das das MCI-Gerät unterstützt, und vereinfacht die zum Senden der MCI-Befehle erforderliche Programmierung.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-118">This window class handles many of the details of managing the window supporting the MCI device and simplifies the programming required to send the MCI commands.</span></span> <span data-ttu-id="e9ba2-119">Die Anwendung kann die mciwnd-Bibliotheksdienste direkt verwenden, um das MCI-Gerät zu steuern. Alternativ kann mciwnd eine Symbolleiste, eine Scrollleiste und Menüs anzeigen, mit denen der Benutzer das Gerät steuern kann.</span><span class="sxs-lookup"><span data-stu-id="e9ba2-119">Your application can use the MCIWnd library services directly to control the MCI device, or it can have MCIWnd display a toolbar, scroll bar, and menus that let the user control the device.</span></span> <span data-ttu-id="e9ba2-120">Weitere Informationen zur mciwnd-Fenster Klasse finden Sie unter [mciwnd Window Class](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="e9ba2-120">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span>

 

 




