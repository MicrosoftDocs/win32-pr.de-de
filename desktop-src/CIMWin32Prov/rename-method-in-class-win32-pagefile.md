---
description: Benennt die im Objektpfad angegebene Auslagerungsdatei um.
ms.assetid: 6a98e05f-337e-4224-a847-f01913031b20
ms.tgt_platform: multiple
title: Umbenennen der Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c47bda2b5466111594617a9f3fc0faa9d2dbf55e4452509015cbbe368ef15cba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077430"
---
# <a name="rename-method-of-the-win32_pagefile-class"></a>Rename-Methode der Win32 \_ PageFile-Klasse

Die [Methode WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) umbenennen benennt die im Objektpfad angegebene Auslagerungsdatei um.  Eine Umbenennung wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn das Überschreiben einer vorhandenen logischen Datei erforderlich ist.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* \[ In\]
</dt> <dd>

Vollqualifizierter neuer Name der Datei (oder des Verzeichnisses).

Beispiel: c: \\ temp \\newfile.txt

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich umbenannt wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.

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

Es ist ein Freigabeverstoß aufgetreten.

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

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ PageFile**](win32-pagefile.md)
</dt> </dl>

 

