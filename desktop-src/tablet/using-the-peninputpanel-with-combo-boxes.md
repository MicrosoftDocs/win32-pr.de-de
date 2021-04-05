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
# <a name="using-the-peninputpanel-with-combo-boxes"></a>Verwenden des "" "" "" "" "" ""

\[Das Objekt " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) " wurde durch " [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100))" ersetzt. Weitere Informationen finden Sie im Abschnitt [Programmieren des Text Eingabe](programming-the-text-input-panel.md)Bereichs.\]

Wenn Sie ein [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) -Objekt an ein [ComboBox](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) -Steuerelement anfügen, tippen Sie auf den Tablettstift im Kombinations Feld Steuerungsteil bearbeiten zur Laufzeit. das PenInputPanel-Objekt wird nicht angezeigt. Sie wird jedoch angezeigt, wenn Sie auf den Dropdown Pfeil tippen. Dies liegt daran, dass es sich bei dem Fenster des Bearbeitungs Steuer Elements im Kombinations Feld nicht um das Fenster handelt, das Stift Nachrichten empfängt. Kombinations Felder verfügen über ein untergeordnetes Bearbeitungsfenster. Die Lösung für dieses Problem besteht darin, zu bestimmen, ob das Fenster, an das das Objekt "das"-Objekt angefügt ist, ein untergeordnetes Fenster hat. Wenn dies der Fall ist, können Sie das Objekt "pinputpanel" an das untergeordnete Fenster anfügen.

Wenn Sie die [VerticalOffset](/previous-versions/ms571983(v=vs.100)) -Eigenschaft des " [pinputpanel](/previous-versions/aa514041(v=msdn.10)) "-Objekts auf den Wert "-1" festlegen, wird der Bereich oben im Kombinations Feld angezeigt.

 

 
