---
description: Die SourceList-Eigenschaft ist eine durch Semikolons getrennte Liste der Netzwerk-oder URL-Quell Pfade zum Installationspaket der Anwendung.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SourceList-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359228"
---
# <a name="sourcelist-property"></a>SourceList-Eigenschaft

Die **SourceList** -Eigenschaft ist eine durch Semikolons getrennte Liste der Netzwerk-oder URL-Quell Pfade zum Installationspaket der Anwendung. Diese Liste wird an das Ende der vorhandenen Quell Liste der einzelnen Benutzer für die Anwendung angehängt. Der Installer sucht eine Quelle, indem er die Liste der Quell Pfade auflistet und den ersten zugänglichen Speicherort verwendet, den er findet. Nur diese Quelle kann für den Rest der Installation verwendet werden. Jeder in der Quell Liste angegebene Pfad muss sich daher an einem Speicherort befinden, der über eine komplette Quelle für die Anwendung verfügt. Die gesamte Verzeichnisstruktur an jedem Quell Speicherort muss identisch sein, und Sie muss alle erforderlichen Quelldateien einschließlich aller Schränke enthalten. Jeder Speicherort muss über eine MSI-Datei mit demselben Dateinamen und Produktcode verfügen.

## <a name="default-value"></a>Standardwert

Das Installationsprogramm überprüft nur die **SourceList** -Eigenschaft, wenn das Produkt nicht bereits angekündigt oder installiert wurde. In allen anderen Fällen verwendet das Installationsprogramm die vorhandene Quell Liste in der Registrierung.

## <a name="remarks"></a>Bemerkungen

Quellen, die mithilfe der **SourceList** -Eigenschaft hinzugefügt werden, werden für jeden Quelltyp direkt am Ende der Liste hinzugefügt und sind immer nach der Standard Quelle, die von der [**SourceDir**](sourcedir.md) -Eigenschaft angegeben wird.

Bei Windows Installer die Anzahl der Quellen in der **SourceList** -Eigenschaft unbegrenzt sein. [**Msisourcelistaddsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) kann zum Hinzufügen von Netzwerk Quellen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> </dl>

 

 




