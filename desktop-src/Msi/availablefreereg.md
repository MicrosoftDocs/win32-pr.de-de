---
description: Die AVAILABLEFREEREG-Eigenschaft gibt den gesamten freien Speicherplatz in kilobytes an, der in der Registrierung nach dem Aufruf der Aktion AllocateRegistrySpace verfügbar ist. Der Höchstwert der AVAILABLEFREEREG-Eigenschaft beträgt 200.000 KB. Diese Eigenschaft wird nur auf Windows 2000 festgelegt.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: AVAILABLEFREEREG-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45508494f9ba87ec8261b38ea18f83d0b3ad9796f7390b70349211cbf244df3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650070"
---
# <a name="availablefreereg-property"></a>AVAILABLEFREEREG-Eigenschaft

Die **AVAILABLEFREEREG-Eigenschaft** gibt den gesamten freien Speicherplatz in kilobytes an, der in der Registrierung nach dem Aufruf der [Aktion AllocateRegistrySpace verfügbar ist.](allocateregistryspace-action.md)

Der Höchstwert der **AVAILABLEFREEREG-Eigenschaft** beträgt 200.000 KB.

Diese Eigenschaft wird nur auf Windows 2000 festgelegt.

## <a name="remarks"></a>Hinweise

Die **AVAILABLEFREEREG-Eigenschaft** muss auf einen Wert festgelegt werden, der groß genug ist, um sicherzustellen, dass in der Registrierung genügend Speicherplatz für alle Registrierungsinformationen vorhanden ist, die von der Installation hinzugefügt werden. Der Mindestwert, der erforderlich ist, um ausreichend Speicherplatz sicherzustellen, hängt davon ab, wo sich die [Aktion AllocateRegistrySpace](allocateregistryspace-action.md) in der Aktionssequenz befindet, da das Installationsprogramm den Speicherplatz bei Bedarf automatisch vergrößert, wenn Informationen in den Tabellen [Registrierung,](registry-table.md) [Klasse,](class-table.md) [SelfReg,](selfreg-table.md) [Erweiterung,](extension-table.md) [MIME](mime-table.md)und [Verb](verb-table.md) registriert werden. Das Installationsprogramm erhöht den gesamten Registrierungsspeicherplatz erst auf den von **AVAILABLEFREEREG** angegebenen Wert, wenn allocateRegistrySpace in der Aktionssequenz erreicht wurde.

Wenn AllocateRegistrySpace eine der ersten Aktionen in der Aktionssequenz ist, sollte **AVAILABLEFREEREG** auf den Gesamtspeicherplatz festgelegt werden, der von den Registrierungsinformationen in [](custom-actions.md) der Registrierungstabelle, der Klassentabelle, der TypeLib-Tabelle, der SelfReg-Tabelle, der Erweiterungstabelle, der MIME-Tabelle, der Verbtabelle, der Registrierung benutzerdefinierter Aktionen, der Selbstregistrierung und allen anderen Registrierungsinformationen benötigt wird, die während der Installation geschrieben wurden. Der Wert von **AVAILABLEFREEREG** ist die Gesamtmenge der von der Installation hinzugefügten Informationen und stellt in allen Fällen ausreichend Speicherplatz sicher. Dies ist auch der häufigste Fall.

Wenn die Aktion AllocateRegistrySpace in der Aktionssequenz nach allen Standardaktionen erstellt werden kann, die Registrierungsdaten schreiben, z. B. [WriteRegistryValues](writeregistryvalues-action.md) und [RegisterClassInfo,](registerclassinfo-action.md)muss der Wert von **AVAILABLEFREEREG** nur auf den Speicherplatz festgelegt werden, der zum Registrieren von benutzerdefinierten Aktionen, Registrieren von Typbibliotheken und anderen Informationen erforderlich ist, die noch nicht über die Tabellen registriert wurden. [](standard-actions.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




