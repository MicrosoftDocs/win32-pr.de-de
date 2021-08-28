---
description: Wenn dieses Bit festgelegt ist, ruft das Dialogfeld in regelmäßigen Abständen das Installationsprogramm auf.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: TrackDiskSpace Dialog Style Bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e12a77f0b7e67bd82e094953a2bacd8204d93b444dc6bd1dc378602e67809
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810570"
---
# <a name="trackdiskspace-dialog-style-bit"></a>TrackDiskSpace Dialog Style Bit

Wenn dieses Bit festgelegt ist, ruft das Dialogfeld in regelmäßigen Abständen das Installationsprogramm auf. Wenn sich die Eigenschaft ändert, werden die Steuerelemente im Dialogfeld benachrichtigt. Dieser Stil kann verwendet werden, wenn im Dialogfeld ein Steuerelement vorhanden ist, das Speicherplatz angibt. Wenn der Benutzer zu einer anderen Anwendung wechselt, Dateien hinzufügt oder entfernt oder anderweitig den verfügbaren Speicherplatz ändert, können Sie die Änderung schnell mithilfe dieses Stils implementieren.

Jedes Dialogfeld, das die [**OutOfDiskSpace-Eigenschaft**](outofdiskspace.md) verwendet, um zu bestimmen, ob ein Dialogfeld geöffnet werden soll, muss das TrackDiskSpace Dialog Style Bit festlegen, damit das Dialogfeld den Speicherplatz auf den Zielvolumes dynamisch aktualisiert.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 



