---
description: In diesem Thema wird beschrieben, wie Bilder mithilfe des -Systems angepasst werden. Windows. Forms.PictureBox.SizeMode-Eigenschaft und Anzeigen von Bildern in Microsoft Visual Studio .NET.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Arbeiten mit Bildern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6e3331d384f30084082e8ef29c5a3a5b44232843bc834a8282bf1786a088d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449177"
---
# <a name="working-with-pictures"></a>Arbeiten mit Bildern

In diesem Thema wird beschrieben, wie Bilder mit [system.Windows angepasst werden. Forms.PictureBox.SizeMode-Eigenschaft](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) und Anzeigen von Bildern in Microsoft Visual Studio .NET.

## <a name="the-sizemode-property"></a>Die SizeMode-Eigenschaft

Mit der [SizeMode-Eigenschaft](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) können Sie angeben, wie ein Bild in das Steuerelement passt. Die SizeMode-Eigenschaft ist sowohl in der verwalteten Bibliothek als auch in der Automation Library verfügbar. Mit SizeMode können Sie:

-   Ändern Sie die Größe der Steuerelementrahmen an ein Bild.
-   Strecken Sie ein Bild so, dass es an die Rahmen des Steuerelements passt.
-   Zentren Sie ein Bild innerhalb der Rahmen des Steuerelements.
-   Verankern Sie ein Bild im linken oberen Bereich des Steuerelements, ohne die Größe des Bilds oder Steuerelements zu ändern (ein Teil des Bilds kann möglicherweise nicht angezeigt werden, wenn Sie die Größe des Bilds oder Steuerelements nicht ändern).

## <a name="working-with-pictures-in-visual-studio-net"></a>Arbeiten mit Bildern in Visual Studio .NET

So zeigen Sie ein Bild zur Entwurfszeit in Visual Studio .NET an:

1.  Ziehen Sie ein [InkPicture-Steuerelement](/previous-versions/aa514604(v=msdn.10)) auf ein Formular, oder doppelklicken Sie in der Toolbox auf das Steuerelement InkPicture.
2.  Wählen Sie **im** Eigenschaftenfenster die Eigenschaft **Image** aus, und klicken Sie dann auf die Schaltfläche mit den Auslassungszeichen, um das Dialogfeld **Öffnen** zu öffnen.
3.  Wenn Sie nach einem bestimmten Dateityp suchen (z. B. .jpg Dateien), wählen Sie ihn im Feld **Dateien vom Typ aus.**
4.  Wählen Sie die Datei aus, die Sie anzeigen möchten.

So löschen Sie das Bild zur Entwurfszeit:

1.  Wählen Sie im Fenster **Eigenschaften** die Eigenschaft **Bild** aus, und klicken Sie mit der rechten Maustaste auf das Miniaturbild.
2.  Klicken Sie auf **Zurücksetzen**.

Das [InkPicture-Steuerelement](/previous-versions/aa514604(v=msdn.10)) wird standardmäßig ohne Rahmen angezeigt. Sie können einen standard- oder dreidimensionalen Rahmen mithilfe der [BorderStyle-Eigenschaft](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) bereitstellen, um das Feld InkPicture vom Rest des Formulars zu unterscheiden, auch wenn es kein Bild enthält.

Sie können ein Bild zur Laufzeit mit der [FromFile-Methode](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) des [System.Drawing.Image-Objekts](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) anzeigen:


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



Sie können auch ein Hintergrundbild mit der [BackgroundImage-Eigenschaft](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) des geerbten [Image-Objekts](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) einschließen. Die Größe dieses Bilds kann jedoch nicht geändert werden.

 

 
