---
description: Die adminproperties-Eigenschaft sollte in der Eigenschaften Tabelle erstellt werden.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Adminproperties (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372760"
---
# <a name="adminproperties-property"></a>Adminproperties (Eigenschaft)

Die **adminproperties** -Eigenschaft sollte in der Eigenschaften [Tabelle](property-table.md)erstellt werden. Der Wert von " **adminproperties** " ist eine Liste von Eigenschaftsnamen, die durch Semikolons getrennt sind. Der Installer speichert die Werte dieser aufgelisteten Eigenschaften zum Zeitpunkt einer [administrativen Installation](administrative-installation.md). Wenn Benutzer über das administrative Image installieren, werden bei der Installation die gespeicherten Werte der Eigenschaften anstelle der Werte in der MSI-Datei verwendet.

## <a name="remarks"></a>Bemerkungen

Bei den Eigenschaften Namen in der Liste kann es sich um groß-und Kleinbuchstaben (private Eigenschaften) oder alle Großbuchstaben (öffentliche Eigenschaften) handeln.

Diese Eigenschaft darf niemals mit einem Semikolon enden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




