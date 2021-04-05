---
description: Entwickler können verhindern, dass vertrauliche Informationen (z. b. Kenn Wörter) während einer Windows Installer-Installation in die Protokolldatei eingegeben werden.
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042140"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a>Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden

Wenn Sie die Windows Installer verwenden, können Sie verhindern, dass vertrauliche Informationen, z. b. Kenn Wörter, in die Protokolldatei eingegeben und sichtbar gemacht werden.

-   Das Installationsprogramm schreibt die Informationen in der Spalte Kennwort der [Tabelle ServiceInstall](serviceinstall-table.md) niemals in das Protokoll.
-   Sie können verhindern, dass das Installationsprogramm die Eigenschaft, die mit einem [Bearbeitungs Steuer](edit-control.md) Element verknüpft ist, in das Protokoll schreibt, indem Sie das Kenn [Wort Steuerungs Attribut](password-control-attribute.md)festlegen. Die Eigenschaft, die mit einem Bearbeitungs Steuerelement verknüpft ist, das über das Kenn Wort Steuerelement-Attribut verfügt, wird ausgeblendet, auch wenn die [debugrichtlinie](debug.md) auf den Wert 7 festgelegt
-   Sie können verhindern, dass das Installationsprogramm eine private-Eigenschaft in das Protokoll schreibt, indem Sie die-Eigenschaft in die [**msihiddenproperties**](msihiddenproperties.md) -Eigenschaft einschließen.
    > [!Note]  
    > Mit dieser Methode können vertrauliche Informationen in einer Befehlszeile eingegeben werden, die im Protokoll sichtbar ist. Wenn die [debugrichtlinie](debug.md) auf den Wert 7 festgelegt ist, schreibt das Installationsprogramm Informationen, die in der Befehlszeile eingegeben werden, in das Protokoll. Dadurch wird die Eigenschaft, die in einer Befehlszeile eingegeben wird, auch dann sichtbar, wenn die Eigenschaft in der [**msihiddenproperties**](msihiddenproperties.md) -Eigenschaft enthalten ist.

     

-   Sie können verhindern, dass die Informationen in der Ziel Spalte der Tabelle [CustomAction](customaction-table.md) in das Protokoll geschrieben werden, indem Sie das hidetarget-Bitflag in das type-Feld der CustomAction-Tabelle einschließen. Der Wert dieses Flags ist 8192 (0x2000). Weitere Informationen finden Sie unter Option für ausgeblendete [Ziel benutzerdefinierte Aktionen](custom-action-hidden-target-option.md).

 

 



