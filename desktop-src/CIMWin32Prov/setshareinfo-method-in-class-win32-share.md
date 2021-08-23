---
description: SetShareInfo&\# 8194; Die WMI-Klassenmethode legt die Parameter einer freigegebenen Ressource fest.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: SetShareInfo-Methode der Win32_Share Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9ee76a0b8336ccdca90a04ee3c2a223b7269a30a00276418d6c46a8bb3abc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800900"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>SetShareInfo-Methode der Win32 \_ Share-Klasse

Die [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** legt die Parameter einer freigegebenen Ressource fest.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MaximumAllowed* \[ in, optional\]
</dt> <dd>

Begrenzen Sie die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.

Beispiel: 10. Dieser Parameter ist optional.

</dd> <dt>

*Beschreibung* \[ in, optional\]
</dt> <dd>

Optionaler Kommentar, um die freigegebene Ressource zu beschreiben.

</dd> <dt>

*Zugriff* \[ in, optional\]
</dt> <dd>

Sicherheitsdeskriptor für Berechtigungen auf Benutzerebene. Ein Sicherheitsdeskriptor enthält Informationen über die Berechtigungs-, Besitzer- und Zugriffsfunktionen der Ressource. Weitere Informationen finden Sie unter [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um auf einen Fehler hindeuten zu können.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

**Ungültiger Name** (9)
</dt> <dt>

**Ungültige Ebene** (10)
</dt> <dt>

**Ungültiger Parameter** (21)
</dt> <dt>

**Doppelte Freigabe** (22)
</dt> <dt>

**Umgeleiteter Pfad** (23)
</dt> <dt>

**Unbekanntes Gerät oder Verzeichnis** (24)
</dt> <dt>

**Net name not found** (25)
</dt> <dt>

**Andere** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

**Die SetShareInfo-Methode** ist eine dynamische Objektmethode und wird bei einem Vorkommen dieser Klasse verwendet.

Nur Mitglieder der lokalen Gruppe Administratoren oder Kontooperatoren oder Mitglieder der Operatorgruppe Communication, Print oder Server können **SetShareInfo erfolgreich ausführen.** Der Druckeroperator kann nur Druckerwarteschlangen festlegen. Der Kommunikationsoperator kann nur Kommunikationsgerätewarteschlangen festlegen.

## <a name="examples"></a>Beispiele

Im folgenden PowerShell-Beispiel wird der Name der **neuen FreigabeFreigabe** aktualisiert.


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a>Anforderungen



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

[**Win32-Freigabe \_**](win32-share.md)
</dt> </dl>

 

