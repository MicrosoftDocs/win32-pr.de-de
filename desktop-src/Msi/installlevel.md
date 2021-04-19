---
description: Die INSTALLLEVEL-Eigenschaft ist die Anfangsstufe, bei der die Features &\# 0034; auf&\# 0034; standardmäßig für die Installation ausgewählt werden.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: INSTALLLEVEL-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354185"
---
# <a name="installlevel-property"></a>INSTALLLEVEL-Eigenschaft

Die **INSTALLLEVEL** -Eigenschaft ist die Anfangsstufe, bei der die Features standardmäßig für die Installation ausgewählt werden. Eine Funktion wird nur installiert, wenn der Wert im Ebenenfeld der [Funktions Tabelle](feature-table.md) kleiner oder gleich dem aktuellen INSTALLLEVEL-Wert ist. Die Installations Ebene für jede Installation wird durch die **INSTALLLEVEL** -Eigenschaft angegeben und kann eine Ganzzahl zwischen 1 und 32.767 sein. Weitere Informationen zu Installations Ebenen finden Sie unter [Feature Table](feature-table.md).

## <a name="default-value"></a>Standardwert

Wenn kein Wert angegeben wird, wird für die Installations Ebene der Standardwert 1 verwendet.

## <a name="remarks"></a>Bemerkungen

Die von der **INSTALLLEVEL** -Eigenschaft angegebene Installations Ebene kann durch die folgenden Eigenschaften überschrieben werden:

-   [**ADDLOCAL**](addlocal.md)
-   [**Addsource**](addsource.md)
-   [**Adddefault**](adddefault.md)
-   [**Compaddlocal**](compaddlocal.md)
-   [**Compaddsource**](compaddsource.md)
-   [**Fileaddlocal**](fileaddlocal.md)
-   [**Fileaddsource**](fileaddsource.md)
-   [**Aufgeh**](remove.md)
-   [**Installieren Sie**](reinstall.md)
-   [**Benen**](advertise.md)

Wenn Sie z. b. "ADDLOCAL = ALL" festlegen, werden alle Features unabhängig vom Wert der Eigenschaft " **INSTALLLEVEL** " lokal installiert. Wenn der Wert der Spalte Ebene in der [Featuretabelle](feature-table.md) auf 0 festgelegt ist, ist das Feature nicht installiert und wird nicht auf der Benutzeroberfläche angezeigt.

Ein Administrator kann eine Funktion dauerhaft deaktivieren, indem er eine Anpassungs Transformation anwendet, die in der Spalte Ebene für diese Funktion 0 (null) festlegt. Die Anwendung der Anpassungs Transformation verhindert die Installation und Anzeige des Features, auch wenn der Benutzer eine vollständige Installation mithilfe der Benutzeroberfläche auswählt oder ADDLOCAL in der Befehlszeile auf alle festgelegt hat. [Ein Beispiel für eine Anpassungs Transformation](a-customization-transform-example.md)finden Sie hier.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




