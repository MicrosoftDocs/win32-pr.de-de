---
description: Der Installer legt die windowsvolume-Eigenschaft auf das Volume des Windows-Ordners fest.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Windowsvolume-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371137"
---
# <a name="windowsvolume-property"></a>Windowsvolume-Eigenschaft

Der Installer legt die **windowsvolume** -Eigenschaft auf das Volume des Windows-Ordners fest. Die-Eigenschaft endet immer mit einem umgekehrten Schrägstrich. Dies kann verwendet werden, um den Standard Speicherort auf das Volume festzulegen, auf dem sich der Windows-Ordner befindet, da die [**ROOTDRIVE**](rootdrive.md) -Eigenschaft nicht notwendigerweise mit diesem Laufwerk identisch ist.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **windowsvolume** -Eigenschaft nicht in der Verzeichnis-Spalte der [Verzeichnis](directory-table.md) Tabelle. Die [**windowsfolder**](windowsfolder.md) -Eigenschaft enthält den Pfad zum Windows-Ordner.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




