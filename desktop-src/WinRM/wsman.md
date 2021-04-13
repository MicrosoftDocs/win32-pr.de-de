---
title: WSMAN-Objekt (WSManDisp. h)
description: Stellt Methoden und Eigenschaften bereit, mit denen eine Sitzung erstellt wird, die durch ein Sitzungs Objekt dargestellt wird.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- WSMAN-Objekt Windows-Remoteverwaltung
- WSMAN-Objekt Windows-Remoteverwaltung, beschrieben
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
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391584"
---
# <a name="wsman-object"></a>WSMAN-Objekt

Stellt Methoden und Eigenschaften bereit, mit denen eine Sitzung erstellt wird, die durch ein [**Sitzungs**](session.md) Objekt dargestellt wird. Alle Windows-Remoteverwaltung Vorgänge erfordern das Erstellen einer [**Sitzung**](session.md) , die eine Verbindung mit einem Remote Computer, einem [*Base Management Controller*](windows-remote-management-glossary.md) (BMC) oder dem lokalen Computer herstellt. Zu den Vorgängen gehören das Erstellen, schreiben, Auflisten von Daten oder das Aufrufen von Methoden.

## <a name="members"></a>Member

Das **WSMAN** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **WSMAN** -Objekt verfügt über diese Methoden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Methode</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createconnectionoptions.md"><strong>"Kreateconnectionoptions"</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> -Objekt, das den Benutzernamen und das Kennwort angibt, die beim Erstellen einer Remote Sitzung verwendet werden.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-createresourcelocator.md"><strong>"Kreateresourcelocator"</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> -Objekt, das Folgendes angeben kann:<br/>
<ul>
<li>Der gesamte Pfad zu einer <a href="windows-remote-management-glossary.md"><em>Ressource</em></a> oder einem einzelnen Datenelement.</li>
<li>Eine <a href="windows-remote-management-glossary.md"><em>Auswahl</em></a> für eine bestimmte Instanz einer Ressource.</li>
<li>Eine <a href="windows-remote-management-glossary.md"><em>Option</em></a> , die dem Ressourcenanbieter zusätzliche Daten bereitstellt.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></td>
<td style="text-align: left;">Erstellt ein <a href="session.md"><strong>Sitzungs</strong></a> Objekt, das dann für nachfolgende Netzwerk Vorgänge verwendet werden kann.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMAN. enumerationflaghierarchydeep</strong></a></td>
<td style="text-align: left;">Gibt den Wert des <strong>Enumerationsflags enumerationflaghierarchydeep</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>zurück.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMAN. enumerationflaghierarchydeepbasepropsonly</strong></a></td>
<td style="text-align: left;">Gibt den Wert des <strong>Enumerationsflags enumerationflaghierarchydeepbasepropsonly</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMAN. enumerationflaghierarchyflache</strong></a></td>
<td style="text-align: left;">Gibt den Wert des <strong>Enumerationsflags enumerationflaghierarchyflache</strong> zurück, der im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>verwendet werden soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMAN. enumerationflagnonxmltext</strong></a></td>
<td style="text-align: left;">Gibt den Wert der Enumerationskonstante <strong>wsmanflagnonxmltext</strong> zurück, der im <em>Flags</em> -Parameter der <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a> -Methode verwendet werden soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMAN. enumerationflagreturnetpr</strong></a></td>
<td style="text-align: left;">Gibt den Wert des <strong>Enumerationsflags enumerationflagreturnetpr</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>zurück.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMAN. enumerationflagreturnobject</strong></a></td>
<td style="text-align: left;">Gibt den Wert des <strong>Enumerationsflags enumerationflagreturnobject</strong> zurück, das im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>verwendet werden soll.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMAN. enumerationflagreturnobjectandepr</strong></a></td>
<td style="text-align: left;">Gibt den Wert des <strong>Enumerationsflags enumerationflagreturnobjectandepr</strong> zurück, der im <em>Flags</em> -Parameter von <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>verwendet werden soll.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-geterrormessage.md"><strong>WSMAN. getErrorMessage</strong></a></td>
<td style="text-align: left;">Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMAN. sessionflagkredusernamepassword</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagkredusernamepassword</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMAN. sessionflagenablespnserverport</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagenablespnserverport</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagnoencryption.md"><strong>WSMAN. sessionflagnoencryption</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagnoencryption</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMAN. sessionflagskipcacheck</strong></a></td>
<td style="text-align: left;">Gibt den Wert des <strong>wsmanflagskipcacheck</strong> -Authentifizierungsflags für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMAN. sessionflagskipcncheck</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagskipcncheck</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusebasic.md"><strong>WSMAN. sessionflagusebasic</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusebasic</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusedigest.md"><strong>WSMAN. sessionflagusedigest</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusedigest</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusekerberos.md"><strong>WSMAN. sessionflagusekerberos</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusekerberos</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMAN. sessionflagusenegotiate</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusenegotiate</strong> zur Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMAN. sessionflagusenoauthentication</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>wsmanflagusenoauthentication</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagutf8.md"><strong>WSMAN. SessionFlagUTF8</strong></a></td>
<td style="text-align: left;">Gibt den Wert des Authentifizierungsflags <strong>WSManFlagUTF8</strong> für die Verwendung im <em>Flags</em> -Parameter von <a href="wsman-createsession.md"><strong>WSMAN. kreatesession</strong></a>zurück.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Eigenschaften

Das **WSMAN** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp          | BESCHREIBUNG                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**CommandLine**](wsman-commandline.md)<br/> | Schreibgeschützt<br/> | Ruft die nicht verarbeitete Befehlszeile für den aktuellen Hostingprozess ab.<br/> |
| [**Fehler**](wsman-error.md)<br/>             | Schreibgeschützt<br/> | Ruft Fehlerinformationen ab.<br/>                                            |



 

## <a name="remarks"></a>Bemerkungen

Das **WSMAN** -Objekt entspricht den [**iwsman**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) -und [**iwsmanex**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) -Schnittstellen. **WSMAN** ist das einzige Objekt, das [direkt mithilfe von](/previous-versions//xzysf6hc(v=vs.85))"" erstellt werden kann.

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie ein **WSMAN** -Objekt instanziiert wird.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinRM-Skript-API](winrm-scripting-api.md)
</dt> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Skripterstellung in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> <dt>

[Abrufen von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Abrufen von Daten von einem Remote Computer](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

