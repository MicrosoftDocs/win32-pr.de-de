---
description: Die EnableLog-Methode des Installer-Objekts ermöglicht die Protokollierung des ausgewählten Nachrichtentyps für alle nachfolgenden Installationssitzungen im aktuellen Prozessbereich.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Installer.EnableLog-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 48481a701b7e78de372f5579dab5c9d5976a68063958b0812d6ae1ddc08b109a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631696"
---
# <a name="installerenablelog-method"></a>Installer.EnableLog-Methode

Die **EnableLog-Methode** des [**Installer-Objekts**](installer-object.md) ermöglicht die Protokollierung des ausgewählten Nachrichtentyps für alle nachfolgenden Installationssitzungen im aktuellen Prozessbereich.

## <a name="syntax"></a>Syntax


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*logMode* 
</dt> <dd>

Eine erforderliche Zeichenfolge, die Buchstaben enthält, die die zu protokollierenden Nachrichtentypen darstellen. Die Zeichenfolge kann eine Kombination der folgenden Werte sein.



| Wert | Beschreibung                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Nur Informationsmeldungen.                                                                             |
| w     | Nicht schwerwiegende Warnmeldungen.                                                                            |
| e     | Fehlermeldungen, die schwerwiegende Fehler sein können.                                                               |
| f     | Liste der verwendeten Dateien, die ersetzt werden müssen.                                                         |
| a     | Start der Aktionsbenachrichtigung.                                                                          |
| r     | Aktionsdatensatz, der aktionsspezifische Inhalte enthält.                                              |
| u     | Benutzeranforderungsnachrichten.                                                                                 |
| c     | Parameter für die Benutzeroberflächeninitialisierung.                                                                          |
| m     | Meldung zu nicht genügend Arbeitsspeicher.                                                                                 |
| v     | Sendet große Mengen von Informationen an Protokolldateien, die für Benutzer im Allgemeinen nicht nützlich sind. Kann zur Unterstützung verwendet werden. |
| p     | Dump-Eigenschaftentabelle; "property = value" beim Beenden der Engine                                          |
| \+    | Fügen Sie an eine vorhandene Protokolldatei an.                                                                           |
| !     | Leeren Sie jede Zeile in die Protokolldatei.                                                                       |
| x     | Zusätzliche Debuginformationen. Diese Option ist nur mit Windows Server 2003 verfügbar.                      |
| o     | Nachrichten mit nicht genügend Speicherplatz.                                                                            |



 

</dd> <dt>

*Logfile* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfad zur zu erstellenden Protokolldatei enthält. Verwenden Sie eine leere Zeichenfolge (""), um die Protokollierung zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Pfad zum Protokolldateispeicherort muss bereits vorhanden sein, wenn diese Methode verwendet wird. Der Installer erstellt nicht die Verzeichnisstruktur für die Protokolldatei.

Die mit **EnableLog** festgelegten Protokollierungsoptionen überschreiben alle vorhandenen Windows Installer-Protokollierungsrichtlinieneinstellungen.

Die Protokollierung überschreibt standardmäßig eine vorhandene Protokolldatei. Sie müssen den Buchstaben "+" im Protokollierungsmodus verwenden, um an eine vorhandene Protokolldatei anzufügen.

Die Option "!" wird nicht empfohlen, da sie die Installation erheblich verlangsamen kann. Diese Option kann beim Debuggen einer Installation nützlich sein.

Das folgende Beispielskript aktiviert die ausführliche Protokollierung für eine Installation. Am Ende der Installation befindet sich die generierte Protokolldatei unter c: \\ temp \\ install.log.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Installerprotokollierung](windows-installer-logging.md)
</dt> </dl>

 

 




