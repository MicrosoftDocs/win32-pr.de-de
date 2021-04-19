---
title: Anpassen eines Miniaturansichtsymbols und einer Bitmap für die Livevorschau
description: Zeigt, wie Sie eine Miniaturansicht und eine Live Vorschau-Bitmap (auch als Peek Preview bezeichnet) anpassen können.
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106364022"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a><span data-ttu-id="b49f4-103">Anpassen eines Miniaturansichtsymbols und einer Bitmap für die Livevorschau</span><span class="sxs-lookup"><span data-stu-id="b49f4-103">Customize an Iconic Thumbnail and a Live Preview Bitmap</span></span>

## <a name="description"></a><span data-ttu-id="b49f4-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b49f4-104">Description</span></span>

<span data-ttu-id="b49f4-105">Sie können eine Miniaturansicht und eine *Live Vorschau* (oder *Peek Preview*)-Bitmap mithilfe von Funktionen und Nachrichten anpassen, die in den Windows 7-Desktopfenster-Manager-APIs (DWM) eingeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b49f4-105">You can customize an iconic thumbnail and a *live preview* (or *Peek preview*) bitmap by using functions and messages that are introduced in the Windows 7 Desktop Window Manager (DWM) APIs.</span></span>

<span data-ttu-id="b49f4-106">Insbesondere verwenden Sie die Funktion " [**dwmstisubicminiatur**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) " und die " [**WM \_ sendianicthumbnailbitmap**](wm-dwmsendiconicthumbnail.md) "-Meldung, um eine Miniaturansicht anzupassen.</span><span class="sxs-lookup"><span data-stu-id="b49f4-106">Specifically, you use the [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function and the [**WM\_SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) message to customize an iconic thumbnail.</span></span> <span data-ttu-id="b49f4-107">Sie können auch die [**dwmseticoniclivepreviewbitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) -Funktion und die [**WM- \_ sendiconiclivepreviewbitmap**](wm-dwmsendiconiclivepreviewbitmap.md) -Nachricht verwenden, um eine legendäre Live Vorschau-Bitmap festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b49f4-107">You can also use the [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) function and the [**WM\_SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) message to set an iconic live preview bitmap.</span></span>

<span data-ttu-id="b49f4-108">Eine Beispielanwendung, die die Funktion " **dwmseticonfiguration** " verwendet, finden Sie unter [Beispiel für tabminiatur Ansichten](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span><span class="sxs-lookup"><span data-stu-id="b49f4-108">For a sample application that uses the **DwmSetIconicThumbnail** function, see [TabThumbnails sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).</span></span>

<span data-ttu-id="b49f4-109">Die folgende Abbildung zeigt eine in eine angepasste Miniaturansicht transformierte Standard Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="b49f4-109">The following illustration shows a default thumbnail transformed into a customized thumbnail.</span></span>

![Abbildung eines ursprünglichen Miniatur Bilds und eines geänderten Miniatur Bilds mit einer benutzerdefinierten Bitmap](images/customthumbnail.jpg)

## <a name="requirements"></a><span data-ttu-id="b49f4-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b49f4-111">Requirements</span></span>

| <span data-ttu-id="b49f4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b49f4-112">Requirement</span></span> | <span data-ttu-id="b49f4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b49f4-113">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b49f4-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b49f4-114">Minimum supported client</span></span> | <span data-ttu-id="b49f4-115">Windows 7 oder Windows Vista mit Service Pack 2 (SP2) und Platt Form Update für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b49f4-115">Windows 7 or Windows Vista with Service Pack 2 (SP2) and Platform Update for Windows Vista</span></span>                          |
| <span data-ttu-id="b49f4-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b49f4-116">Minimum supported server</span></span> | <span data-ttu-id="b49f4-117">Windows Server 2008 R2 oder Windows Server 2008 mit Service Pack 2 (SP2) und Platt Form Update für Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b49f4-117">Windows Server 2008 R2 or Windows Server 2008 with Service Pack 2 (SP2) and Platform Update for Windows Server 2008</span></span> |
| <span data-ttu-id="b49f4-118">Minimale Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b49f4-118">Minimum Windows SDK</span></span>      | [<span data-ttu-id="b49f4-119">Windows Software Development Kit (SDK) für Windows 7</span><span class="sxs-lookup"><span data-stu-id="b49f4-119">Windows Software Development Kit (SDK) for Windows 7</span></span>](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a><span data-ttu-id="b49f4-120">Aufbauen des tabthumbnails-Beispiels</span><span class="sxs-lookup"><span data-stu-id="b49f4-120">Building the TabThumbnails sample</span></span>

<span data-ttu-id="b49f4-121">**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugte Methode)**</span><span class="sxs-lookup"><span data-stu-id="b49f4-121">**To build the sample by using Microsoft Visual Studio (preferred method)**</span></span>

1.  <span data-ttu-id="b49f4-122">Öffnen Sie Windows-Explorer, und navigieren Sie zu dem Ordner, in dem sich die Datei "tabthumbnails. sln" befindet.</span><span class="sxs-lookup"><span data-stu-id="b49f4-122">Open Windows Explorer and browse to the folder where the TabThumbnails.sln file is located.</span></span>
2.  <span data-ttu-id="b49f4-123">Doppelklicken Sie auf die Projektmappendatei (. sln), um die Datei in Microsoft Visual Studio zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b49f4-123">Double-click the solution file (.sln) to open the file in Microsoft Visual Studio.</span></span>
3.  <span data-ttu-id="b49f4-124">Klicken Sie im Menü **Erstellen** auf **Projektmappe erstellen**.</span><span class="sxs-lookup"><span data-stu-id="b49f4-124">On the **Build** menu, click **Build Solution**.</span></span> <span data-ttu-id="b49f4-125">Die Anwendung wird im standardmäßigen \\ Debug-oder \\ releaseverzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="b49f4-125">The application is built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="b49f4-126">**So erstellen Sie das Beispiel mithilfe der Eingabeaufforderung**</span><span class="sxs-lookup"><span data-stu-id="b49f4-126">**To build the sample by using the command prompt**</span></span>

1.  <span data-ttu-id="b49f4-127">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zum Beispiel Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b49f4-127">Open a Command Prompt window and browse to the sample directory.</span></span>
2.  <span data-ttu-id="b49f4-128">Geben Sie `msbuild TabThumbnails.sln` ein.</span><span class="sxs-lookup"><span data-stu-id="b49f4-128">Enter `msbuild TabThumbnails.sln`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b49f4-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b49f4-129">Related topics</span></span>

[<span data-ttu-id="b49f4-130">Desktopfenster-Manager</span><span class="sxs-lookup"><span data-stu-id="b49f4-130">Desktop Window Manager</span></span>](dwm-overview.md)

[<span data-ttu-id="b49f4-131">Windows-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="b49f4-131">Windows Development</span></span>](/windows/desktop/win32-and-com-development)
