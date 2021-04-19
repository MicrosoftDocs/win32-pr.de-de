---
description: Die availablefreereg-Eigenschaft gibt in Kilobyte den gesamten freien Speicherplatz an, der in der Registrierung nach dem Aufrufen der Aktion "depjeeregistryspace" verfügbar ist. Der maximale Wert der availablefreereg-Eigenschaft beträgt 2 Millionen Kilobyte. Diese Eigenschaft wird nur unter Windows 2000 festgelegt.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Availablefreereg (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359680"
---
# <a name="availablefreereg-property"></a>Availablefreereg (Eigenschaft)

Die **availablefreereg** -Eigenschaft gibt in Kilobyte den gesamten freien Speicherplatz an, der in der Registrierung nach dem Aufrufen der [Aktion "depjeeregistryspace](allocateregistryspace-action.md)" verfügbar ist.

Der maximale Wert der **availablefreereg** -Eigenschaft beträgt 2 Millionen Kilobyte.

Diese Eigenschaft wird nur unter Windows 2000 festgelegt.

## <a name="remarks"></a>Bemerkungen

Die **availablefreereg** -Eigenschaft muss auf einen Wert festgelegt werden, der groß genug ist, um für alle von der Installation hinzugefügten Registrierungsinformationen ausreichenden Speicherplatz in der Registrierung sicherzustellen. Der Mindestwert, der erforderlich ist, um ausreichend Speicherplatz sicherzustellen, hängt davon ab, wo sich die [Zuweisung "depasseregistryspace](allocateregistryspace-action.md) " in der Aktions Sequenz befindet, da der Installer beim Registrieren von Informationen in den Tabellen [Registry](registry-table.md), [Class](class-table.md), [selfreg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md)und [Verb](verb-table.md) automatisch den Speicherplatz vergrößert. Das Installationsprogramm erhöht den gesamten Registrierungsbereich nicht auf den durch **availablefreereg** angegebenen Betrag, bis "zustellereregistryspace" in der Aktions Sequenz erreicht ist.

Wenn ' zugeregistryspace ' einer der ersten Aktionen in der Aktions Sequenz ist, sollte **availablefreereg** auf den gesamten Speicherplatz festgelegt werden, der für die Registrierungsinformationen in der Registrierungs Tabelle, der Klassen Tabelle, der TypeLib-Tabelle, der selfreg-Tabelle, der Erweiterungs Tabelle, der MIME-Tabelle, der Verb Tabelle, der Registrierung von [benutzerdefinierten Aktionen](custom-actions.md) Der Wert von **availablefreereg** ist die Gesamtmenge der von der Installation hinzugefügten Informationen und stellt in allen Fällen ausreichend Speicherplatz zur Verfügung. Dies ist auch der häufigste Fall.

Wenn die Aktion "zuordnet zuregistrieren" in der Aktions Sequenz nach allen [Standard Aktionen](standard-actions.md) erstellt werden kann, die Registrierungsdaten schreiben, z. b. " [schreiteregistryvalues](writeregistryvalues-action.md) " und " [RegisterClassInfo](registerclassinfo-action.md)", muss der Wert von " **availablefreereg** " nur auf den Speicherplatz festgelegt werden, der zum Registrieren von benutzerdefinierten Aktionen benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




