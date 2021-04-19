---
description: Die msifastinstall-Eigenschaft kann verwendet werden, um die Zeit zu verkürzen, die für die Installation eines großen Windows Installer Pakets erforderlich ist.
ms.assetid: 011668da-da04-4b80-989e-192b0daa3060
title: Msifastinstall (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9474e295269fa4a8347210653bed5db772878662
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366732"
---
# <a name="msifastinstall-property"></a>Msifastinstall (Eigenschaft)

Die **msifastinstall** -Eigenschaft kann verwendet werden, um die Zeit zu verkürzen, die für die Installation eines großen Windows Installer Pakets erforderlich ist. Die-Eigenschaft kann in der Befehlszeile oder in der [Eigenschaften](property-table.md) Tabelle festgelegt werden, um Vorgänge zu konfigurieren, die der Benutzer oder Entwickler für die Installation nicht benötigt.

Der Wert der **msifastinstall** -Eigenschaft kann eine Kombination der folgenden Werte sein.



| Wert | Bedeutung                                                                      |
|-------|------------------------------------------------------------------------------|
| 0     | Standardwert                                                                |
| 1     | Für diese Installation wurde kein Systemwiederherstellungspunkt gespeichert.                      |
| 2     | Führen Sie nur die [Datei Kosten](file-costing.md) aus, und überspringen Sie andere Kosten. |
| 4     | Reduzieren Sie die Häufigkeit von Statusmeldungen.                                   |



 

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Eigenschaft ist ab Windows Installer 5,0 verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



 

 




