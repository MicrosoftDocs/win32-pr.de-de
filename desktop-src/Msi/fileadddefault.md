---
description: Der Wert der FILEADDDEFAULT-Eigenschaft ist eine Liste von Dateischlüsseln, die durch Kommas getrennt sind, die in ihrer Standardkonfiguration installiert sind.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: FILEADDDEFAULT(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa5692cbba5b00aff6c3cbdef66e33420b4b135d0c3dfa13d9ae6e2255e5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828950"
---
# <a name="fileadddefault-property"></a>FILEADDDEFAULT(Eigenschaft)

Der Wert der **FILEADDDEFAULT-Eigenschaft** ist eine Liste von Dateischlüsseln, die durch Kommas getrennt sind, die in ihrer Standardkonfiguration installiert sind. Für jeden Dateischlüssel in der Liste bestimmt das Installationsprogramm die Komponente, die diese Datei steuert, und installiert das Feature, das den geringsten Speicherplatz erfordert. Die Dateischlüssel in der Liste müssen in der Spalte Datei der Tabelle [Datei vorhanden](file-table.md) sein. Ein Feature wird im gleichen Installationszustand installiert, als ob der Benutzer bei Bedarf eine Installation des Features angefordert hätte. Der Zustand wird bestimmt, welche Bits für das Feature in der Spalte Attribute der [Featuretabelle](feature-table.md)festgelegt werden und welche Bits für die Komponenten des Features in der Spalte Attribute der Component -Tabelle festgelegt [werden.](component-table.md)

## <a name="remarks"></a>Hinweise

Beachten Sie, dass bei den Dateischlüsselnamen die Kleinschreibung beachtet wird. Beachten Sie außerdem Folgendes: Wenn das SourceOnly-Bitflag in der Spalte Attribute der [Component-Tabelle](component-table.md) für eine Komponente festgelegt ist, wird die Komponente installiert, um sie aus der Quelle ausführen zu können.

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
11. [**FILEADDSOURCE**](fileaddsource.md)
12. **FILEADDDEFAULT**

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

 

 




