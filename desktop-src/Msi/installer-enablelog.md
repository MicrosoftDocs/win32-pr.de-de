---
description: Die EnableLog-Methode des Installer-Objekts aktiviert die Protokollierung des ausgewählten Nachrichten Typs für alle nachfolgenden Installations Sitzungen im aktuellen Prozessbereich.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Installer. EnableLog-Methode
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
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373599"
---
# <a name="installerenablelog-method"></a>Installer. EnableLog-Methode

Die **EnableLog** -Methode des [**Installer**](installer-object.md) -Objekts aktiviert die Protokollierung des ausgewählten Nachrichten Typs für alle nachfolgenden Installations Sitzungen im aktuellen Prozessbereich.

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

Eine erforderliche Zeichenfolge, die Buchstaben enthält, die die zu protokollieren Nachrichten Typen darstellen. Die Zeichenfolge kann eine Kombination der folgenden Werte sein.



| Wert | BESCHREIBUNG                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Informationsmeldungen.                                                                             |
| w     | Nicht schwerwiegende Warnmeldungen.                                                                            |
| e     | Fehlermeldungen, die schwerwiegende Fehler sein könnten.                                                               |
| f     | Die Liste der zu verwendenden Dateien, die ersetzt werden müssen.                                                         |
| a     | Beginn der Aktions Benachrichtigung.                                                                          |
| r     | Aktions Daten Satz mit Inhalt, der für Action spezifisch ist.                                              |
| u     | Benutzer Anforderungs Nachrichten.                                                                                 |
| c     | Initialisierungs Parameter für die Benutzeroberfläche.                                                                          |
| m     | Nicht genügend Arbeitsspeicher.                                                                                 |
| v     | Sendet große Mengen von Informationen an die Protokolldatei, die für Benutzer im Allgemeinen nicht nützlich sind. Kann zur Unterstützung von verwendet werden. |
| p     | Dump-Eigenschaften Tabelle; "Property = Value" bei der Engine-Beendigung                                          |
| \+    | Fügen Sie an die vorhandene Protokolldatei an.                                                                           |
| !     | Leeren Sie jede Zeile in die Protokolldatei.                                                                       |
| x     | Zusätzliche Debuginformationen. Diese Option ist nur in Windows Server 2003 verfügbar.                      |
| o     | Nicht genügend Speicherplatz Nachrichten.                                                                            |



 

</dd> <dt>

*Protokolldatei* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfad zu der zu erstellenden Protokolldatei enthält. Verwenden Sie eine leere Zeichenfolge (""), um die Protokollierung zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Pfad zum Speicherort der Protokolldatei muss bereits vorhanden sein, wenn diese Methode verwendet wird. Das Installationsprogramm erstellt nicht die Verzeichnisstruktur für die Protokolldatei.

Die mithilfe von **EnableLog** festgelegten Protokollierungs Optionen überschreiben alle vorhandenen Windows Installer Protokollierungs Richtlinien Einstellungen.

Bei der Protokollierung wird standardmäßig eine vorhandene Protokolldatei überschrieben. Sie müssen den Buchstaben "+" im Protokollierungs Modus verwenden, um an eine vorhandene Protokolldatei anzufügen.

Die Option "!" wird nicht empfohlen, da Sie die Installation erheblich verlangsamen kann. Diese Option kann nützlich sein, wenn Sie eine-Installation Debuggen.

Das folgende Beispielskript schaltet die ausführliche Protokollierung für eine-Installation ein. Am Ende der Installation wird die generierte Protokolldatei unter "c: \\ Temp \\ install. log" angezeigt.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows Installer Protokollierung](windows-installer-logging.md)
</dt> </dl>

 

 




