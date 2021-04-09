---
title: Session-Objekt (WSManDisp. h)
description: Definiert Vorgänge und Sitzungs Einstellungen.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Sitzungs Objekt Windows-Remoteverwaltung
- Sitzungs Objekt Windows-Remoteverwaltung, beschrieben
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
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957220"
---
# <a name="session-object-wsmandisph"></a>Session-Objekt (WSManDisp. h)

Definiert Vorgänge und Sitzungs Einstellungen. Alle Windows-Remoteverwaltung Vorgänge erfordern das Erstellen einer **Sitzung** , die eine Verbindung mit einem Remote Computer, einem [*Base Management Controller*](windows-remote-management-glossary.md) (BMC) oder dem lokalen Computer herstellt. WinRM-Netzwerk Vorgänge umfassen das aufrufen, schreiben, Auflisten von Daten oder das Aufrufen von Methoden. Die Methoden des **Session** -Objekts spiegeln die grundlegenden Vorgänge wider, die im WS-Management-Protokoll definiert sind.

## <a name="members"></a>Member

Das **Sitzungs** Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Sitzungs** Objekt verfügt über diese Methoden.



| Methode                                 | BESCHREIBUNG                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Stelle**](session-create.md)       | Erstellt eine neue Instanz einer Ressource und gibt den URI des neuen-Objekts zurück.<br/>                                      |
| [**Lösch**](session-delete.md)       | Löscht die im Ressourcen-URI angegebene Ressource.<br/>                                                              |
| [**Aufzählen**](session-enumerate.md) | Listet eine Auflistung, eine Tabelle oder eine Nachrichtenprotokoll Ressource auf.<br/>                                                         |
| [**Erhalten**](session-get.md)             | Ruft eine Ressource vom Dienst ab und gibt eine XML-Darstellung der aktuellen Instanz der Ressource zurück.<br/> |
| [**Identifizieren**](session-identify.md)   | Fragt einen Remote Computer ab, um zu bestimmen, ob das WS-Management Protokoll unterstützt wird.<br/>                                 |
| [**Invoke**](session-invoke.md)       | Ruft eine Methode auf, die die Ergebnisse des Methoden Aufrufes zurückgibt.<br/>                                                    |
| [**Stellte**](session-put.md)             | Aktualisieren Sie eine Ressource.<br/>                                                                                              |



 

### <a name="properties"></a>Eigenschaften

Das **Sitzungs** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Batchitems**](session-batchitems.md)<br/> | Lesen/Schreiben<br/> | Legt die Anzahl der Elemente in jedem enumerationsbatch fest und ruft Sie ab. Dieser Wert kann während einer Enumeration nicht geändert werden. Standardmäßig ist der Standardwert eine unbegrenzte Anzahl von Elementen. Der Ressourcenanbieter kann ein Limit festlegen.<br/> |
| [**Fehler**](session-error.md)<br/>           | Schreibgeschützt<br/>  | Ruft zusätzliche Fehlerinformationen in einem XML-Stream ab.<br/>                                                                                                                                                              |
| [**Timeout**](session-timeout.md)<br/>       | Lesen/Schreiben<br/> | Legt die maximale Zeitspanne (in Millisekunden) fest, die die Client Anwendung wartet, und ruft Sie ab.<br/>                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Das **Sitzungs** Objekt entspricht der [**iwsmansession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) -Schnittstelle.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird gezeigt, wie ein **Sitzungs** Objekt erstellt wird.


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

 

 





