---
description: Die MsiLogging-Eigenschaft legt den Standardprotokollierungsmodus für das Windows Installer-Paket fest.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: MsiLogging-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e166a52e970cdb3e0be5ffae6611a8ea9a299232d55f36a45ba470b3717cafae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042780"
---
# <a name="msilogging-property"></a>MsiLogging-Eigenschaft

Die **MsiLogging-Eigenschaft** legt den Standardprotokollierungsmodus für das Windows Installer-Paket fest. Wenn diese optionale Eigenschaft in der [Property-Tabelle](property-table.md)vorhanden ist, generiert das Installationsprogramm eine Protokolldatei mit dem Namen \* MSI. Protokoll. Der vollständige Pfad zur Protokolldatei wird durch den Wert der [**MsiLogFileLocation-Eigenschaft**](msilogfilelocation.md) angegeben.

## <a name="value"></a>Wert

Der Wert dieser Eigenschaft sollte eine Zeichenfolge der folgenden Zeichen sein, die den Standardprotokollierungsmodus angeben.



| Wert                                                                        | Bedeutung                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>I</dt> </dl> | Statusmeldungen.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Nichttale Warnungen.<br/>                                                  |
| <dl> <dt>e</dt> </dl> | Alle Fehlermeldungen.<br/>                                                 |
| <dl> <dt>Eine</dt> </dl> | Starten von Aktionen.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Aktionsspezifische Datensätze.<br/>                                            |
| <dl> <dt>n</dt> </dl> | Benutzeranforderungen.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Anfängliche Benutzeroberflächenparameter.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Informationen zu nicht genügend Arbeitsspeicher oder schwerwiegenden Beendigungsinformationen.<br/>                            |
| <dl> <dt>o</dt> </dl> | Nachrichten mit nicht genügend Speicherplatz.<br/>                                         |
| <dl> <dt>p</dt> </dl> | Terminaleigenschaften.<br/>                                                |
| <dl> <dt>V</dt> </dl> | Ausführliche Ausgabe.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Zusätzliche Debuginformationen. Nur auf Windows Server 2003 verfügbar.<br/> |
| <dl> <dt>!</dt> </dl> | Leeren Sie jede Zeile in das Protokoll.<br/>                                         |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist ab Windows Installer 4.0 verfügbar.

Sie können die Werte "+" und \* "" der Option /L nicht im Wert der **MsiLogging-Eigenschaft** verwenden.

Der Protokollierungsmodus kann mithilfe einer Richtlinie, einer Befehlszeilenoption oder programmgesteuert festgelegt werden. Dadurch wird der Standardprotokollierungsmodus überschrieben. Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungsmodus verfügbar sind, finden Sie im Abschnitt Protokollierung des [Windows Installers](windows-installer-logging.md) unter Normale [Protokollierung.](normal-logging.md)

Wenn die **MsiLogging-Eigenschaft** in der [Property-Tabelle](property-table.md)vorhanden ist, kann der Standardprotokollierungsmodus des Pakets geändert werden, indem der Wert dieser Eigenschaft mithilfe einer [Datenbanktransformation](database-transforms.md)geändert wird. Der Standardprotokollierungsmodus kann nicht mithilfe eines [Patchpakets](patch-packages.md) (einer MSP-Datei) geändert werden.

Wenn die **MsiLogging-Eigenschaft** in der [Property-Tabelle](property-table.md)festgelegt wurde, kann der Standardprotokollierungsmodus für alle Benutzer des Computers durch Festlegen der [Richtlinie DisableLoggingFromPackage](disableloggingfrompackage.md) und [der Protokollierungsrichtlinie](logging.md) angegeben werden. Wenn Sie sowohl die Richtlinie DisableLoggingFromPackage als auch die Protokollierungsrichtlinie festlegen, wird die **MsiLogging-Eigenschaft** für alle Pakete überschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 4.5 auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




