---
description: Der Wert der COMPADDLOCAL-Eigenschaft ist eine Liste von Komponenten-GUIDs aus der ComponentId-Spalte der Component-Tabelle, die durch Kommas getrennt sind und lokal installiert werden sollen.
ms.assetid: 10c178c5-1eae-4191-b79c-9285810efb6a
title: COMPADDLOCAL-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c442ede6e8affaaddef1dc028a8a6fffc5b780afd536bbc3eaa52e6949df8fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145143"
---
# <a name="compaddlocal-property"></a>COMPADDLOCAL-Eigenschaft

Der Wert der **COMPADDLOCAL-Eigenschaft** ist eine Liste von Komponenten-GUIDs aus der ComponentId-Spalte der [Component-Tabelle,](component-table.md)die durch Kommas getrennt ist und lokal installiert werden soll. Das Installationsprogramm verwendet diese Liste, um basierend auf den angegebenen Komponenten zu bestimmen, welche Features lokal installiert werden sollen. Für jede aufgelistete Komponenten-ID überprüft das Installationsprogramm alle Features, die über die [Tabelle FeatureComponents](featurecomponents-table.md) mit dieser Komponente verknüpft sind, und installiert das Feature, für das die Installation des geringsten Speicherplatzes erforderlich ist. Die aufgeführten Komponenten müssen in der Spalte Komponente der [Tabelle Komponente](component-table.md) vorhanden sein.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass bei den Komponentennamen die Groß-/Kleinschreibung beachtet wird. Beachten Sie außerdem Folgendes: Wenn das SourceOnly-Bitflag in der Spalte Attribute der [Komponententabelle](component-table.md) für eine Komponente festgelegt ist, wird die Komponente installiert, um von der Quelle aus ausgeführt zu werden.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Entfernen**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Installieren**](reinstall.md)
6.  [**Werben**](advertise.md)
7.  **COMPADDLOCAL**
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Wenn die Befehlszeile beispielsweise FOLGENDEs angibt: ADDLOCAL=ALL, ADDSOURCE = MyFeature, werden alle Features zuerst auf "run-local" und dann auf "MyFeature" auf "run-from-source" festgelegt. Wenn die Befehlszeile lautet: ADDSOURCE=ALL, ADDLOCAL=MyFeature, wird zuerst MyFeature auf run-local festgelegt, und wenn ADDSOURCE=ALL ausgewertet wird, werden alle Features (einschließlich MyFeature) auf run-from-source zurückgesetzt.

Das Installationsprogramm legt die [**Preselected-Eigenschaft**](preselected.md) während der Wiederaufnahme einer angehaltenen Installation oder wenn eine der oben genannten Eigenschaften in der Befehlszeile angegeben wird, auf den Wert "1" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




