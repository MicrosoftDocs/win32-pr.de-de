---
description: Für ein Installationspaket enthält die Revision Number Summary -Eigenschaft den Paketcode für das Installationspaket.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Revision Number Summary -Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11371c4a431322fd7ceca7fd645fc8eb8bea47688b740340e973507271f6a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869060"
---
# <a name="revision-number-summary-property"></a>Revision Number Summary -Eigenschaft

Für ein Installationspaket enthält die Revision **Number Summary** -Eigenschaft den [*Paketcode*](p-gly.md) für das Installationspaket. Weitere Informationen zu Paketcodes finden Sie unter [Paketcodes.](package-codes.md)

Für eine Transformation listet die Revision **Number Summary** -Eigenschaft die Produktcode-GUIDs und die Version der neuen und ursprünglichen Produkte sowie die Upgradecode-GUID auf. Die Liste ist wie folgt durch Semikolons getrennt.

"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"

Für ein Patchpaket gibt die **Revision Number Summary** -Eigenschaft den GUID-Patchcode für den Patch an. Darauf kann eine Liste der Patchcode-GUIDs für veraltete Patches folgen, die entfernt werden sollen, wenn dieser Patch angewendet wird. Die Patchcodes werden ohne Trennzeichen verkettet, die GUIDs in der Liste trennen.

**Windows Installer 3.0: ** Wenn sequenzierungsinformationen in der [MsiPatchSequence-Tabelle](msipatchsequence-table.md)vorhanden sind, verwendet Windows Installer 3.0 die Sequenzierungsinformationen in der Tabelle und ignoriert die Liste veralteter Patches, die in der Revision **Number Summary** -Eigenschaft enthalten sind. Windows Installer 3.0 kann weiterhin die veralteten Patchinformationen in der **Revision Number Summary** -Eigenschaft verwenden, wenn das Paket keine MsiPatchSequence-Tabelle enthält.

**Windows Installer 2.0: ** Die [Tabelle MsiPatchSequence](msipatchsequence-table.md) wird nicht unterstützt. Windows Installer 2.0 kann weiterhin die veralteten Patchinformationen in der **Revision Number Summary** -Eigenschaft verwenden, wenn das Paket keine MsiPatchSequence-Tabelle enthält.

Diese Zusammenfassungseigenschaft ist erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zusammenfassungseigenschaftenbeschreibungen](summary-property-descriptions.md)
</dt> </dl>

 

 




