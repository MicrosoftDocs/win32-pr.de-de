---
description: Das Sitzungs Objekt steuert den Installationsvorgang.
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: Session-Objekt (Windows Installer)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c391249d5ccc58fe9a947c9db761a77521c9776d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361044"
---
# <a name="session-object-windows-installer"></a>Session-Objekt (Windows Installer)

Das **Sitzungs** Objekt steuert den Installationsvorgang. Die Installer-Datenbank wird geöffnet, in der die Installations Tabellen und Daten enthalten sind. Dieses Objekt ist einem Standardsatz von Aktions Funktionen zugeordnet, die jeweils bestimmte Vorgänge für Daten aus einer oder mehreren Tabellen ausführen. Für bestimmte Produkt Installationen können zusätzliche benutzerdefinierte Aktionen hinzugefügt werden. Bei der grundlegenden Engine-Funktion handelt es sich um einen Sequencer, der sequenzielle Datensätze aus einer bestimmten Sequenz Tabelle abruft, einen angegebenen Bedingungs Ausdruck auswertet und die angegebene Aktion ausführt. Die von der-Engine nicht erkannten Aktionen werden im UI-Handlerobjekt zur Verarbeitung verzögert, normalerweise in Dialogfeld Sequenzen.

Beachten Sie, dass nur ein **Sitzungs** Objekt von einem einzelnen Prozess geöffnet werden kann.

## <a name="members"></a>Member

Das **Sitzungs** Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Sitzungs** Objekt verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DoAction**](session-doaction.md)                   | Führt die angegebene Aktion aus. <br/>                                                                                                                                                                                                                                |
| [**Evaluatecondition**](session-evaluatecondition.md) | Wertet einen logischen Ausdruck aus, der Symbole und Werte enthält, und gibt eine Ganzzahl der Enumeration msievaluateconditionerrorenum zurück.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Gibt ein [**FeatureInfo**](featureinfo-object.md) -Objekt zurück, das beschreibende Informationen für die angegebene Funktion enthält.<br/>                                                                                                                                       |
| [**Formatrecord**](session-formatrecord.md)           | Gibt eine formatierte Zeichenfolge aus Vorlagen-und Daten Satz Daten zurück.<br/>                                                                                                                                                                                                      |
| [**Nachricht**](session-message.md)                     | Führt alle aktivierten Protokollierungs Vorgänge aus und führt die Ausführung für das UI-Handlerobjekt aus, das der Engine zugeordnet ist.<br/>                                                                                                                                              |
| [**Sequenz**](session-sequence.md)                   | Öffnet eine Abfrage für die angegebene Tabelle und ordnet die Aktionen nach den Zahlen in der Sequenz Spalte an. Für jede abgerufene Zeile wird die [**doaction**](session-doaction.md) -Methode aufgerufen, vorausgesetzt, dass ein beliebiger angegebener Bedingungs Ausdruck nicht als false ausgewertet wird.<br/> |
| [**Setinstalllevel**](session-setinstalllevel.md)     | Legt die Installations Ebene für die aktuelle Installation auf einen angegebenen Wert fest und berechnet die SELECT-und install-Zustände für alle Funktionen neu.<br/>                                                                                                                    |



 

### <a name="properties"></a>Eigenschaften

Das **Sitzungs** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                  | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Componentcosts**](session-componentcosts.md)<br/>               |                       | Gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das den für die Installation einer Komponente erforderlichen Speicherplatz pro Laufwerk auflistet.<br/>                                  |
| [**Componentcurrentstate**](session-componentcurrentstate.md)<br/> |                       | Gibt den aktuell installierten Zustand der angegebenen Komponente zurück.<br/>                                                                                                |
| [**Componentrequeststate**](session-componentrequeststate.md)<br/> |                       | Ruft eine Änderung des Aktions Zustands einer Zeile in der Komponenten Tabelle ab oder fordert Sie auf.<br/>                                                                               |
| [**Verbindung**](session-database.md)<br/>                           |                       | Gibt die Datenbank für die aktuelle Installationssitzung zurück.<br/>                                                                                                      |
| [**Featurecost**](session-featurecost.md)<br/>                     |                       | Gibt die Gesamtmenge des Speicherplatzes (in Einheiten von 512 Bytes) zurück, die für die angegebene Funktion und ihre übergeordneten Funktionen (bis zum Stamm der Funktions Tabelle) erforderlich ist.<br/> |
| [**Featurecurrentstate**](session-featurecurrentstate.md)<br/>     |                       | Gibt den aktuell installierten Zustand der angegebenen Funktion zurück.<br/>                                                                                                  |
| [**Featurerequeststate**](session-featurerequeststate.md)<br/>     | Lesen/Schreiben<br/> | Ruft eine Änderung im SELECT-Status des Datensatzes und der untergeordneten Datensätze einer Funktion ab oder fordert Sie an.<br/>                                                                          |
| [**Featurevalidstates**](session-featurevalidstates.md)<br/>       |                       | Gibt eine ganze Zahl zurück, die Bitflags mit jedem relevanten Bit darstellt, das einen gültigen Installations Zustand für das angegebene Feature darstellt.<br/>                             |
| [**Installationsprogramm**](session-installer.md)<br/>                         |                       | Gibt das aktive Installer-Objekt zurück.<br/>                                                                                                                            |
| [**Sprache (Sitzungs Objekt)**](session-language.md)<br/>          |                       | Stellt den numerischen sprach Bezeichner dar, der von der aktuellen Installationssitzung verwendet wird.<br/>                                                                            |
| [**Mode**](session-mode.md)<br/>                                   |                       | Diese Eigenschaft ist ein Wert, der das Flag für den vorgesehenen Modus für die aktuelle Installationssitzung darstellt.<br/>                                                            |
| [**Productproperty**](session-productproperty.md)<br/>             |                       | Stellt den Zeichen folgen Wert einer benannten installereigenschaft dar.<br/>                                                                                                      |
| [**Property (Session-Objekt)**](session-session.md)<br/>           | Lesen/Schreiben<br/> | Ruft Produkteigenschaften aus der Produktdatenbank ab.<br/>                                                                                                         |
| [**SourcePath**](session-sourcepath.md)<br/>                       |                       | Stellt den vollständigen Pfad zum angegebenen Ordner auf dem Quell Medium oder dem Server Image bereit.<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | Lesen/Schreiben<br/> | Gibt den vollständigen Pfad zum angegebenen Ordner auf dem Installationsziel Laufwerk an.<br/>                                                                               |
| [**Verifydiskspace**](session-verifydiskspace.md)<br/>             |                       | Gibt true zurück, wenn ausreichend Speicherplatz vorhanden ist, und false, wenn der Datenträger voll ist.<br/>                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




