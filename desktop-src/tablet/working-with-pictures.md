---
description: In diesem Thema wird beschrieben, wie Bilder mithilfe der System. Windows. Forms. PictureBox. SizeMode-Eigenschaft angepasst werden und wie Bilder in Microsoft Visual Studio .net angezeigt werden.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Arbeiten mit Bildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a90c0d18253eaf4aea60eafc48bd1c24fcc3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346985"
---
# <a name="working-with-pictures"></a><span data-ttu-id="5a819-103">Arbeiten mit Bildern</span><span class="sxs-lookup"><span data-stu-id="5a819-103">Working with Pictures</span></span>

<span data-ttu-id="5a819-104">In diesem Thema wird beschrieben, wie Bilder mithilfe der [System. Windows. Forms. PictureBox. SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) -Eigenschaft angepasst werden und wie Bilder in Microsoft Visual Studio .net angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a819-104">This topic describes how to adjust pictures using the [System.Windows.Forms.PictureBox.SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property, and how to display pictures in Microsoft Visual Studio .NET.</span></span>

## <a name="the-sizemode-property"></a><span data-ttu-id="5a819-105">Die SizeMode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5a819-105">The SizeMode Property</span></span>

<span data-ttu-id="5a819-106">Sie können angeben, wie ein Bild im Steuerelement mit der [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) -Eigenschaft passt.</span><span class="sxs-lookup"><span data-stu-id="5a819-106">You can specify how an image fits in the control with the [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property.</span></span> <span data-ttu-id="5a819-107">Die SizeMode-Eigenschaft ist sowohl in der verwalteten Bibliothek als auch in der Automation-Bibliothek verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a819-107">The SizeMode property is available in both the Managed Library and in the Automation Library.</span></span> <span data-ttu-id="5a819-108">Mit SizeMode können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="5a819-108">With SizeMode you can:</span></span>

-   <span data-ttu-id="5a819-109">Passen Sie die Größe der Steuerelement Ränder an ein Bild an.</span><span class="sxs-lookup"><span data-stu-id="5a819-109">Resize the control borders to fit an image.</span></span>
-   <span data-ttu-id="5a819-110">Strecken Sie ein Bild, das an die Steuerelement Rahmen angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="5a819-110">Stretch an image to fit the control borders.</span></span>
-   <span data-ttu-id="5a819-111">Zentrieren Sie ein Bild innerhalb der Steuerelement Ränder.</span><span class="sxs-lookup"><span data-stu-id="5a819-111">Center an image within the control borders.</span></span>
-   <span data-ttu-id="5a819-112">Verankern Sie ein Bild in der linken oberen Ecke des Steuer Elements, ohne die Größe des Bilds oder Steuer Elements zu ändern (ein Bild kann möglicherweise nicht angezeigt werden, wenn Sie die Größe des Bilds oder Steuer Elements nicht ändern).</span><span class="sxs-lookup"><span data-stu-id="5a819-112">Anchor an image to the upper-left area of the control without resizing the image or control (some of the image may not be viewable if you do not resize the image or control).</span></span>

## <a name="working-with-pictures-in-visual-studio-net"></a><span data-ttu-id="5a819-113">Arbeiten mit Bildern in Visual Studio .net</span><span class="sxs-lookup"><span data-stu-id="5a819-113">Working with Pictures in Visual Studio .NET</span></span>

<span data-ttu-id="5a819-114">So zeigen Sie ein Bild zur Entwurfszeit in Visual Studio .net an:</span><span class="sxs-lookup"><span data-stu-id="5a819-114">To display an image at design time in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="5a819-115">Ziehen Sie ein [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement auf ein Formular, oder Doppelklicken Sie auf das InkPicture-Steuerelement in der Toolbox.</span><span class="sxs-lookup"><span data-stu-id="5a819-115">Drag an [InkPicture](/previous-versions/aa514604(v=msdn.10)) control on a form, or double-click the InkPicture control in the Toolbox.</span></span>
2.  <span data-ttu-id="5a819-116">Wählen Sie im Fenster **Eigenschaften** die Eigenschaft **Bild** aus, und klicken Sie dann auf die Schaltfläche mit den Auslassungs Punkten, um das Dialogfeld **Öffnen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5a819-116">In the **Properties** window, select the **Image** property, and then click the ellipsis button to open the **Open** dialog box.</span></span>
3.  <span data-ttu-id="5a819-117">Wenn Sie nach einem bestimmten Dateityp suchen (z. b. jpg-Dateien), wählen Sie ihn im Feld **Dateityp aus** .</span><span class="sxs-lookup"><span data-stu-id="5a819-117">If you are looking for a specific file type (for example, .jpg files), select it in the **Files of type** box.</span></span>
4.  <span data-ttu-id="5a819-118">Wählen Sie die Datei aus, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="5a819-118">Select the file you want to display.</span></span>

<span data-ttu-id="5a819-119">So löschen Sie das Bild zur Entwurfszeit:</span><span class="sxs-lookup"><span data-stu-id="5a819-119">To clear the picture at design time:</span></span>

1.  <span data-ttu-id="5a819-120">Wählen Sie im Fenster **Eigenschaften** die Eigenschaft **Image** aus, und klicken Sie mit der rechten Maustaste auf das Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="5a819-120">In the **Properties** window, select the **Image** property and right-click the thumbnail image.</span></span>
2.  <span data-ttu-id="5a819-121">Klicken Sie auf **Zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="5a819-121">Click **Reset**.</span></span>

<span data-ttu-id="5a819-122">Das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement wird standardmäßig ohne Ränder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5a819-122">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is displayed by default without any borders.</span></span> <span data-ttu-id="5a819-123">Sie können einen Standard-oder dreidimensionalen Rahmen mithilfe der [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) -Eigenschaft bereitstellen, um das InkPicture-Feld vom restlichen Formular zu unterscheiden, auch wenn es kein Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="5a819-123">You can provide a standard or three-dimensional border using the [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) property to distinguish the InkPicture box from the rest of the form, even if it contains no image.</span></span>

<span data-ttu-id="5a819-124">Sie können ein Bild zur Laufzeit mit der [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) -Methode des [System. Drawing. Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) -Objekts anzeigen:</span><span class="sxs-lookup"><span data-stu-id="5a819-124">You can display an image at run time with the [System.Drawing.Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) method:</span></span>


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



<span data-ttu-id="5a819-125">Sie können auch ein Hintergrundbild mit der [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) -Eigenschaft des geerbten [Bild](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) Objekts einschließen. das Image kann jedoch nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5a819-125">You can also include a background image with the inherited [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) property; however, that image cannot be resized.</span></span>

 

 
