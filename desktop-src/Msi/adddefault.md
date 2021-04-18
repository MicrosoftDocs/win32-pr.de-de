---
description: Der Wert der Eigenschaft adddefault ist eine Liste von Funktionen, die durch Kommas getrennt sind und in der Standardkonfiguration installiert werden sollen.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Adddefault (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372294"
---
# <a name="adddefault-property"></a>Adddefault (Eigenschaft)

Der Wert der Eigenschaft **adddefault** ist eine Liste von Funktionen, die durch Kommas getrennt sind und in der Standardkonfiguration installiert werden sollen. Die Funktionen müssen in der featurespalte der [Funktions Tabelle](feature-table.md) vorhanden sein. Verwenden Sie zum Installieren aller Features in ihren Standardkonfigurationen adddefault = all in der Befehlszeile.

Eine Funktion, die in der Eigenschaft **adddefault** aufgeführt ist, wird in demselben Installationsstatus installiert, als ob der Benutzer eine Installation bei Bedarf des Features angefordert hat. Der Status wird durch die Bits bestimmt, die für die Funktion in der Spalte Attribute der [Featuretabelle](feature-table.md)festgelegt sind, und welche Bits für die Featurekomponenten in der Spalte Attribute der [Komponenten Tabelle](component-table.md)festgelegt werden.

## <a name="remarks"></a>Bemerkungen

Bei den Funktionsnamen wird Groß-/Kleinschreibung beachtet.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Aufgeh**](remove.md)
3.  [**Addsource**](addsource.md)
4.  **Adddefault**
5.  [**Installieren Sie**](reinstall.md)
6.  [**Benen**](advertise.md)
7.  [**Compaddlocal**](compaddlocal.md)
8.  [**Compaddsource**](compaddsource.md)
9.  [**Compadddefault**](compadddefault.md)
10. [**Fileaddlocal**](fileaddlocal.md)
11. [**Fileaddsource**](fileaddsource.md)
12. [**Fileadddefault**](fileadddefault.md)

Beispiel:

-   Wenn in der Befehlszeile Folgendes angegeben wird: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und **myfeature** wird auf Run-From-Source festgelegt.
-   Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First **myfeature** " auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich " **myfeature**") auf "Run-From-Source" zurückgesetzt.

Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




