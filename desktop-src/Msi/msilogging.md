---
description: Die MsiLogging-Eigenschaft legt den Standard Protokollierungs Modus für das Windows Installer Paket fest.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: MsiLogging-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358757"
---
# <a name="msilogging-property"></a>MsiLogging-Eigenschaft

Die **MsiLogging** -Eigenschaft legt den Standard Protokollierungs Modus für das Windows Installer Paket fest. Wenn diese optionale Eigenschaft in der [Eigenschaften Tabelle](property-table.md)vorhanden ist, generiert das Installationsprogramm eine Protokolldatei mit dem Namen MSI \* . Angezeigt. Der vollständige Pfad zur Protokolldatei wird durch den Wert der [**msilogfileloation**](msilogfilelocation.md) -Eigenschaft angegeben.

## <a name="value"></a>Wert

Der Wert dieser Eigenschaft muss eine Zeichenfolge mit den folgenden Zeichen sein, die den Standard Protokollierungs Modus angeben.



| Wert                                                                        | Bedeutung                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>I</dt> </dl> | Status Meldungen.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Nicht schwerwiegende Warnungen.<br/>                                                  |
| <dl> <dt>e</dt> </dl> | Alle Fehlermeldungen.<br/>                                                 |
| <dl> <dt>ein</dt> </dl> | Starten von Aktionen.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Aktions spezifische Datensätze.<br/>                                            |
| <dl> <dt>n</dt> </dl> | Benutzer Anforderungen.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Anfängliche Parameter für die Benutzeroberfläche.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Nicht genügend Arbeitsspeicher oder schwerwiegende Exit-Informationen.<br/>                            |
| <dl> <dt>o</dt> </dl> | Nicht genügend Speicherplatz Nachrichten.<br/>                                         |
| <dl> <dt>cker</dt> </dl> | Terminal Eigenschaften.<br/>                                                |
| <dl> <dt>Ramelow</dt> </dl> | Ausführliche Ausgabe.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Zusätzliche Debuginformationen. Nur verfügbar auf Windows Server 2003.<br/> |
| <dl> <dt>!</dt> </dl> | Leeren Sie jede Zeile in das Protokoll.<br/>                                         |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist ab Windows Installer 4,0 verfügbar.

Sie können die Werte "+" und " \* " der/L-Option nicht im Wert der **MsiLogging** -Eigenschaft verwenden.

Der Protokollierungs Modus kann mithilfe von Richtlinie, einer Befehlszeilenoption oder Programm gesteuert festgelegt werden. Dies überschreibt den Standard Protokollierungs Modus. Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungs Modus verfügbar sind, finden Sie unter [normale Protokollierung](normal-logging.md) im Abschnitt [Windows Installer Protokollierung](windows-installer-logging.md) .

Wenn die **MsiLogging** -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)vorhanden ist, kann der Standard Protokollierungs Modus des Pakets durch Ändern des Werts dieser Eigenschaft mithilfe einer [Daten Bank Transformation](database-transforms.md)geändert werden. Der Standard Protokollierungs Modus kann nicht mithilfe eines [Patchpakets](patch-packages.md) (MSP-Datei) geändert werden.

Wenn die **MsiLogging** -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)festgelegt wurde, kann der Standard Protokollierungs Modus für alle Benutzer des Computers durch Festlegen der Richtlinie " [disableloggingfrompackage](disableloggingfrompackage.md) " und der [Protokollierungs](logging.md) Richtlinie angegeben werden. Durch das Festlegen der disableloggingfrompackage-Richtlinie und der Protokollierungs Richtlinie wird die **MsiLogging** -Eigenschaft für alle Pakete überschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




