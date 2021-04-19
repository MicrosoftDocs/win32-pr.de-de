---
description: Der Wert der compaddsource-Eigenschaft ist eine Liste von Komponenten-GUIDs aus der Spalte "ComponentId" der Komponenten Tabelle, die durch Kommas getrennt sind, die zur Installation vom Quell Medium installiert werden sollen.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: Compaddsource (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356419"
---
# <a name="compaddsource-property"></a>Compaddsource (Eigenschaft)

Der Wert der **compaddsource** -Eigenschaft ist eine Liste von Komponenten-GUIDs aus der Spalte "ComponentId" der [Komponenten](component-table.md) Tabelle, die durch Kommas getrennt sind, die zur Installation vom Quell Medium installiert werden sollen. Das Installationsprogramm verwendet diesen Wert, um zu bestimmen, welche Funktionen auf der Grundlage der angegebenen Komponenten zum Ausführen aus der Quelle installiert werden. Für jede aufgelistete Komponenten-ID überprüft das Installationsprogramm alle Features, die (über die Tabelle " [FeatureComponents](featurecomponents-table.md) ") mit dieser Komponente verknüpft sind, und installiert die Funktion, die den geringsten Speicherplatz für die Installation erfordert. Die aufgeführten Komponenten müssen in der Component-Spalte der [Component](component-table.md) -Tabelle vorhanden sein.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass bei den Komponentennamen die Groß-/Kleinschreibung beachtet Beachten Sie auch Folgendes: Wenn das LocalOnly-Bitflag in der Attribute-Spalte der [Komponenten](component-table.md) Tabelle für eine Komponente festgelegt ist, wird die Komponente zur lokalen Installation installiert.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Aufgeh**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**Adddefault**](adddefault.md)
5.  [**Installieren Sie**](reinstall.md)
6.  [**Benen**](advertise.md)
7.  [**Compaddlocal**](compaddlocal.md)
8.  **Compaddsource**
9.  [**Compadddefault**](compadddefault.md)
10. [**Fileaddlocal**](fileaddlocal.md)
11. [**Fileaddsource**](fileaddsource.md)
12. [**Fileadddefault**](fileadddefault.md)

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

 

 




