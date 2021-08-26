---
description: Löscht einen Freigabenamen aus der Liste der freigegebenen Ressourcen eines Servers und trennt verbindungen mit der freigegebenen Ressource.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Delete-Methode der Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1331ce9dfa3309c1cfbd0ba0ddc3b4a0c96d431d524d8f0e74f7937c8cdb332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918470"
---
# <a name="delete-method-of-the-win32_share-class"></a>Delete-Methode der Win32 \_ Share-Klasse

Die [Methode WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **löschen** löscht einen Freigabenamen aus der Liste der freigegebenen Ressourcen eines Servers und trennt die Verbindungen mit der freigegebenen Ressource.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

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

**Net Name nicht gefunden** (25)
</dt> <dt>

**Sonstige** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Die **Delete-Methode** ist eine Objektmethode und wird für eine Instanz einer Klasse verwendet.

Nur Mitglieder der lokalen Gruppe "Administratoren" oder "Kontooperatoren" oder Mitglieder der Gruppe "Kommunikation", "Drucken" oder "Serveroperator" können die Methode erfolgreich ausführen. Der Druckeroperator kann nur Druckerwarteschlangen löschen. Der Kommunikationsoperator kann nur Warteschlangen für Kommunikationsgeräte löschen.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird die angegebene Freigabe gelöscht.


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



Im folgenden PowerShell-Codebeispiel werden leere Freigaben gelöscht.


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
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

[**\_Win32-Freigabe**](win32-share.md)
</dt> </dl>

 

