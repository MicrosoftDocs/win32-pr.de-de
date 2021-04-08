---
description: Kopiert die logische Auslagerungs Datei oder das im Objekt Pfad angegebene Verzeichnis an den Speicherort, der durch den filename-Parameter angegeben wird. Diese Methode ist eine erweiterte Version der Copy-Methode.
ms.assetid: a8376dc8-eb73-4097-b84c-839432ac3a25
ms.tgt_platform: multiple
title: CopyEx-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 810f1d3bcf878d33756930f6bd3b6799c3513dc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861755"
---
# <a name="copyex-method-of-the-win32_pagefile-class"></a>CopyEx-Methode der Win32- \_ Pagefile-Klasse

Die **CopyEx** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode kopiert die logische Auslagerungs Datei oder das im Objekt Pfad angegebene Verzeichnis in den Speicherort, der durch den *filename* -Parameter angegeben wird. Diese Methode ist eine erweiterte Version der [**Copy**](copy-method-in-class-win32-directory.md) -Methode. Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Der voll qualifizierte Name der Kopie der Datei (oder des Verzeichnisses).

Beispiel: c: \\ Temp \\ NewDirectory

</dd> <dt>

*Stop filename* \[ vorgenommen\]
</dt> <dd>

Der Name der Datei oder des Verzeichnisses, in der die **CopyEx** -Methode fehlgeschlagen ist. Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.

</dd> <dt>

*Startdateiname* \[ in, optional\]
</dt> <dd>

Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **CopyEx** verwendet werden soll. Der Parameter " *StartFileName* " ist in der Regel der " *Stop filename* "-Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen Wenn dieser Parameter **null** ist, wird der Vorgang für die im ExecMethod-Befehl angegebene Datei oder das Verzeichnis ausgeführt.

</dd> <dt>

*Rekursiv* \[ in, optional\]
</dt> <dd>

**True** gibt an, dass die Eigentums Änderung rekursiv auf die Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.

> [!Note]  
> Bei Datei Instanzen wird der *rekursive* Parameter ignoriert.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich kopiert wurde, und jede andere Zahl gibt einen Fehler an.

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

Das Dateisystem ist nicht NTFS.

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

[**Win32- \_ Pagefile**](win32-pagefile.md)
</dt> </dl>

 

