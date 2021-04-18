---
description: Die ROOTDRIVE-Eigenschaft gibt das Standard Laufwerk für das Zielverzeichnis der Installation an.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: ROOTDRIVE (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372308"
---
# <a name="rootdrive-property"></a>ROOTDRIVE (Eigenschaft)

Die **ROOTDRIVE** -Eigenschaft gibt das Standard Laufwerk für das Zielverzeichnis der Installation an. Wenn in der Verzeichnis-Spalte der [Verzeichnis Tabelle](directory-table.md) das Stammverzeichnis durch einen nicht definierten Eigenschaftsnamen angegeben ist, verwendet das Installationsprogramm den Wert der **ROOTDRIVE** -Eigenschaft, um den Pfad zum Zielverzeichnis aufzulösen.

Wenn **ROOTDRIVE** nicht in einer Befehlszeile festgelegt oder in der [Eigenschaften Tabelle](property-table.md)erstellt wurde, legt das Installationsprogramm diese Eigenschaft fest. Während einer [administrativen Installation](administrative-installation.md) legt das Installationsprogramm **ROOTDRIVE** auf das erste gefundene Netzwerklaufwerk fest, in das geschrieben werden kann. Wenn es sich nicht um eine administrative Installation handelt, oder wenn das Installationsprogramm keine Netzwerklaufwerke finden kann, legt das Installationsprogramm **ROOTDRIVE** auf das lokale Laufwerk fest, das mit dem meisten freien Speicherplatz geschrieben werden kann.

Der Wert für diese Eigenschaft muss auf " \\ " enden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




