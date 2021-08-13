---
description: Die ROOTDRIVE-Eigenschaft gibt das Standardlaufwerk für das Zielverzeichnis der Installation an.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: ROOTDRIVE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ca4a3230dde5086b1383f3016da30d99976cf6560d0be994ecb0aaccc0ba6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625737"
---
# <a name="rootdrive-property"></a>ROOTDRIVE-Eigenschaft

Die **ROOTDRIVE-Eigenschaft** gibt das Standardlaufwerk für das Zielverzeichnis der Installation an. Wenn die Directory -Spalte der [Directory-Tabelle](directory-table.md) das Stammzielverzeichnis mit einem nicht definierten Eigenschaftennamen angibt, verwendet das Installationsprogramm den Wert der **ROOTDRIVE-Eigenschaft,** um den Pfad zum Zielverzeichnis aufzulösen.

Wenn **ROOTDRIVE** nicht über die Befehlszeile festgelegt oder in der [Tabelle Property (Eigenschaft)](property-table.md)verfasst wurde, legt das Installationsprogramm diese Eigenschaft fest. Während einer [Administratorinstallation legt](administrative-installation.md) das Installationsprogramm **ROOTDRIVE** auf das erste verbundene Netzwerklaufwerk fest, auf das geschrieben werden kann. Wenn es sich nicht um eine Administratorinstallation handelt oder das Installationsprogramm keine Netzwerklaufwerke finden kann, legt das Installationsprogramm **ROOTDRIVE** auf das lokale Laufwerk fest, auf das der größte freie Speicherplatz geschrieben werden kann.

Der Wert für diese Eigenschaft muss mit ' ' \\ enden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Requirements (Anforderungen für den Windows Installer).<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




