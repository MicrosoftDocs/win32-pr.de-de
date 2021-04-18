---
description: Der setshareingefo-&\# 8194; WMI-Klassenmethode legt die Parameter einer freigegebenen Ressource fest.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Setshareingefo-Methode der Win32_Share-Klasse
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
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214295"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Setshareingefo-Methode der Win32- \_ Freigabe Klasse

Die **setshareinfo** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode legt die Parameter einer freigegebenen Ressource fest.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

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

Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.

Beispiel: 10. Dieser Parameter ist optional.

</dd> <dt>

*Beschreibung* \[ in, optional\]
</dt> <dd>

Optionaler Kommentar zum Beschreiben der freigegebenen Ressource.

</dd> <dt>

*Zugriff* \[ in, optional\]
</dt> <dd>

Sicherheits Beschreibung für Berechtigungen auf Benutzerebene. Eine Sicherheits Beschreibung enthält Informationen zu den Berechtigungen, den Besitzern und den Zugriffs Funktionen der Ressource. Weitere Informationen finden Sie unter [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.

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

Der **Netzwerkname wurde nicht gefunden** (25).
</dt> <dt>

**Sonstige** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Die **setshareinfo** -Methode ist eine dynamische Objektmethode und wird bei einem Vorkommen dieser Klasse verwendet.

Nur Mitglieder der lokalen Gruppe "Administratoren" oder "Konto Operatoren" oder die Gruppenmitgliedschaften "Kommunikation", "Drucken" oder "Server Operator" können " **setshareinfo**" erfolgreich ausführen Der Druck Operator kann nur Drucker Warteschlangen festlegen. Der Kommunikations Operator kann nur Warteschlangen für Kommunikationsgeräte festlegen.

## <a name="examples"></a>Beispiele

Im folgenden PowerShell-Beispiel wird der Name der **NewShare** -Freigabe aktualisiert.


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
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

[**Win32- \_ Freigabe**](win32-share.md)
</dt> </dl>

 

