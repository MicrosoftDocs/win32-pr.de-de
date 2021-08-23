---
description: Die TARGETDIR-Eigenschaft gibt das Stammzielverzeichnis für die Installation an.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b61575de21b47b1d82764d96e5876a9fd4c89fb1f837150988aa2c7a08e07be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626600"
---
# <a name="targetdir-property"></a>TARGETDIR(Eigenschaft)

Die **TARGETDIR-Eigenschaft** gibt das Stammzielverzeichnis für die Installation an. **TARGETDIR** muss der Name eines Stamms in der [Directory-Tabelle](directory-table.md) sein. Möglicherweise gibt es nur ein einzelnes Stammzielverzeichnis. Während einer [Administratorinstallation](administrative-installation.md) gibt diese Eigenschaft den Speicherort zum Kopieren des Installationspakets an. Während einer Installation ohne Administratorrechte gibt diese Eigenschaft das Stammzielverzeichnis an.

Um das Stammzielverzeichnis anzugeben, legen Sie die Directory -Spalte der Directory-Tabelle auf die **TARGETDIR-Eigenschaft** und die DefaultDir -Spalte auf die [**SourceDir-Eigenschaft**](sourcedir.md) fest. Wenn die **TARGETDIR-Eigenschaft** definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst. Wenn die **TARGETDIR-Eigenschaft** nicht definiert ist, wird die [**ROOTDRIVE-Eigenschaft**](rootdrive.md) verwendet, um den Pfad aufzulösen. Weitere Informationen zur Verwendung der **TARGETDIR-Eigenschaft** finden Sie unter [Verwenden der Verzeichnistabelle](using-the-directory-table.md).

Beachten Sie, dass der Wert der **TARGETDIR-Eigenschaft** in der Regel über die Befehlszeile oder über eine Benutzeroberfläche festgelegt wird. Das **Festlegen von TARGETDIR** durch Erstellen eines Pfads in der [Tabelle Eigenschaft](property-table.md) wird nicht empfohlen, da computer sich in der Einrichtung des lokalen Laufwerks unterscheiden.

Weitere Informationen zum Ändern von TARGETDIR während einer Installation finden Sie unter [Ändern des Zielspeicherorts für ein Verzeichnis.](changing-the-target-location-for-a-directory.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




