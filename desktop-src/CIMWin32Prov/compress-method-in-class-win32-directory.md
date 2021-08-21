---
description: Komprimiert die logische Verzeichniseintragsdatei (oder das Verzeichnis), die im Objektpfad angegeben ist.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Compress-Methode der Win32_Directory Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15d9142abb95998fce803c30c439632775cd8ff807f3b7d99653875d08e534e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020668"
---
# <a name="compress-method-of-the-win32_directory-class"></a>Compress-Methode der Win32 \_ Directory-Klasse

Die **Compress** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) komprimiert die logische Verzeichniseintragsdatei (oder das Verzeichnis), die im Objektpfad angegeben ist.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.

<dl> <dt>

**0**
</dt> <dd>

Die Anforderung wurde erfolgreich gesendet.

</dd> <dt>

**2**
</dt> <dd>

Der Zugriff wurde verweigert.

</dd> <dt>

**8**
</dt> <dd>

Es ist ein nicht angegebener Fehler aufgetreten.

</dd> <dt>

**9**
</dt> <dd>

Der angegebene Name war ungültig.

</dd> <dt>

**10**
</dt> <dd>

Das angegebene Objekt ist bereits vorhanden.

</dd> <dt>

**11**
</dt> <dd>

Das Dateisystem ist kein NTFS-System.

</dd> <dt>

**12**
</dt> <dd>

Die Plattform ist nicht Windows.

</dd> <dt>

**13**
</dt> <dd>

Das Laufwerk ist nicht identisch.

</dd> <dt>

**14**
</dt> <dd>

Das Verzeichnis ist nicht leer.

</dd> <dt>

**15**
</dt> <dd>

Es ist ein Freigabeverstoß vor worden.

</dd> <dt>

**16**
</dt> <dd>

Die angegebene Startdatei war ungültig.

</dd> <dt>

**17**
</dt> <dd>

Für den Vorgang ist keine Berechtigung erforderlich.

</dd> <dt>

**21**
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Komprimierung bietet eine Möglichkeit, zusätzlichen Speicherplatz auf einem Laufwerk frei zu geben, ohne neue Hardware zu kaufen und ohne Dateien oder Ordner zu entfernen. Abhängig von der Größe Ihrer Festplatte und dem Typ der auf diesem Datenträger gespeicherten Dateien können Sie möglicherweise Hunderte von Megabyte Speicherplatz auf dem Datenträger wiederherstellen und so die Notwendigkeit ausschließen, eine neue Festplatte zu erwerben und den Computer offline zu schalten, bis das neue Laufwerk installiert ist.

Die Compress-Methode komprimiert alle Dateien und Unterordner innerhalb eines angegebenen Ordners. Darüber hinaus enthält die -Klasse auch eine Uncompress-Methode, die die Komprimierung aus allen Dateien und Unterordnern in einem Ordner entfernt. Ähnliche Methoden werden auch mit der CIM \_ Datafile-Klasse bereitgestellt. Dadurch können Sie bestimmte Dateien in einem Ordner selektiv komprimieren oder dekomprimieren.

Da die Komprimierung eine geringfügige Leistungsschwätung mit sich kommt, wird sie nicht für Dateien oder Ordner empfohlen, auf die routinemäßig zugegriffen wird. Beispielsweise möchten Sie wahrscheinlich keine Datenbankdateien, Protokolldateien oder Benutzerprofilordner komprimieren. Bessere Kandidaten für die Komprimierung sind Dateien und Ordner, auf die nicht sehr häufig zugegriffen wird. Beispielsweise können Sie ein Skript schreiben, um eine Sammlung von Ordnern auf einem Laufwerk zurücksendet, auf die seit einem Monat oder mehr nicht zugegriffen wurde, und dann jeden dieser Ordner zu komprimieren.

Der speicherplatz, der durch komprimieren von Ordnern freigegeben wird, hängt vom Typ der in diesem Ordner gespeicherten Dateien ab. Beispielsweise sind .jpg Dateien bereits komprimiert, und eine weitere Komprimierung hat nur geringe Auswirkungen auf die Größe der Datei. Bei anderen Dateitypen können die Einsparungen jedoch erheblich sein. Beispielsweise wurde ein neuer Ordner auf einem Windows 2000-basierten Testcomputer erstellt, und 33 Microsoft Word-Dokumente, die insgesamt 15 MB Speicherplatz auf dem Datenträger belegen, wurden in diesen Ordner kopiert. Als die Dokumente komprimiert wurden, dauerte der Ordner nur 7 MB Speicherplatz.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Beispiel wird der Ordner C: \\ Skripts komprimiert.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32-Verzeichnis \_**](win32-directory.md)
</dt> <dt>

[**Dekomprimieren**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

