---
title: WSMan-Objekt (WSManDisp.h)
description: Stellt Methoden und Eigenschaften bereit, die zum Erstellen einer Sitzung verwendet werden, die durch ein Session-Objekt dargestellt wird.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- WSMan-Objekt Windows Remoteverwaltung
- WSMan-Objekt Windows Remoteverwaltung , beschrieben
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dac26be22118a320848ea227643f9c4d3857dc01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475966"
---
# <a name="wsman-object"></a>WSMan-Objekt

Stellt Methoden und Eigenschaften bereit, die zum Erstellen einer Sitzung verwendet werden, die durch ein [**Session-Objekt**](session.md) dargestellt wird. Alle Windows Remoteverwaltungsvorgänge erfordern die Erstellung einer [**Sitzung,**](session.md) die eine Verbindung mit einem Remotecomputer, [*einem Basisverwaltungscontroller (Base Management Controller,*](windows-remote-management-glossary.md) BMC) oder dem lokalen Computer herstellt. Vorgänge umfassen das Abrufen, Schreiben, Aufzählen von Daten oder Aufrufen von Methoden.

## <a name="members"></a>Member

Das **WSMan-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **WSMan-Objekt** verfügt über diese Methoden.




| Methode | BESCHREIBUNG | 
|--------|-------------|
| <a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a> | Erstellt ein <a href="connectionoptions.md"><strong>ConnectionOptions-Objekt,</strong></a> das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Remotesitzung verwendet werden.<br /> | 
| <a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a> | Erstellt ein <a href="resourcelocator.md"><strong>ResourceLocator-Objekt,</strong></a> das Folgendes angeben kann:<br /><ul><li>Der vollständige Pfad zu einer <a href="windows-remote-management-glossary.md"><em>Ressource</em></a> oder einem einzelnen Datenteil.</li><li>Ein <a href="windows-remote-management-glossary.md"><em>Selektor</em></a> für eine bestimmte Instanz einer Ressource.</li><li>Eine <a href="windows-remote-management-glossary.md"><em>Option,</em></a> die dem Ressourcenanbieter zusätzliche Daten zur Verfügung stellt.</li></ul> | 
| <a href="wsman-createsession.md"><strong>CreateSession</strong></a> | Erstellt ein <a href="session.md"><strong>Session-Objekt,</strong></a> das dann für nachfolgende Netzwerkvorgänge verwendet werden kann.<br /> | 
| <a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a> | Gibt den Wert des Enumerationsflags <strong>EnumerationFlagHierarchyDeep</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>zurück.<br /> | 
| <a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a> | Gibt den Wert des <strong>EnumerationsflagHierarchyDeepBasePropsOnly</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>zurück.<br /> | 
| <a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a> | Gibt den Wert des Enumerationsflags <strong>EnumerationFlagHierarchyShallow</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>zurück.<br /> | 
| <a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a> | Gibt den Wert der Enumerationskonstante <strong>WSManFlagNonXmlText</strong> für die Verwendung im <em>flags-Parameter</em> der <a href="session-enumerate.md"><strong>Session.Enumerate-Methode</strong></a> zurück.<br /> | 
| <a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a> | Gibt den Wert des Enumerationsflags <strong>EnumerationFlagReturnEPR</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>zurück.<br /> | 
| <a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a> | Gibt den Wert des <strong>EnumerationFlagReturnObject-EnumerationFlag-Flags</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>zurück.<br /> | 
| <a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a> | Gibt den Wert des <strong>EnumerationsflagReturnObjectAndEPR</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>zurück.<br /> | 
| <a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a> | Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält.<br /> | 
| <a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagCredUsernamePassword</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagEnableSPNServerPort</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagNoEncryption</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a> | Gibt den Wert des <strong>WSManFlagSkipCACheck-Authentifizierungsflags</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagSkipCNCheck</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagUseBasic</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagUseDigest</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagUseKerberos</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagUseNegotiate</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagUseNoAuthentication</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 
| <a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a> | Gibt den Wert des Authentifizierungsflags <strong>WSManFlagUTF8</strong> für die Verwendung im <em>flags-Parameter</em> von <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>zurück.<br /> | 




 

### <a name="properties"></a>Eigenschaften

Das **WSMan-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | BESCHREIBUNG                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**Commandline**](wsman-commandline.md)<br/> | Schreibgeschützt<br/> | Ruft die nicht verarbeitete Befehlszeile für den aktuellen Hostingprozess ab.<br/> |
| [**Fehler**](wsman-error.md)<br/>             | Schreibgeschützt<br/> | Ruft Fehlerinformationen ab.<br/>                                            |



 

## <a name="remarks"></a>Hinweise

Das **WSMan-Objekt** entspricht den [**Schnittstellen IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) und [**IWSManEx.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) **WSMan** ist das einzige Objekt, das direkt mit [CreateObject](/previous-versions//xzysf6hc(v=vs.85))erstellt werden kann.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie ein **WSMan-Objekt** instanziiert wird.


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WinRM-Skript-API](winrm-scripting-api.md)
</dt> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden der Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Skripterstellung in Windows Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> <dt>

[Abrufen von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Abrufen von Daten von einem Remotecomputer](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

