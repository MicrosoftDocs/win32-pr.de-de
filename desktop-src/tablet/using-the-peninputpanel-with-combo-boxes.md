---
description: Beschreibt die Verwendung des "pinputpanel"-Objekts mit Kombinations Feldern.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Verwenden des "" "" "" "" "" ""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5306708fd00871f07b241ca777e672e2d3de94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751264"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a><span data-ttu-id="27a1c-103">Verwenden des "" "" "" "" "" ""</span><span class="sxs-lookup"><span data-stu-id="27a1c-103">Using the PenInputPanel with Combo Boxes</span></span>

<span data-ttu-id="27a1c-104">\[Das Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " wurde durch " [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100))" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="27a1c-104">\[The [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="27a1c-105">Weitere Informationen finden Sie im Abschnitt [Programmieren des Text Eingabe](programming-the-text-input-panel.md)Bereichs.\]</span><span class="sxs-lookup"><span data-stu-id="27a1c-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="27a1c-106">Wenn Sie ein [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) -Objekt an ein [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) -Steuerelement anfügen, tippen Sie auf den Tablettstift im Kombinations Feld Steuerungsteil bearbeiten zur Laufzeit. das PenInputPanel-Objekt wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27a1c-106">If you attach a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) control, then tap your tablet pen on the edit control portion combo box at runtime, the PenInputPanel object does not appear.</span></span> <span data-ttu-id="27a1c-107">Sie wird jedoch angezeigt, wenn Sie auf den Dropdown Pfeil tippen.</span><span class="sxs-lookup"><span data-stu-id="27a1c-107">However, it does appear if you tap on the dropdown arrow.</span></span> <span data-ttu-id="27a1c-108">Dies liegt daran, dass es sich bei dem Fenster des Bearbeitungs Steuer Elements im Kombinations Feld nicht um das Fenster handelt, das Stift Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="27a1c-108">This is because the window of the edit control in the combo box is not the window that receives pen messages.</span></span> <span data-ttu-id="27a1c-109">Kombinations Felder verfügen über ein untergeordnetes Bearbeitungsfenster.</span><span class="sxs-lookup"><span data-stu-id="27a1c-109">Combo boxes have a child edit window.</span></span> <span data-ttu-id="27a1c-110">Die Lösung für dieses Problem besteht darin, zu bestimmen, ob das Fenster, an das das Objekt "das"-Objekt angefügt ist, ein untergeordnetes Fenster hat.</span><span class="sxs-lookup"><span data-stu-id="27a1c-110">The solution to this problem is to determine whether the window the PenInputPanel object is attached to has a child window.</span></span> <span data-ttu-id="27a1c-111">Wenn dies der Fall ist, können Sie das Objekt "pinputpanel" an das untergeordnete Fenster anfügen.</span><span class="sxs-lookup"><span data-stu-id="27a1c-111">If so, you can attach the PenInputPanel object to the child window.</span></span>

<span data-ttu-id="27a1c-112">Wenn Sie die [VerticalOffset](/previous-versions/ms571983(v=vs.100)) -Eigenschaft des " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekts auf den Wert "-1" festlegen, wird der Bereich oben im Kombinations Feld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27a1c-112">Setting the [VerticalOffset](/previous-versions/ms571983(v=vs.100)) property of the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) object to a value of -1 makes the panel appear on top of the combo box.</span></span>

 

 
