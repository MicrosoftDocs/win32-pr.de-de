---
description: WMI verfügt über Objekte und Methoden, mit denen Sie Sicherheits Deskriptoren lesen und bearbeiten können, um zu bestimmen, wer Zugriff auf Sicherungs fähige Objekte hat.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: WMI-sicherheitsdeskriptorobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564422"
---
# <a name="wmi-security-descriptor-objects"></a>WMI-sicherheitsdeskriptorobjekte

WMI verfügt über Objekte und Methoden, mit denen Sie Sicherheits Deskriptoren lesen und bearbeiten können, um zu bestimmen, wer Zugriff auf Sicherungs fähige Objekte hat.

-   [Die Rolle der Sicherheits Deskriptoren](#the-role-of-security-descriptors)
-   [Access Control und WMI-Sicherheits Objekte](#access-control-and-wmi-security-objects)
-   [Win32 \_ securityDescriptor-Objekt](/windows)
-   [DACL und SACL](#dacl-and-sacl)
-   [Win32- \_ ACE, Win32- \_ Treuhänder, Win32- \_ sid](/windows)
-   [Beispiel: überprüfen, wer Zugriff auf Drucker hat](#example-checking-who-has-access-to-printers)
-   [Zugehörige Themen](#related-topics)

## <a name="the-role-of-security-descriptors"></a>Die Rolle der Sicherheits Deskriptoren

Sicherheits Deskriptoren definieren die Sicherheits Attribute von Sicherungs fähigen Objekten wie Dateien, Registrierungs Schlüsseln, WMI-Namespaces, Druckern, Diensten oder Freigaben. Eine Sicherheits Beschreibung enthält Informationen zum Besitzer und zur primären Gruppe eines Objekts. Ein Anbieter kann die Ressourcen Sicherheits Beschreibung mit der Identität eines anfordernden Benutzers vergleichen und ermitteln, ob der Benutzer über die Berechtigung zum Zugriff auf die Ressource verfügt, die ein Benutzer anfordert. Weitere Informationen finden Sie unter [Zugriff auf Sicherungs fähige WMI-Objekte](access-to-wmi-securable-objects.md).

Einige WMI-Methoden, wie z. [**b. gezd**](--systemsecurity-getsd.md), geben eine Sicherheits Beschreibung im binären Byte Array Format zurück. Beginnend mit Windows Vista verwenden Sie die Methoden der [**Win32 \_ securitydescriptorhelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) -Klasse, um eine binäre Sicherheits Beschreibung in eine Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)zu konvertieren, die einfacher bearbeitet werden kann. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

## <a name="access-control-and-wmi-security-objects"></a>Access Control und WMI-Sicherheits Objekte

Im folgenden finden Sie eine Liste von WMI-Sicherheits Objekten:

-   [**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [**Win32- \_ Treuhänder**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [**Win32- \_ sid**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

Das folgende Diagramm zeigt die Beziehungen zwischen WMI-Sicherheits Objekten.

![Beziehungen zwischen WMI-Sicherheits Objekten](images/security-descriptor.png)

Weitere Informationen zur Rolle der Zugriffssicherheit finden Sie unter [Bewährte Sicherheitsmethoden](/windows/desktop/SecBP/best-practices-for-the-security-apis), Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md)und [Access Control](/windows/desktop/SecAuthZ/access-control).

## <a name="win32_securitydescriptor-object"></a>Win32 \_ securityDescriptor-Objekt

In der folgenden Tabelle sind die Win32-Eigenschaften der [**\_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse aufgelistet.



| Eigenschaft         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ControlFlags** | Ein Satz von Steuerungs Bits, die die Bedeutung einer SD oder ihrer einzelnen Member qualifizieren. Weitere Informationen zum Festlegen der **ControlFlags** -Bitwerte finden Sie [**unter \_ Win32 securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).<br/>                                                                                                                                                                      |
| **DACL**         | Eine freigegebene [Access Control Liste (ACL)](/windows/desktop/SecAuthZ/access-control-lists) von Benutzern und Gruppen sowie deren Zugriffsrechte für ein gesichertes Objekt. Diese Eigenschaft enthält ein Array von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Instanzen, die [Access Control Einträge](/windows/desktop/SecAuthZ/access-control-entries)darstellen. Weitere Informationen finden Sie unter [Erstellen einer DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).<br/> |
| **Gruppieren**        | Die Gruppe, zu der dieses gesicherte Objekt gehört. Diese Eigenschaft enthält eine Instanz des [**Win32- \_ Treuhänders**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , die den Namen, die Domäne und die Sicherheits-ID (SID) der Gruppe enthält, zu der der Besitzer gehört.<br/>                                                                                                                                                             |
| **Besitzer**        | Besitzer dieses gesicherten Objekts. Diese Eigenschaft enthält eine Instanz des [Win32- \_ Treuhänders](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , die den Namen, die Domäne und die Sicherheits-ID (SID) des Besitzers enthält.<br/>                                                                                                                                                                                                          |
| **SACL**         | Die [System Access Control Liste (ACL)](/windows/desktop/SecAuthZ/access-control-lists) enthält ein Array von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Instanzen, die den Typ der Zugriffsversuche darstellen, die Überwachungsdaten Sätze für Benutzer oder Gruppen generieren. Weitere Informationen finden Sie unter [SACL für ein neues Objekt](/windows/desktop/SecAuthZ/sacl-for-a-new-object).<br/>                                                                        |



 

## <a name="dacl-and-sacl"></a>DACL und SACL

Die Arrays von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Objekten in der freigegebenen Zugriffs Steuerungs Liste (DACL) und der System Zugriffs Steuerungs Liste {SACL) erstellen eine Verknüpfung zwischen einem Benutzer oder einer Gruppe und Ihren Zugriffsrechten.

Wenn eine DACL-Eigenschaft keinen Zugriffs Steuerungs Eintrag (Access Control Entry, ACE) enthält, werden keine Zugriffsrechte erteilt, und der Zugriff auf das Objekt wird verweigert.

> [!Note]  
> Eine **null** -DACL bietet vollständigen Zugriff auf alle, was ein schwerwiegendes Sicherheitsrisiko darstellt. Weitere Informationen finden Sie unter [Erstellen einer DACL](/windows/desktop/SecBP/creating-a-dacl).

 

## <a name="win32_ace-win32_trustee-win32_sid"></a>Win32- \_ ACE, Win32- \_ Treuhänder, Win32- \_ sid

Ein [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Objekt enthält eine Instanz der Win32-Vertrauens nehmer Klasse, die einen Benutzer oder eine Gruppe identifiziert, und eine **AccessMask** -Eigenschaft, bei der es sich um eine Bitmaske handelt, die angibt, welche Aktionen ein Benutzer oder eine Gruppe ausführen kann. [**\_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) Beispielsweise kann einem Benutzer oder einer Gruppe das Recht erteilt werden, eine Datei zu lesen, aber nicht in die Datei zu schreiben. Ein **Win32- \_ ACE** -Objekt enthält auch einen ACE, der angibt, ob es sich um einen Zulassungs-oder Verweigerungs Zugriff handelt.

> [!Note]  
> Die [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Reihenfolge in einer DACL ist wichtig, da sowohl der Allow-als auch der Deny-Zugriffs Steuerungs Eintrag (ACE) in einer DACL zulässig sind. Weitere Informationen finden Sie unter [Reihenfolge von ACEs in einer DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Jedes Benutzerkonto oder jede Gruppe, das durch einen [**Win32- \_ Treuhänder**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) repräsentiert wird, verfügt über eine Sicherheits-ID (SID), die ein Konto eindeutig identifiziert, und gibt die Zugriffsrechte des Kontos an. Wie Sie die SID-Daten angeben, hängt vom Betriebssystem ab. Weitere Informationen finden Sie unter [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).

Das folgende Diagramm zeigt den Inhalt einer [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Instanz.

![Inhalt einer Win32- \- ACE-Instanz](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a>Beispiel: überprüfen, wer Zugriff auf Drucker hat

Im folgenden VBScript-Codebeispiel wird gezeigt, wie die Sicherheits Beschreibung des Druckers verwendet wird. Das Skript ruft die [**getsecuritydescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) -Methode in der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse auf, um den Deskriptor abzurufen, und bestimmt dann, ob eine freigegebene Access Control Liste (DACL) in der Sicherheits Beschreibung vorhanden ist. Wenn eine DACL vorhanden ist, erhält das Skript die Liste der Access Control Einträge (ACE) aus der DACL. Jeder ACE wird durch eine Instanz von [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)dargestellt. Das Skript prüft jeden ACE, um den Namen des Benutzers zu erhalten, und bestimmt, ob der Benutzer Zugriff auf den Drucker hat. Der Benutzer wird in durch eine Instanz des Win32-Vertrauens nehmers dargestellt, der in die **Win32- \_ ACE** -Instanz eingebettet ist. [**\_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md)
</dt> <dt>

[Hilfsklasse für Sicherheits Deskriptoren](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Bewährte Sicherheitsmethoden](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Zugriffssteuerung](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Zugriff auf WMI-Namespaces](access-to-wmi-namespaces.md)
</dt> </dl>

 

