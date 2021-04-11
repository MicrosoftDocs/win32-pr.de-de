---
description: Komprimiert die im Objekt Pfad angegebene logische Verzeichniseintrags Datei (oder das angegebene Verzeichnis).
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Compress-Methode der Win32_Directory-Klasse
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
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126116"
---
# <a name="compress-method-of-the-win32_directory-class"></a>Methode komprimieren der Win32- \_ Verzeichnis Klasse

Die  [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode komprimieren komprimiert die im Objekt Pfad angegebene logische Verzeichniseintrags Datei (oder das Verzeichnis).

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und jede andere Zahl gibt einen Fehler an.

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

Ein nicht angegebener Fehler ist aufgetreten.

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

Das Dateisystem ist kein NTFS.

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

Es ist eine Freigabe Verletzung aufgetreten.

</dd> <dt>

**16**
</dt> <dd>

Die angegebene Startdatei war ungültig.

</dd> <dt>

**17**
</dt> <dd>

Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.

</dd> <dt>

**21**
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit der Komprimierung können Sie zusätzlichen Speicherplatz auf einem Laufwerk freigeben, ohne neue Hardware kaufen und Dateien oder Ordner nicht entfernen zu müssen. Abhängig von der Größe der Festplatte und dem Dateityp, der auf diesem Datenträger gespeichert ist, können Sie möglicherweise Hunderte von Megabyte Speicherplatz wiederherstellen. dadurch ist es nicht mehr erforderlich, dass Sie eine neue Festplatte kaufen und den Computer offline schalten, bis das neue Laufwerk installiert ist.

Die Methode komprimieren komprimiert alle Dateien und Unterordner innerhalb eines angegebenen Ordners. Darüber hinaus enthält die-Klasse auch eine uncompress-Methode, die die Komprimierung aus allen Dateien und Unterordnern in einem Ordner entfernt. Ähnliche Methoden werden auch mit der CIM \_ DataFile-Klasse bereitgestellt. Auf diese Weise können Sie bestimmte Dateien in einem Ordner selektiv komprimieren oder dekomprimieren.

Da die Komprimierung eine geringfügige Leistungs Einbuße eingibt, wird Sie nicht für Dateien oder Ordner empfohlen, auf die routinemäßig zugegriffen wird. beispielsweise möchten Sie wahrscheinlich nicht Datenbankdateien, Protokolldateien oder Benutzerprofil Ordner komprimieren. Bessere Kandidaten für die Komprimierung sind Dateien und Ordner, auf die nicht sehr häufig zugegriffen wird. Sie können z. b. ein Skript schreiben, um eine Sammlung von Ordnern auf einem Laufwerk zurückzugeben, auf die mindestens ein Monat lang nicht zugegriffen wurde, und dann alle diese Ordner komprimieren.

Der durch die Komprimierung von Ordnern freigegebene Speicherplatz variiert je nach Dateityp, der in diesem Ordner gespeichert ist. Beispielsweise sind die JPG-Dateien bereits komprimiert, und die weitere Komprimierung hat kaum Auswirkungen auf die Größe der Datei. Bei anderen Dateitypen können die Einsparungen jedoch beträchtlich sein. Beispielsweise wurde ein neuer Ordner auf einem Windows 2000-basierten Testcomputer erstellt, und es wurden 33 Microsoft Word-Dokumente mit einer Gesamtgröße von 15 Megabyte (MB) an Speicherplatz in diesen Ordner kopiert. Wenn die Dokumente komprimiert wurden, benötigte der Ordner nur 7 MB Speicherplatz.

## <a name="examples"></a>Beispiele

Das folgende VBScript-Beispiel komprimiert den Ordner C: \\ Scripts.


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
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Verzeichnis**](win32-directory.md)
</dt> <dt>

[**Dekomprimieren**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

