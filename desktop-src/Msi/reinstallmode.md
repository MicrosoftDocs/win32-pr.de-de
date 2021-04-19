---
description: Die REINSTALLMODE-Eigenschaft ist eine Zeichenfolge, die Buchstaben enthält, die den Typ der auszuführenden Neuinstallation angeben.
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: REINSTALLMODE (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab48043ef92770cbc3a1f5ab92e459128c9945ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355900"
---
# <a name="reinstallmode-property"></a>REINSTALLMODE (Eigenschaft)

Die **REINSTALLMODE** -Eigenschaft ist eine Zeichenfolge, die Buchstaben enthält, die den Typ der auszuführenden Neuinstallation angeben. Optionen Unterscheidung nach Groß-/Kleinschreibung und Reihenfolge unabhängig. Diese Eigenschaft sollte normalerweise immer in Verbindung mit der Eigenschaft [**neu installieren**](reinstall.md) verwendet werden. Diese Eigenschaft kann jedoch auch während der Installation verwendet werden, nicht nur bei der erneuten Installation.

> [!Note]  
> Der Windows Installer ignoriert die Eigenschaft **REINSTALLMODE** während einer [administrativen Installation](administrative-installation.md).

 

## <a name="reinstall-option-codes"></a>Optionen Codes für Neuinstallation

Der **REINSTALLMODE** ist standardmäßig "omus".



| Code | Option                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | Installieren Sie nur dann neu, wenn die Datei fehlt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | Installieren Sie neu, wenn die Datei fehlt oder eine ältere Version vorhanden ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| e    | Installieren Sie neu, wenn die Datei fehlt oder eine gleichmäßige oder eine ältere Version ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | Installieren Sie neu, wenn die Datei fehlt oder eine andere Version vorhanden ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | Überprüfen Sie die Prüfsummen Werte, und installieren Sie die Datei erneut, wenn Sie nicht vorhanden oder beschädigt sind. Dieses Flag repariert nur Dateien, die msidbFileAttributesChecksum enthalten, in der Spalte Attribute der [Dateitabelle](file-table.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a    | Erzwingen, dass alle Dateien neu installiert werden, unabhängig von der Prüfsumme oder der Version.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | Alle erforderlichen Registrierungseinträge aus der [Registrierungs Tabelle](registry-table.md) neu schreiben, die zum **aktuellen HKEY- \_ \_ Benutzer** wechseln<br/> oder **HKEY- \_ Benutzer**<br/> Registrierungs Struktur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | Schreiben Sie alle erforderlichen Registrierungseinträge aus der [Registrierungs Tabelle](registry-table.md) um, die an den **lokalen HKEY- \_ \_ Computer** weitergeleitet werden.<br/> oder **HKEY \_ - \_ Klassen** Stamm<br/> Registrierungs Struktur. Schreiben Sie alle Informationen aus der [Klassen Tabelle](class-table.md), [Verb Tabelle](verb-table.md), [PublishComponent-Tabelle](publishcomponent-table.md), [ProgID](progid-table.md)-Tabelle, [MIME](mime-table.md)-Tabelle, [Symboltabelle](icon-table.md), [Erweiterungs Tabelle](extension-table.md)und [AppID-Tabelle](appid-table.md) unabhängig von Computer-oder Benutzer Zuweisung um. Installieren Sie alle [**qualifizierten Komponenten neu.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) Bei der erneuten Installation einer Anwendung werden mit dieser Option die Aktionen [registertypelibraries](registertypelibraries-action.md) und [installodbc](installodbc-action.md) ausgeführt.<br/> |
| s    | Installieren Sie alle Verknüpfungen neu, und Zwischenspeichern Sie alle Symbole neu, indem Sie vorhandene Tastenkombinationen und Symbole überschreiben.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | Verwenden Sie, um aus dem Quellpaket auszuführen und das lokale Paket erneut zwischenzuspeichern. Verwenden Sie den Code für die v-Neuinstallations Option nicht für die erste Installation einer Anwendung oder eines Features.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

Wenn die Eigenschaft **REINSTALLMODE** definiert ist, ohne auch die Eigenschaft [**neu installieren**](reinstall.md) zu definieren, gelten die angegebenen "Erkennungs Modi" weiterhin und geben den Modus "überschreiben" für eine normale Installation an. Die Eigenschaft **REINSTALLMODE** wirkt sich nur auf die Features aus, die normalerweise für die Installation ausgewählt werden. Wenn die Eigenschaft **REINSTALLMODE** vorhanden ist, werden die Funktionen nicht neu installiert. Die Neuinstallation von Features erfordert, dass die Eigenschaft **neu installieren** vorhanden ist.

Die Options Codes für diese Eigenschaft entsprechen der [Befehlszeilenoption](command-line-options.md) "/f". Die Befehlszeilenoption hat den Standardwert "pecms".

> [!Note]  
> Nur die Dateien, die Prüfsummeninformationen enthalten, werden immer überprüft und repariert. Das Flag REINSTALLMODE \_ fileverify (ccode oben) repariert nur Dateien, die msidbFileAttributesChecksum haben, in der Spalte Attribute der [Dateitabelle](file-table.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




