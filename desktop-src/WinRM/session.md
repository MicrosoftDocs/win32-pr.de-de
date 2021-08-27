---
title: Sitzungsobjekt (WSManDisp.h)
description: Definiert Vorgänge und Sitzungseinstellungen.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Sitzungsobjekt Windows Remoteverwaltung
- Sitzungsobjekt Windows Remoteverwaltung , beschrieben
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b63ce9aa5898f3b6dad716f7af19688059ccf7a3f48901fa73ed3250cd2660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121560"
---
# <a name="session-object-wsmandisph"></a>Sitzungsobjekt (WSManDisp.h)

Definiert Vorgänge und Sitzungseinstellungen. Alle Windows Remoteverwaltungsvorgänge erfordern die  Erstellung einer Sitzung, die eine Verbindung mit einem Remotecomputer, einem Basisverwaltungscontroller (Base [*Management Controller,*](windows-remote-management-glossary.md) BMC) oder dem lokalen Computer herstellt. WinRM-Netzwerkvorgänge umfassen das Abrufen, Schreiben oder Aufzählen von Daten oder das Aufrufen von Methoden. Die Methoden des **Session-Objekts** spiegeln die grundlegenden Vorgänge wider, die im WS-Management definiert sind.

## <a name="members"></a>Member

Das **Session-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Session-Objekt** verfügt über diese Methoden.



| Methode                                 | Beschreibung                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Erstellen**](session-create.md)       | Erstellt eine neue Instanz einer Ressource und gibt den URI des neuen -Objekts zurück.<br/>                                      |
| [**Löschen**](session-delete.md)       | Löscht die im Ressourcen-URI angegebene Ressource.<br/>                                                              |
| [**Aufzählen**](session-enumerate.md) | Enumeriert eine Sammlung, Tabelle oder Nachrichtenprotokollressource.<br/>                                                         |
| [**Erhalten**](session-get.md)             | Ruft eine Ressource aus dem Dienst ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.<br/> |
| [**Identifizieren**](session-identify.md)   | Fragt einen Remotecomputer ab, um zu ermitteln, ob er das WS-Management unterstützt.<br/>                                 |
| [**Invoke**](session-invoke.md)       | Ruft eine Methode auf, die die Ergebnisse des Methodenaufrufs zurückgibt.<br/>                                                    |
| [**Put**](session-put.md)             | Aktualisieren Sie eine Ressource.<br/>                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Das **Session-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp           | Beschreibung                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchItems**](session-batchitems.md)<br/> | Lesen/Schreiben<br/> | Legt die Anzahl der Elemente in jedem Enumerationsbatch fest und ruft sie ab. Dieser Wert kann während einer Enumeration nicht geändert werden. Standardmäßig ist der Standardwert eine unbegrenzte Anzahl von Elementen. Der Ressourcenanbieter kann einen Grenzwert festlegen.<br/> |
| [**Fehler**](session-error.md)<br/>           | Schreibgeschützt<br/>  | Ruft zusätzliche Fehlerinformationen in einem XML-Stream ab.<br/>                                                                                                                                                              |
| [**Timeout**](session-timeout.md)<br/>       | Lesen/Schreiben<br/> | Legt die maximale Wartezeit (in Millisekunden) für die Clientanwendung fest und ruft sie ab.<br/>                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Das **Session-Objekt** entspricht der [**IWSManSession-Schnittstelle.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)

## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel zeigt, wie ein **Session-Objekt erstellt** wird.


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WinRM-Skripterstellungs-API](winrm-scripting-api.md)
</dt> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Skripterstellung in Windows Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> <dt>

[Abrufen von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Abrufen von Daten von einem Remotecomputer](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





