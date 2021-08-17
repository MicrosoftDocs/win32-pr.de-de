---
description: Der Wert der FILEADDSOURCE-Eigenschaft gibt eine Liste von Dateischlüsseln an, die durch Kommas getrennt sind, die installiert werden sollen, um von den Quellmedien ausgeführt zu werden.
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: FILEADDSOURCE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7678c42e683b70fc61e563c57ee234c523078bcdd737bf8f28bc2c05302fbb43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636562"
---
# <a name="fileaddsource-property"></a>FILEADDSOURCE-Eigenschaft

Der Wert der **FILEADDSOURCE-Eigenschaft** gibt eine Liste von Dateischlüsseln an, die durch Kommas getrennt sind, die installiert werden sollen, um von den Quellmedien ausgeführt zu werden. Für jeden Dateischlüssel in der Liste bestimmt das Installationsprogramm die Komponente, die diese Datei steuert, untersucht dann alle Features, die mit dieser Komponente durch die [Tabelle FeatureComponents](featurecomponents-table.md) verknüpft sind, und installiert das Feature, das die geringste Menge an Speicherplatz erfordert. Die Dateischlüssel in der Liste müssen in der Spalte Datei der [Dateitabelle](file-table.md) vorhanden sein.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass bei den Dateischlüsselnamen die Groß-/Kleinschreibung beachtet wird. Beachten Sie außerdem Folgendes: Wenn das LocalOnly-Bitflag in der Spalte Attribute der [Komponententabelle](component-table.md) für eine Komponente festgelegt ist, wird die Komponente installiert, um lokal ausgeführt zu werden.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Entfernen**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Installieren**](reinstall.md)
6.  [**Werben**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. **FILEADDSOURCE**
12. [**FILEADDDEFAULT**](fileadddefault.md)

Wenn die Befehlszeile beispielsweise FOLGENDEs angibt: ADDLOCAL=ALL, ADDSOURCE = MyFeature, werden alle Features zuerst auf "run-local" und dann auf "MyFeature" auf "run-from-source" festgelegt. Wenn die Befehlszeile lautet: ADDSOURCE=ALL, ADDLOCAL=MyFeature, wird zuerst MyFeature auf run-local festgelegt, und wenn ADDSOURCE=ALL ausgewertet wird, werden alle Features (einschließlich MyFeature) auf run-from-source zurückgesetzt.

Das Installationsprogramm legt die [**Preselected-Eigenschaft**](preselected.md) während der Wiederaufnahme einer angehaltenen Installation oder wenn eine der oben genannten Eigenschaften in der Befehlszeile angegeben wird, auf den Wert "1" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




