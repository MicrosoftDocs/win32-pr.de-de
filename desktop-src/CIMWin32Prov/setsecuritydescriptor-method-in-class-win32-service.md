---
description: Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Dienst steuert.
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: SETSECURITYDESCRIPTOR-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82c08f9c560a1d8e419d9a8f6474f8ea9db4e541
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340131"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>SETSECURITYDESCRIPTOR-Methode der Win32_Service-Klasse (cimwin32-WMI-Anbieter)

Die **SETSECURITYDESCRIPTOR** -Methode schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Dienst steuert.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deskriptor* \[ in\]
</dt> <dd>

Die Sicherheits Beschreibung, die dem Dienst zugeordnet ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Die Anforderung wurde akzeptiert.

</dd> <dt>

**1**
</dt> <dd>

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.

</dd> <dt>

**3**
</dt> <dd>

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**4**
</dt> <dd>

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**5**
</dt> <dd>

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.

</dd> <dt>

**6**
</dt> <dd>

Der Dienst wurde nicht gestartet.

</dd> <dt>

**7**
</dt> <dd>

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

8

Unbekannter Fehler beim Starten des Dienstanbieter.

</dd> <dt>

**Fehlende Berechtigungen**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

</dd> <dt>

**10**
</dt> <dd>

Der Dienst wird schon ausgeführt.

</dd> <dt>

**11**
</dt> <dd>

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**12**
</dt> <dd>

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

</dd> <dt>

**13**
</dt> <dd>

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**14**
</dt> <dd>

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**15**
</dt> <dd>

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**16**
</dt> <dd>

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**17**
</dt> <dd>

Der Dienst hat keinen Ausführungs Thread.

</dd> <dt>

**Jahren**
</dt> <dd>

Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter dem gleichen Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienst Name enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Parameter**
</dt> <dd>

21

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>

**22**
</dt> <dd>

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

</dd> <dt>

**23**
</dt> <dd>

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**24**
</dt> <dd>

Der Dienst ist im System derzeitig angehalten.

</dd> <dt>

**Andere**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz stellt einen Datentyp für die [**Sicherheits \_ \_ deskriptorsteuerung**](/windows/desktop/SecAuthZ/security-descriptor-control) dar und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) und eine [*System Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL). Weitere Informationen finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists).

Wenn **SeSecurityPrivilege** beim erhalten einer Sicherheits Beschreibung nicht gewährt oder aktiviert ist, wird nur die DACL in der zurückgegebenen Sicherheits Beschreibung zurückgegeben. Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants) und [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).

Wenn Sie diese Methode aufrufen, können Sie sowohl die DACL als auch die SACL in der [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Instanz aktualisieren, aber Sie können auch nur die DACL oder nur die SACL aktualisieren.

Die folgenden Werte im [**\_ \_ sicherheitsdeskriptorsteuerelement**](/windows/desktop/SecAuthZ/security-descriptor-control) bestimmen, ob die DACL, die SACL oder beides aktualisiert wird.

-   **SE \_ DACL \_ vorhanden**

    Gibt an, dass die DACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der DACL bei.

-   **SE \_ SACL \_ vorhanden**

    Gibt an, dass die SACL aktualisiert werden soll. Wenn dies nicht festgelegt ist, behält WMI den ursprünglichen Wert der SACL bei. Zum Aktualisieren der SACL muss für das Konto die Berechtigung " **SeSecurityPrivilege** " aktiviert sein. Bei der Skripterstellung lautet der Berechtigungs Name " **SeSecurityPrivilege**". Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants).

Wenn die Eigenschaften des Gruppen Vertrauens nehmers und des Besitzer Treuhänders nicht **null** sind, werden Sie aktualisiert. Andernfalls behält WMI die ursprünglichen Werte bei. Weitere Informationen finden Sie unter [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).

Wenn eine neue SACL in einem Aufruf dieser Methode **null** ist, bleibt die SACL der Sicherheits Beschreibung für das Sicherungs fähige Zielobjekt unverändert.

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

[**Win32- \_ Dienst**](win32-service.md)
</dt> <dt>

[**Berechtigungs Konstanten**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI-sicherheitsdeskriptorobjekte](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

