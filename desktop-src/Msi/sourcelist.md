---
description: Die SOURCELIST-Eigenschaft ist eine durch Semikolons getrennte Liste von Netzwerk- oder URL-Quellpfaden zum Installationspaket der Anwendung.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SOURCELIST-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd0ab879d55481f71c663e4375a305232be576d0c923f67fa419530012d1ce89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893750"
---
# <a name="sourcelist-property"></a>SOURCELIST-Eigenschaft

Die **SOURCELIST-Eigenschaft** ist eine durch Semikolons getrennte Liste von Netzwerk- oder URL-Quellpfaden zum Installationspaket der Anwendung. Diese Liste wird am Ende der vorhandenen Quellliste jedes Benutzers für die Anwendung angefügt. Das Installationsprogramm sucht eine Quelle, indem es die Liste der Quellpfade auflistet und den ersten gefundenen zugänglichen Speicherort verwendet. Nur diese Quelle kann für den Rest der Installation verwendet werden. Jeder in der Quellliste angegebene Pfad muss daher zu einem Speicherort mit einer vollständigen Quelle für die Anwendung sein. Die gesamte Verzeichnisstruktur an jedem Quellspeicherort muss identisch sein und alle erforderlichen Quelldateien enthalten, einschließlich aller Schränke. Jeder Speicherort muss über eine .msi datei mit dem gleichen Dateinamen und Produktcode verfügen.

## <a name="default-value"></a>Standardwert

Das Installationsprogramm überprüft nur die **SOURCELIST-Eigenschaft,** wenn das Produkt noch nicht angekündigt oder installiert wurde. In allen anderen Fällen verwendet das Installationsprogramm die vorhandene Quellliste, die sich in der Registrierung befindet.

## <a name="remarks"></a>Hinweise

Quellen, die mithilfe der **SOURCELIST-Eigenschaft** hinzugefügt werden, werden direkt am Ende der Liste für jeden Quelltyp hinzugefügt und kommen immer nach der von der [**SourceDir-Eigenschaft**](sourcedir.md) angegebenen Standardquelle.

Für Windows Installer ist die Anzahl der Quellen in der **SOURCELIST-Eigenschaft** unbegrenzt. [**MsiSourceListAddSource kann**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) verwendet werden, um Netzwerkquellen hinzuzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Quellresilienz](source-resiliency.md)
</dt> </dl>

 

 




