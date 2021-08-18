---
description: Die REINSTALLMODE-Eigenschaft ist eine Zeichenfolge, die Buchstaben enthält, die den Typ der auszuführenden Neuinstallation angeben.
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: REINSTALLMODE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 227a069fa0974758bf623c83ef23d40902d9feb140f69446c57c2d723468054f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637876"
---
# <a name="reinstallmode-property"></a>REINSTALLMODE-Eigenschaft

Die **REINSTALLMODE-Eigenschaft** ist eine Zeichenfolge, die Buchstaben enthält, die den Typ der auszuführenden Neuinstallation angeben. Bei Optionen wird die Groß-/Kleinschreibung nicht beachtet, und die Reihenfolge ist unabhängig. Diese Eigenschaft sollte normalerweise immer in Verbindung mit der [**REINSTALL-Eigenschaft**](reinstall.md) verwendet werden. Diese Eigenschaft kann jedoch auch während der Installation verwendet werden, nicht nur neu installieren.

> [!Note]  
> Der Windows Installer ignoriert die **REINSTALLMODE-Eigenschaft** während einer [Administratorinstallation.](administrative-installation.md)

 

## <a name="reinstall-option-codes"></a>Codes für Neuinstallationsoptionen

Der **REINSTALLMODE** ist standardmäßig "omus".



| Code | Option                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | Installieren Sie nur neu, wenn die Datei fehlt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | Installieren Sie neu, wenn die Datei fehlt oder eine ältere Version ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| e    | Installieren Sie neu, wenn die Datei fehlt oder eine identische oder ältere Version ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | Installieren Sie neu, wenn die Datei fehlt oder eine andere Version vorhanden ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | Überprüfen Sie die Prüfsummenwerte, und installieren Sie die Datei neu, wenn sie fehlen oder beschädigt sind. Dieses Flag repariert nur Dateien, die msidbFileAttributesChecksum in der Attributes -Spalte der [Dateitabelle enthalten.](file-table.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a    | Erzwingen sie, dass alle Dateien unabhängig von prüfsumme oder Version neu installiert werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | Schreiben Sie alle erforderlichen Registrierungseinträge aus der [Registrierungstabelle](registry-table.md) neu, die an **HKEY \_ CURRENT \_ USER** gehen.<br/> oder **HKEY \_ USERS**<br/> Registrierungsstruktur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | Umschreiben aller erforderlichen Registrierungseinträge aus der [Registrierungstabelle,](registry-table.md) die zum **lokalen HKEY-COMPUTER \_ \_** wechseln<br/> oder **HKEY \_ CLASSES \_ ROOT**<br/> Registrierungsstruktur. Schreiben Sie alle Informationen aus den [Klassentabellen](class-table.md), [Verbtabellen,](verb-table.md) [PublishComponent-Tabellen,](publishcomponent-table.md) [ProgID-Tabellen,](progid-table.md) [MIME-Tabellen,](mime-table.md) [Symboltabellen,](icon-table.md) [Erweiterungstabellen](extension-table.md)und [AppID-Tabellen](appid-table.md) neu, unabhängig von der Computer- oder Benutzerzuweisung. Installieren Sie alle [**qualifizierten Komponenten neu.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) Bei der Neuinstallation einer Anwendung werden mit dieser Option die Aktionen [RegisterTypeLibraries](registertypelibraries-action.md) und [InstallODBC](installodbc-action.md) ausgeführt.<br/> |
| s    | Installieren Sie alle Verknüpfungen neu, und speichern Sie alle Symbole neu, wobei vorhandene Verknüpfungen und Symbole überschrieben werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | Verwenden Sie , um aus dem Quellpaket auszuführen und das lokale Paket erneut zwischenzuspeichern. Verwenden Sie den v-Neuinstallationsoptionscode nicht für die erste Installation einer Anwendung oder eines Features.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

Wenn die **REINSTALLMODE-Eigenschaft** definiert ist, ohne auch die [**REINSTALL-Eigenschaft**](reinstall.md) zu definieren, gelten die angegebenen Erkennungsmodi weiterhin und geben den "Overwrite"-Modus für eine normale Installation an. Die **REINSTALLMODE-Eigenschaft** wirkt sich nur auf die Features aus, die normalerweise für die Installation ausgewählt werden. Wenn die **REINSTALLMODE-Eigenschaft** vorhanden ist, werden die Features nicht neu installiert. Die Neuinstallation von Features erfordert das Vorhandensein der **REINSTALL-Eigenschaft.**

Die Optionscodes für diese Eigenschaft entsprechen der [Befehlszeilenoption](command-line-options.md) "/f". Die Befehlszeilenoption hat den Standardwert "pecms".

> [!Note]  
> Nur die Dateien, die Prüfsummeninformationen enthalten, werden jemals überprüft und repariert. Das REINSTALLMODE \_ FILEVERIFY-Flag (ccode oben) repariert nur Dateien, die msidbFileAttributesChecksum in der Attributes -Spalte der [Dateitabelle enthalten.](file-table.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




