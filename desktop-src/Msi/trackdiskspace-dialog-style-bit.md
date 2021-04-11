---
description: Wenn dieses Bit festgelegt ist, ruft das Dialogfeld den Installer regelmäßig auf.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: Trackdiskspace-Dialog Feld-Stilbit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128109"
---
# <a name="trackdiskspace-dialog-style-bit"></a>Trackdiskspace-Dialog Feld-Stilbit

Wenn dieses Bit festgelegt ist, ruft das Dialogfeld den Installer regelmäßig auf. Wenn sich die-Eigenschaft ändert, werden die-Steuerelemente im Dialogfeld benachrichtigt. Dieser Stil kann verwendet werden, wenn ein Steuerelement im Dialogfeld vorhanden ist, das den Speicherplatz angibt. Wenn der Benutzer zu einer anderen Anwendung wechselt, Dateien hinzufügt oder entfernt oder den verfügbaren Speicherplatz anderweitig ändert, können Sie die Änderung schnell mithilfe dieses Stils implementieren.

Alle Dialogfelder, die sich auf die [**ouesfdiskspace**](outofdiskspace.md) -Eigenschaft verlassen, um zu bestimmen, ob ein Dialogfeld angezeigt werden soll, müssen das Dialogfeld "trackdiskspace"-Dialogfeld für den Dialog festlegen, um den Speicherplatz auf den Zielvolumes

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbdialogattributestrackdiskspace** |



 

 

 



