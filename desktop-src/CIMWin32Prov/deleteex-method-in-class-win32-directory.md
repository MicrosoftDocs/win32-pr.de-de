---
description: Die DeleteEx-WMI-Klassenmethode löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. DeleteEx ist eine erweiterte Version der Delete-Methode.
ms.assetid: 6e5447c1-4d71-4a51-a1e0-b5785c13dfd2
ms.tgt_platform: multiple
title: DeleteEx-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0725011b39628f5376293bc82273723a89dfb0eafe1535d2f58393919f18c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080064"
---
# <a name="deleteex-method-of-the-win32_directory-class"></a>DeleteEx-Methode der Win32 \_ Directory-Klasse

Die  [DeleteEx-WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) löscht die logische Datei (oder das Verzeichnis), die im Objektpfad angegeben ist. **DeleteEx** ist eine erweiterte Version der [**Delete-Methode.**](delete-method-in-class-win32-directory.md)

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Name der Datei oder des Verzeichnisses, in der die **DeleteEx-Methode** fehlgeschlagen ist. Dieser Parameter ist **NULL,** wenn die Methode erfolgreich ist.

</dd> <dt>

*StartFileName* \[ in, optional\]
</dt> <dd>

Benennt die untergeordnete Datei oder das untergeordnete Verzeichnis, die bzw. das als Ausgangspunkt für **DeleteEx** verwendet werden soll. Der *StartFileName-Parameter* ist in der Regel der *StopFileName-Parameter,* der die Datei oder das Verzeichnis angibt, bei der beim vorherigen Methodenaufruf ein Fehler aufgetreten ist. Wenn dieser Parameter **NULL** ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, die bzw. das im ExecMethod-Aufruf angegeben ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und eine beliebige andere Zahl, um einen Fehler anzugeben.

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

[**\_Win32-Verzeichnis**](win32-directory.md)
</dt> </dl>

 

