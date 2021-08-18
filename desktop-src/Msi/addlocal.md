---
description: Der Wert der ADDLOCAL-Eigenschaft ist eine Liste von Features, die durch Kommas getrennt sind und lokal installiert werden sollen.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: ADDLOCAL-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82ca86fabd1f90c55c1c3dbf4704a89480a9b23a19f943aca3fd53c1f9065270
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822010"
---
# <a name="addlocal-property"></a>ADDLOCAL-Eigenschaft

Der Wert der **ADDLOCAL-Eigenschaft** ist eine Liste von Features, die durch Kommas getrennt sind und lokal installiert werden sollen. Die Features müssen in der Spalte Feature der [Featuretabelle](feature-table.md)vorhanden sein. Um alle Features lokal zu installieren, verwenden Sie ADDLOCAL=ALL in der Befehlszeile. Geben Sie ADDLOCAL=ALL nicht in die [Eigenschaftentabelle](property-table.md)ein, da dadurch ein lokal installiertes Paket generiert wird, das nicht ordnungsgemäß entfernt werden kann.

## <a name="remarks"></a>Hinweise

Bei Featurenamen wird die Groß-/Kleinschreibung beachtet. Wenn das SourceOnly-Bitflag in der Spalte Attribute der [Komponententabelle](component-table.md) für eine Komponente eines Features in der Liste festgelegt ist, wird diese Komponente als Ausführung aus der Quelle installiert.

Das Installationsprogramm wertet immer die folgenden Eigenschaften in der folgenden Reihenfolge aus:

1.  **ADDLOCAL**
2.  [**Entfernen**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Installieren**](reinstall.md)
6.  [**Werben**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Beispiel:

-   Wenn in der Befehlszeile Folgendes angegeben ist: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, werden alle Features zuerst auf "run-local" und dann auf **"MyFeature"** auf "run-from-source" festgelegt.
-   Wenn die Befehlszeile lautet: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, wird **zuerst MyFeature** auf run-local festgelegt, und wenn ADDSOURCE=ALL ausgewertet wird, werden alle Features (einschließlich **MyFeature**) auf run-from-source zurückgesetzt.

Das Installationsprogramm legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation oder wenn eine der vorherigen Eigenschaften in der Befehlszeile angegeben wird, auf den Wert "1" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




