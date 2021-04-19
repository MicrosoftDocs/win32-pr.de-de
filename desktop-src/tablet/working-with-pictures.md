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
# <a name="working-with-pictures"></a>Arbeiten mit Bildern

In diesem Thema wird beschrieben, wie Bilder mithilfe der [System. Windows. Forms. PictureBox. SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) -Eigenschaft angepasst werden und wie Bilder in Microsoft Visual Studio .net angezeigt werden.

## <a name="the-sizemode-property"></a>Die SizeMode-Eigenschaft

Sie können angeben, wie ein Bild im Steuerelement mit der [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) -Eigenschaft passt. Die SizeMode-Eigenschaft ist sowohl in der verwalteten Bibliothek als auch in der Automation-Bibliothek verfügbar. Mit SizeMode können Sie folgende Aktionen ausführen:

-   Passen Sie die Größe der Steuerelement Ränder an ein Bild an.
-   Strecken Sie ein Bild, das an die Steuerelement Rahmen angepasst wird.
-   Zentrieren Sie ein Bild innerhalb der Steuerelement Ränder.
-   Verankern Sie ein Bild in der linken oberen Ecke des Steuer Elements, ohne die Größe des Bilds oder Steuer Elements zu ändern (ein Bild kann möglicherweise nicht angezeigt werden, wenn Sie die Größe des Bilds oder Steuer Elements nicht ändern).

## <a name="working-with-pictures-in-visual-studio-net"></a>Arbeiten mit Bildern in Visual Studio .net

So zeigen Sie ein Bild zur Entwurfszeit in Visual Studio .net an:

1.  Ziehen Sie ein [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement auf ein Formular, oder Doppelklicken Sie auf das InkPicture-Steuerelement in der Toolbox.
2.  Wählen Sie im Fenster **Eigenschaften** die Eigenschaft **Bild** aus, und klicken Sie dann auf die Schaltfläche mit den Auslassungs Punkten, um das Dialogfeld **Öffnen** zu öffnen.
3.  Wenn Sie nach einem bestimmten Dateityp suchen (z. b. jpg-Dateien), wählen Sie ihn im Feld **Dateityp aus** .
4.  Wählen Sie die Datei aus, die Sie anzeigen möchten.

So löschen Sie das Bild zur Entwurfszeit:

1.  Wählen Sie im Fenster **Eigenschaften** die Eigenschaft **Image** aus, und klicken Sie mit der rechten Maustaste auf das Miniaturbild.
2.  Klicken Sie auf **Zurücksetzen**.

Das [InkPicture](/previous-versions/aa514604(v=msdn.10)) -Steuerelement wird standardmäßig ohne Ränder angezeigt. Sie können einen Standard-oder dreidimensionalen Rahmen mithilfe der [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) -Eigenschaft bereitstellen, um das InkPicture-Feld vom restlichen Formular zu unterscheiden, auch wenn es kein Bild enthält.

Sie können ein Bild zur Laufzeit mit der [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) -Methode des [System. Drawing. Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) -Objekts anzeigen:


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



Sie können auch ein Hintergrundbild mit der [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) -Eigenschaft des geerbten [Bild](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) Objekts einschließen. das Image kann jedoch nicht geändert werden.

 

 
