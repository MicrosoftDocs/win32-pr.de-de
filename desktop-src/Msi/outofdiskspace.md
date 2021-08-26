---
description: Das Installationsprogramm legt die OutOfDiskSpace-Eigenschaft auf TRUE fest, wenn ein Volume, das ein Ziel der aktuellen Installation ist, nicht über genügend Speicherplatz für die Installation verfügt.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: OutOfDiskSpace (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a99146d08722038bbc2d9b1e0d7b32fd8b587126b0fc942e14823909a2aef79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042580"
---
# <a name="outofdiskspace-property"></a>OutOfDiskSpace (Eigenschaft)

Das Installationsprogramm legt die **OutOfDiskSpace-Eigenschaft** auf TRUE fest, wenn ein Volume, das ein Ziel der aktuellen Installation ist, nicht über genügend Speicherplatz für die Installation verfügt. Wenn alle Volumes über ausreichend Speicherplatz verfügen, ist der Wert FALSE. Auswahlauflösungsaktionen verwenden diesen Wert, um eine Installation abzubricht und ein Dialogfeld zu generieren.

Diese Eigenschaft ist jederzeit gültig, nachdem die [Aktion CostFinalize](costfinalize-action.md) ausgeführt wurde. Der [**OutOfNoRbDiskSpace-Eigenschaftsstatus**](outofnorbdiskspace.md) wird jedes Mal dynamisch aktualisiert, wenn die Gesamtkosten für die Installation neu berechnet werden (z. B. jedes Mal, wenn der Installationsstatus eines Features über das Dialogfeld Auswahl geändert [wird).](selection-dialog.md)

## <a name="remarks"></a>Hinweise

Jeder Dialog, der die **OutOfDiskSpace-Eigenschaft** verwendet, um zu bestimmen, ob ein Dialog geöffnet werden soll, muss das [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) festlegen, damit das Dialogfeld den Speicherplatz auf den Zielvolumes dynamisch aktualisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




