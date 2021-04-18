---
description: Der Wert der Eigenschaft fileadddefault ist eine Liste von Datei Schlüsseln, die durch Kommas getrennt sind, die in der Standardkonfiguration installiert sind.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: File adddefault (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357934"
---
# <a name="fileadddefault-property"></a>File adddefault (Eigenschaft)

Der Wert der Eigenschaft **fileadddefault** ist eine Liste von Datei Schlüsseln, die durch Kommas getrennt sind, die in der Standardkonfiguration installiert sind. Für jeden Datei Schlüssel in der Liste bestimmt das Installationsprogramm die Komponente, die diese Datei steuert, und installiert die Funktion, die den geringsten Speicherplatz benötigt. Die Datei Schlüssel in der Liste müssen in der Datei Spalte der [Datei](file-table.md) Tabelle vorhanden sein. Eine Funktion wird in demselben Installationsstatus installiert, als ob der Benutzer eine Installation bei Bedarf der Funktion angefordert hätte. Der Status wird durch die Bits festgelegt, die für die Funktion in der Spalte Attribute der [Funktions Tabelle](feature-table.md)festgelegt sind, und welche Bits für die Komponenten der Funktion in der Spalte Attribute der Komponenten [Tabelle](component-table.md)festgelegt werden.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die Datei Schlüsselnamen die Groß-/Kleinschreibung beachten. Beachten Sie auch Folgendes: Wenn das sourceOnly-Bitflag in der Attribute-Spalte der [Komponenten](component-table.md) Tabelle für eine Komponente festgelegt ist, wird die Komponente installiert, um von der Quelle ausgeführt zu werden.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Aufgeh**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**Adddefault**](adddefault.md)
5.  [**Installieren Sie**](reinstall.md)
6.  [**Benen**](advertise.md)
7.  [**Compaddlocal**](compaddlocal.md)
8.  [**Compaddsource**](compaddsource.md)
9.  [**Compadddefault**](compadddefault.md)
10. [**Fileaddlocal**](fileaddlocal.md)
11. [**Fileaddsource**](fileaddsource.md)
12. **Fileadddefault**

Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt. Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.

Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




