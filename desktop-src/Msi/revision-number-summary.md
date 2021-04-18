---
description: Bei einem Installationspaket enthält die Zusammenfassungs Eigenschaft Revisionsnummer den Paket Code für das Installer-Paket.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Zusammenfassungs Eigenschaft der Revisionsnummer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361461"
---
# <a name="revision-number-summary-property"></a>Zusammenfassungs Eigenschaft der Revisionsnummer

Bei einem Installationspaket enthält die **Zusammenfassungs Eigenschaft Revisionsnummer** den [*Paket Code*](p-gly.md) für das Installer-Paket. Weitere Informationen zu Paket Codes finden Sie unter [Paket Codes](package-codes.md).

Bei einer Transformation werden in der **Zusammenfassungs Eigenschaft Revisionsnummer** die Produktcode-GUIDs und die Version der neuen und ursprünglichen Produkte sowie die UpgradeCode-GUID aufgelistet. Die Liste wird wie folgt durch Semikolons getrennt.

"Original-Product-Code Original-Product-Version; New-Product Code New-Product-Version; UpgradeCode "

Bei einem Patchpaket gibt die **Zusammenfassungs Eigenschaft der Revisionsnummer** den GUID-Patchcode für den Patch an. Auf diese Weise kann eine Liste von Patchcode-GUIDs für veraltete Patches folgen, die entfernt werden sollen, wenn dieser Patch angewendet wird. Die Patchcodes werden ohne Trennzeichen verkettet, in denen GUIDs in der Liste getrennt sind.

* * Windows Installer 3,0: * * Wenn in der [msipatchsequence-Tabelle](msipatchsequence-table.md)Sequenzierungs Informationen vorhanden sind, verwendet Windows Installer 3,0 die Sequenzierungs Informationen in der Tabelle und ignoriert die Liste veralteter Patches, die in der **Revisionsnummer-Zusammenfassungs** Eigenschaft enthalten sind. In Windows Installer 3,0 können weiterhin die veralteten Patchinformationen in der **Revisionsnummer-Zusammenfassungs** Eigenschaft verwendet werden, wenn das Paket keine msipatchsequence-Tabelle enthält.

* * Windows Installer 2,0: * * die [msipatchsequence-Tabelle](msipatchsequence-table.md) wird nicht unterstützt. In Windows Installer 2,0 können weiterhin die veralteten Patchinformationen in der **Revisionsnummer-Zusammenfassungs** Eigenschaft verwendet werden, wenn das Paket keine msipatchsequence-Tabelle enthält.

Diese Zusammenfassungs Eigenschaft ist erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beschreibungen der Zusammenfassungs Eigenschaften](summary-property-descriptions.md)
</dt> </dl>

 

 




