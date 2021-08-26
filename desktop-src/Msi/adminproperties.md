---
description: AdminProperties sollte in der Eigenschaftentabelle erstellt werden.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: AdminProperties-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f59d2452e244bd22110ab918dff61279bf9d27f3c8735f37474aea894d0d02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078130"
---
# <a name="adminproperties-property"></a>AdminProperties-Eigenschaft

Die **AdminProperties** sollten in der [Eigenschaftentabelle](property-table.md)erstellt werden. Der Wert von **AdminProperties** ist eine Liste von Eigenschaftennamen, die durch Semikolons getrennt sind. Das Installationsprogramm speichert die Werte dieser aufgelisteten Eigenschaften zum Zeitpunkt einer [Administratorinstallation.](administrative-installation.md) Wenn Benutzer über das Administratorimage installieren, werden bei der Installation die gespeicherten Werte der Eigenschaften anstelle der Werte in der .msi-Datei verwendet.

## <a name="remarks"></a>Hinweise

Die Eigenschaftennamen in der Liste können Groß- und Kleinbuchstaben (private Eigenschaften) oder alle Großbuchstaben (öffentliche Eigenschaften) sein.

Diese Eigenschaft darf nie mit einem Semikolon enden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




