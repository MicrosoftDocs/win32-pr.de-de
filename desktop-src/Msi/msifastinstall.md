---
description: Die MSIFASTINSTALL-Eigenschaft kann verwendet werden, um den Zeitaufwand für die Installation eines großen Windows Installer-Pakets zu reduzieren.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: MSIFASTINSTALL-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28c731d34e769f0612acc12586349247231bce663036d3577f41df6a7256f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628503"
---
# <a name="msifastinstall-property"></a>MSIFASTINSTALL-Eigenschaft

Die **MSIFASTINSTALL-Eigenschaft** kann verwendet werden, um den Zeitaufwand für die Installation eines großen Windows Installer-Pakets zu reduzieren. Die -Eigenschaft kann in der Befehlszeile oder in der [Tabelle Eigenschaft](property-table.md) festgelegt werden, um Vorgänge zu konfigurieren, die der Benutzer oder Entwickler als nicht wichtig für die Installation festlegt.

Der Wert der **MSIFASTINSTALL-Eigenschaft** kann eine Kombination der folgenden Werte sein.



| Wert | Bedeutung                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Standardwert                                                                |
| 1     | Für diese Installation wird kein Systemwiederherstellungspunkt gespeichert.                      |
| 2     | Führen Sie nur [Dateikosten aus,](file-costing.md) und überspringen Sie die Überprüfung anderer Kosten. |
| 4     | Reduzieren Sie die Häufigkeit von Statusmeldungen.                                   |



 

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Wird nicht unterstützt. Diese Eigenschaft ist ab Windows Installer 5.0 verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



 

 




