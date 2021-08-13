---
description: Die INSTALLLEVEL-Eigenschaft ist die anfängliche Ebene, auf der Features &\# 0034;ON&0034; für die Installation standardmäßig \# ausgewählt werden.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: INSTALLLEVEL-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e349e8d92a2c480866b04a1ca57885ffa1cdb230d8346b357318fa239ead72a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629959"
---
# <a name="installlevel-property"></a>INSTALLLEVEL-Eigenschaft

Die **INSTALLLEVEL-Eigenschaft** ist die anfängliche Ebene, auf der Features standardmäßig für die Installation "ON" ausgewählt werden. Ein Feature wird nur installiert, wenn der Wert im Feld Ebene der [Tabelle Feature](feature-table.md) kleiner oder gleich dem aktuellen INSTALLLEVEL-Wert ist. Die Installationsebene für jede Installation wird von der **INSTALLLEVEL-Eigenschaft** angegeben und kann ein ganzzahlig von 1 bis 32.767 sein. Weitere Informationen zu Den Installationsebenen finden Sie in [der Featuretabelle](feature-table.md).

## <a name="default-value"></a>Standardwert

Wenn kein Wert angegeben wird, wird die Installationsebene standardmäßig auf 1 festgelegt.

## <a name="remarks"></a>Hinweise

Die von der **INSTALLLEVEL-Eigenschaft angegebene Installationsebene** kann durch die folgenden Eigenschaften überschrieben werden:

-   [**ADDLOCAL**](addlocal.md)
-   [**ADDSOURCE**](addsource.md)
-   [**ADDDEFAULT**](adddefault.md)
-   [**COMPADDLOCAL**](compaddlocal.md)
-   [**COMPADDSOURCE**](compaddsource.md)
-   [**FILEADDLOCAL**](fileaddlocal.md)
-   [**FILEADDSOURCE**](fileaddsource.md)
-   [**Entfernen**](remove.md)
-   [**Installieren**](reinstall.md)
-   [**Werben**](advertise.md)

Wenn Sie beispielsweise ADDLOCAL=ALL festlegen, werden alle Features lokal installiert, unabhängig vom Wert der **INSTALLLEVEL-Eigenschaft.** Wenn der Wert der Spalte Ebene in der [Featuretabelle](feature-table.md) 0 ist, wird dieses Feature nicht installiert und nicht auf der Benutzeroberfläche angezeigt.

Ein Administrator kann ein Feature dauerhaft deaktivieren, indem er eine Anpassungstransformation anwenden, die in der Spalte Ebene für dieses Feature einen Wert von 0 (0) festgelegt. Die Anwendung der Anpassungstransformation verhindert die Installation und Anzeige des Features, selbst wenn der Benutzer über die Benutzeroberfläche oder durch Festlegen von ADDLOCAL auf ALL in der Befehlszeile eine vollständige Installation auswählt. Weitere Informationen finden [Sie unter Beispiel für eine Anpassungstransformation.](a-customization-transform-example.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Requirements (Anforderungen für den Windows Installer).<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




