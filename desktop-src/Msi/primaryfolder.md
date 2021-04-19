---
description: Der Ordner "PRIMARYFOLDER" ist eine globale Eigenschaft, die dem Autor das Festlegen eines primären Ordners für die Installation ermöglicht.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: PRIMARYFOLDER (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359290"
---
# <a name="primaryfolder-property"></a>PRIMARYFOLDER (Eigenschaft)

Der **Ordner "PRIMARYFOLDER** " ist eine globale Eigenschaft, die dem Autor das Festlegen eines primären Ordners für die Installation ermöglicht. Der Wert für diese Eigenschaft muss der Schlüssel Name eines Verzeichnisses sein, das in der [Verzeichnis Tabelle](directory-table.md)vorhanden ist.

Das Installationsprogramm verwendet den aufgelösten Pfad des primären Ordners, um zu bestimmen, welches Volume beim Festlegen der Werte der Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) , der Eigenschaft [**primaryvolumespaceavailable**](primaryvolumespaceavailable.md) , der Eigenschaft [**primaryvolumespacerequired**](primaryvolumespacerequired.md) und der Eigenschaft [**primaryvolumespaceremainte**](primaryvolumespaceremaining.md) verwendet werden soll. Das Installationsprogramm stellt den Benutzern in der Benutzeroberfläche die Werte dieser letzteren Eigenschaften zur Verfügung, um Sie bei der Verwaltung des Speicherplatzes zu unterstützen. Häufig können Paket Autoren den größten Ordner als primären Ordner auswählen.

Der Wert für diese Eigenschaft muss der Schlüssel Name eines Verzeichnis Datensatzes sein, der in der [Verzeichnis Tabelle](directory-table.md)gefunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




