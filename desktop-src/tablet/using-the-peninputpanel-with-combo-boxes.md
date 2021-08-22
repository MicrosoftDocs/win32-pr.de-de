---
description: Beschreibt die Verwendung des PenInputPanel-Objekts mit Kombinationsfeldern.
ms.assetid: 19902bfa-504e-40cd-882a-4fac4bb7daf6
title: Verwenden von PenInputPanel mit Kombinationsfeldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1e90d581e08f9a23346bbf13cf8c3866f6e947f1d9b23375248f3ba9c8636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589300"
---
# <a name="using-the-peninputpanel-with-combo-boxes"></a>Verwenden von PenInputPanel mit Kombinationsfeldern

\[Das [PenInputPanel-Objekt](/previous-versions/aa514041(v=msdn.10)) wurde durch [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100))ersetzt. Weitere Informationen finden Sie unter [Programmieren des Texteingabebereichs.](programming-the-text-input-panel.md)\]

Wenn Sie ein [PenInputPanel-Objekt](/previous-versions/aa514041(v=msdn.10)) an ein [ComboBox-Steuerelement](/dotnet/api/system.windows.forms.combobox?view=netcore-3.1) anfügen und dann zur Laufzeit auf den Tablettstift im Bearbeitungssteuerelement-Kombinationsfeld tippen, wird das PenInputPanel-Objekt nicht angezeigt. Sie wird jedoch angezeigt, wenn Sie auf den Dropdownpfeil tippen. Dies liegt daran, dass das Fenster des Bearbeitungssteuerelements im Kombinationsfeld nicht das Fenster ist, das Stiftmeldungen empfängt. Kombinationsfelder verfügen über ein untergeordnetes Bearbeitungsfenster. Die Lösung für dieses Problem besteht darin, zu bestimmen, ob das Fenster, an das das PenInputPanel-Objekt angefügt ist, über ein untergeordnetes Fenster verfügt. Wenn ja, können Sie das PenInputPanel-Objekt an das untergeordnete Fenster anfügen.

Wenn Sie die [VerticalOffset-Eigenschaft](/previous-versions/ms571983(v=vs.100)) des [PenInputPanel-Objekts](/previous-versions/aa514041(v=msdn.10)) auf den Wert -1 festlegen, wird der Bereich über dem Kombinationsfeld angezeigt.

 

 
