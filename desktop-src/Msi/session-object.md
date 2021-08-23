---
description: Das Sitzungsobjekt steuert den Installationsvorgang.
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: Sitzungsobjekt (Windows Installer)
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
ms.openlocfilehash: 7b02d1f617f7e558acd9c0423dd785c84e0175f195ee0085b2fdc79d66054683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628920"
---
# <a name="session-object-windows-installer"></a>Sitzungsobjekt (Windows Installer)

Das **Sitzungsobjekt** steuert den Installationsvorgang. Daraufhin wird die Installer-Datenbank geöffnet, die die Installationstabellen und -daten enthält. Dieses Objekt ist einem Standardsatz von Aktionsfunktionen zugeordnet, die jeweils bestimmte Vorgänge für Daten aus einer oder mehreren Tabellen ausführen. Für bestimmte Produktinstallationen können zusätzliche benutzerdefinierte Aktionen hinzugefügt werden. Die grundlegende Engine-Funktion ist ein Sequencer, der sequenzielle Datensätze aus einer angegebenen Sequenztabelle abruft, jeden angegebenen Bedingungsausdruck auswertet und die angegebene Aktion ausführt. Aktionen, die von der Engine nicht erkannt werden, werden zur Verarbeitung auf das Benutzeroberflächenhandlerobjekt zurückgestellt, in der Regel Dialogfeldsequenzen.

Beachten Sie, dass nur ein **Sitzungsobjekt** von einem einzelnen Prozess geöffnet werden kann.

## <a name="members"></a>Member

Das **Session-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Session-Objekt** verfügt über diese Methoden.



| Methode                                                 | Beschreibung                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DoAction**](session-doaction.md)                   | Führt die angegebene Aktion aus. <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | Wertet einen logischen Ausdruck aus, der Symbole und Werte enthält, und gibt eine ganze Zahl der Enumeration msiEvaluateConditionErrorEnum zurück.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Gibt ein [**FeatureInfo-Objekt**](featureinfo-object.md) zurück, das beschreibende Informationen für das angegebene Feature enthält.<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | Gibt eine formatierte Zeichenfolge aus Vorlagen- und Datensatzdaten zurück.<br/>                                                                                                                                                                                                      |
| [**`Message`**](session-message.md)                     | Führt alle aktivierten Protokollierungsvorgänge aus und verzieht die Ausführung auf das Benutzeroberflächenhandlerobjekt, das der Engine zugeordnet ist.<br/>                                                                                                                                              |
| [**Sequenz**](session-sequence.md)                   | Öffnet eine Abfrage für die angegebene Tabelle und sortiert die Aktionen nach den Zahlen in der Spalte Sequenz. Für jede abgerufene Zeile wird die [**DoAction-Methode**](session-doaction.md) aufgerufen, vorausgesetzt, jeder angegebene Bedingungsausdruck wird nicht als False ausgewertet.<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | Legt die Installationsebene für die aktuelle Installation auf einen angegebenen Wert fest und berechnet den Status Auswählen und Installiert für alle Features neu.<br/>                                                                                                                    |



 

### <a name="properties"></a>Eigenschaften

Das **Session-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                  | Zugriffstyp           | Beschreibung                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | Gibt ein [**RecordList-Objekt**](recordlist-object.md) zurück, das den Speicherplatz pro Laufwerk auflistet, der für die Installation einer Komponente erforderlich ist.<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | Gibt den aktuellen installierten Zustand der angegebenen Komponente zurück.<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | Ruft eine Änderung des Aktionszustands einer Zeile in der Tabelle Komponente ab oder fordert sie an.<br/>                                                                               |
| [**Datenbank**](session-database.md)<br/>                           |                       | Gibt die Datenbank für die aktuelle Installationssitzung zurück.<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | Gibt die Gesamtmenge des Speicherplatzes (in Einheiten von 512 Bytes) zurück, die für das angegebene Feature und die übergeordneten Features (bis zum Stamm der Featuretabelle) erforderlich sind.<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | Gibt den aktuellen installierten Zustand des angegebenen Features zurück.<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | Lesen/Schreiben<br/> | Ruft eine Änderung des Select-Zustands des Datensatzes und der Unteraufträge eines Features ab oder fordert diese an.<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | Gibt eine ganze Zahl zurück, die Bitflags darstellt, wobei jedes relevante Bit einen gültigen Installationszustand für das angegebene Feature darstellt.<br/>                             |
| [**Installer**](session-installer.md)<br/>                         |                       | Gibt das aktive Installationsprogrammobjekt zurück.<br/>                                                                                                                            |
| [**Sprache (Sitzungsobjekt)**](session-language.md)<br/>          |                       | Stellt den numerischen Sprachbezeichner dar, der von der aktuellen Installationssitzung verwendet wird.<br/>                                                                            |
| [**Mode**](session-mode.md)<br/>                                   |                       | Diese Eigenschaft ist ein Wert, der das angegebene Modusflag für die aktuelle Installationssitzung darstellt.<br/>                                                            |
| [**ProductProperty**](session-productproperty.md)<br/>             |                       | Stellt den Zeichenfolgenwert einer benannten Installereigenschaft dar.<br/>                                                                                                      |
| [**Eigenschaft (Sitzungsobjekt)**](session-session.md)<br/>           | Lesen/Schreiben<br/> | Ruft Produkteigenschaften aus der Produktdatenbank ab.<br/>                                                                                                         |
| [**Sourcepath**](session-sourcepath.md)<br/>                       |                       | Stellt den vollständigen Pfad zum angegebenen Ordner auf dem Quellmedium oder Serverimage bereit.<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | Lesen/Schreiben<br/> | Stellt den vollständigen Pfad zum angegebenen Ordner auf dem Installationsziellaufwerk bereit.<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | Gibt TRUE zurück, wenn genügend Speicherplatz vorhanden ist, und FALSE, wenn der Datenträger voll ist.<br/>                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession ist als 000C109E-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Beispiele für Skripterstellung für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




