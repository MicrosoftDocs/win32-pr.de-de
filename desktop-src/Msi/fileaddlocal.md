---
description: Der Wert der FILEADDLOCAL-Eigenschaft gibt eine Liste von Dateischlüsseln an, die durch Kommas getrennt sind, die für die Ausführung auf dem lokalen Quellmedium installiert werden sollen.
ms.assetid: 89ae876e-53f0-4c1d-ba16-7513af79ee5e
title: FILEADDLOCAL (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c764fa89480cf4f37e19a4f6a10ee354a07bfe18f9fbc203ea0db4410f7bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946990"
---
# <a name="fileaddlocal-property"></a>FILEADDLOCAL (Eigenschaft)

Der Wert der **FILEADDLOCAL-Eigenschaft** gibt eine Liste von Dateischlüsseln an, die durch Kommas getrennt sind, die für die Ausführung auf dem lokalen Quellmedium installiert werden sollen. Für jeden Dateischlüssel in der Liste bestimmt das Installationsprogramm die Komponente, die diese Datei steuert, untersucht dann alle Features, die von der [Tabelle FeatureComponents](featurecomponents-table.md) mit dieser Komponente verknüpft sind, und installiert das Feature, das die geringste Menge an Speicherplatz erfordert. Die Dateischlüssel in der Liste müssen in der Spalte Datei der Tabelle [Datei vorhanden](file-table.md) sein.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass bei den Dateischlüsselnamen die Kleinschreibung beachtet wird. Beachten Sie außerdem Folgendes: Wenn das LocalOnly-Bitflag in der Spalte Attribute der Component-Tabelle für eine Komponente festgelegt ist, wird die Komponente für die lokale Ausführung installiert. [](component-table.md)

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
10. **FILEADDLOCAL**
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Wenn die Befehlszeile z. B. FOLGENDEs angibt: ADDLOCAL=ALL, ADDSOURCE = MyFeature, werden alle Features zuerst auf run-local und dann myFeature auf run-from-source festgelegt. Wenn die Befehlszeile auf ADDSOURCE=ALL, ADDLOCAL=MyFeature festgelegt ist, wird zuerst MyFeature auf run-local festgelegt, und wenn ADDSOURCE=ALL ausgewertet wird, werden alle Features (einschließlich MyFeature) auf die Ausführung aus der Quelle zurückgesetzt.

Das Installationsprogramm legt die [**Preselected-Eigenschaft**](preselected.md) während der Wiederaufnahme einer angehaltenen Installation oder bei Angabe einer der oben genannten Eigenschaften in der Befehlszeile auf den Wert "1" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




