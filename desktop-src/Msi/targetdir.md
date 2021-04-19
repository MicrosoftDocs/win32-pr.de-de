---
description: Die TARGETDIR-Eigenschaft gibt das Stammverzeichnis für die Installation an.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368626"
---
# <a name="targetdir-property"></a>TARGETDIR-Eigenschaft

Die **TARGETDIR** -Eigenschaft gibt das Stammverzeichnis für die Installation an. **TARGETDIR** muss der Name eines Stamms in der [Verzeichnis](directory-table.md) Tabelle sein. Möglicherweise gibt es nur ein einzelnes Stammverzeichnis. Bei einer [administrativen Installation](administrative-installation.md) gibt diese Eigenschaft den Speicherort für das Kopieren des Installationspakets an. Bei einer nicht administrativen Installation gibt diese Eigenschaft das Stammverzeichnis für das Ziel an.

Zum Angeben des Stammverzeichnis Verzeichnisses legen Sie die Verzeichnis Spalte der Verzeichnis Tabelle auf die **TARGETDIR** -Eigenschaft und die DefaultDir-Spalte auf die [**SourceDir**](sourcedir.md) -Eigenschaft fest. Wenn die Eigenschaft **TARGETDIR** definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst. Wenn die **TARGETDIR** -Eigenschaft nicht definiert ist, wird der Pfad mithilfe der [**ROOTDRIVE**](rootdrive.md) -Eigenschaft aufgelöst. Weitere Informationen zur Verwendung der **TARGETDIR** -Eigenschaft finden Sie unter [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md).

Beachten Sie, dass der Wert der **TARGETDIR** -Eigenschaft in der Regel in der Befehlszeile oder über eine Benutzeroberfläche festgelegt wird. Es wird nicht empfohlen, **TARGETDIR** durch das Erstellen eines Pfads in die [Eigenschaften Tabelle](property-table.md) festzulegen, da die Computer sich in der Einrichtung des lokalen Laufwerks unterscheiden.

Weitere Informationen zum Ändern von TARGETDIR während einer Installation finden Sie unter [Ändern des Zielspeicher Orts für ein Verzeichnis](changing-the-target-location-for-a-directory.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




