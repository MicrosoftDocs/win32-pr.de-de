---
description: Die Fehler Tabelle wird verwendet, um Formatierungs Vorlagen für Fehlermeldungen zu suchen, wenn Fehler mit einem Fehlercode Satz, aber ohne Formatierungs Vorlagen Satz (normalerweise) verarbeitet werden.
ms.assetid: 3c817468-cba7-46bf-9208-5e6699c02fb6
title: Fehler Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfcba5f68eb48621891c7a48aeedea2329996f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216370"
---
# <a name="error-table"></a>Fehler Tabelle

Die Fehler Tabelle wird verwendet, um Formatierungs Vorlagen für Fehlermeldungen zu suchen, wenn Fehler mit einem Fehlercode Satz, aber ohne Formatierungs Vorlagen Satz (normalerweise) verarbeitet werden.

Die Fehler Tabelle enthält die folgenden Spalten.



| Spalte  | Typ                     | Schlüssel | Nullwerte zulässig |
|---------|--------------------------|-----|----------|
| Fehler   | [Integer](integer.md)   | J   | N        |
| `Message` | [Vorlage](template.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit
</dt> <dd>

Eine Liste der Fehlernummern und Meldungen finden Sie unter [Windows Installer Fehlermeldungen](windows-installer-error-messages.md) .

Die Fehlernummer muss eine nicht negative ganze Zahl sein.

Der Bereich von 25000 bis 30000 ist für Fehler von benutzerdefinierten Aktionen reserviert. Autoren benutzerdefinierter Aktionen können diesen Bereich für benutzerdefinierte Aktionen verwenden.

</dd> <dt>

<span id="Message"></span><span id="message"></span><span id="MESSAGE"></span>Nachricht
</dt> <dd>

Diese Spalte enthält die Vorlage für lokalisierbare Fehler Formatierung. Die Fehler Tabelle wird vom anfänglichen Buildprozess generiert, der die Debug-Formatvorlagen enthält.

In der folgenden Tabelle sind reservierte Nachrichten aufgeführt. Eine Liste der Versand-und internen Fehlercodes finden Sie unter [Windows Installer Fehlermeldungen](windows-installer-error-messages.md).



| Fehler | `Message`                                                    | Bemerkungen                                                                                                                                                                                                      |
|-------|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | {{Schwerwiegender Fehler:}}                                          | Header Präfix für schwerwiegende Fehler (installmessage \_ fatalexit). Text in doppelten geschweiften Klammern {{Text}} ist nur in der Protokolldatei sichtbar. Der Text wird dem Benutzer nicht in der Benutzeroberfläche angezeigt.                  |
| 1     | Fehler \[ 1 \] .                                               | Header Präfix für Fehler (installmessage- \_ Fehler)                                                                                                                                                             |
| 2     | Warnung \[ 1 \] .                                             | Header Präfix für Warnungen (installmessage- \_ Warnung)                                                                                                                                                         |
| 3     |                                                            |                                                                                                                                                                                                              |
| 4     | Informationen \[ 1 \] .                                                | Header Präfix für Informationsmeldungen (installmessage \_ Info)                                                                                                                                              |
| 5     | Interner Fehler \[ 1 \] . \[2 \] {, \[ 3 \] } {, \[ 4 \] }              | Header Präfix für interne Fehler                                                                                                                                                                            |
| 6     |                                                            |                                                                                                                                                                                                              |
| 7     | {{Datenträger voll:}}                                            | Header Präfix für nicht genügend Speicherplatz Fehler (installmessage \_ oudesspace). Text in doppelten geschweiften Klammern {{Text}} ist nur in der Protokolldatei sichtbar. Der Text wird dem Benutzer nicht in der Benutzeroberfläche angezeigt. |
| 8     | Aktions \[ Zeit \] : \[ 1 \] . \[2\]                              |                                                                                                                                                                                                              |
| 9     | \[ProductName\]                                            |                                                                                                                                                                                                              |
| 10    | { \[ 2 \] } {, \[ 3 \] } {, \[ 4 \] }                                  |                                                                                                                                                                                                              |
| 11    | Nachrichtentyp: \[ 1 \] , Argument: \[ 2\]                       |                                                                                                                                                                                                              |
| 12    | = = = Protokollierung gestartet: \[ Datum/ \] \[ Uhrzeit\] ===                 |                                                                                                                                                                                                              |
| 13    | = = = Protokollierung beendet: \[ Datum und \] \[ Uhrzeit\] ===                 |                                                                                                                                                                                                              |
| 14    | Aktions \[ Startzeit \] : \[ 1\]                               |                                                                                                                                                                                                              |
| 15    | Beendigungs \[ Zeit für Aktion \] : \[ 1 \] . Rückgabewert \[ 2\]           |                                                                                                                                                                                                              |
| 16    | Verbleibende Zeit: { \[ 1 \] Min.} { \[ 2 \] Sek.                    |                                                                                                                                                                                                              |
| 17    | Nicht genügend Arbeitsspeicher. Andere Anwendungen vor dem erneuten Versuch Herunterfahren |                                                                                                                                                                                                              |
| 18    | Der Installer antwortet nicht mehr.                          |                                                                                                                                                                                                              |
| 19    | Installer wurde vorzeitig beendet.                           |                                                                                                                                                                                                              |
| 20    | Bitte warten Sie, während " \[ ProductName" konfiguriert wird \] ...    |                                                                                                                                                                                                              |
| 21    | Erforderliche Informationen werden ermittelt...                          |                                                                                                                                                                                                              |
| 22    | Ältere Versionen dieser Anwendung werden entfernt...             |                                                                                                                                                                                                              |
| 23    | Das Entfernen älterer Versionen dieser Anwendung wird vorbereitet...  |                                                                                                                                                                                                              |
| 32    | Das \[ Setup für {ProductName \] } wurde erfolgreich abgeschlossen.            |                                                                                                                                                                                                              |
| 33    | Fehler beim Setup für { \[ ProductName \] }.                            |                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Vorlage enthält keine Formatierung für die Fehlernummer in Feld 1. Bei der Verarbeitung des Fehlers fügt das Installationsprogramm einen Header Präfix an die Vorlage an, abhängig vom Nachrichtentyp. Diese Header werden auch in der Fehler Tabelle gespeichert.

Text in doppelten geschweiften Klammern {{Text}} ist nur in der Protokolldatei sichtbar. Der Text wird dem Benutzer nicht in der Benutzeroberfläche angezeigt.

Sie können eine lokalisierte Fehler Tabelle mithilfe von Msidb.exe oder [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)in die-Datenbank importieren. Das SDK enthält eine lokalisierte Fehler Tabelle für jede der Sprachen, die im Abschnitt [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md) aufgeführt sind. Wenn die Fehler Tabelle nicht aufgefüllt ist, lädt das Installationsprogramm lokalisierte Zeichen folgen für die Sprache, die von der [**productlanguage**](productlanguage.md) -Eigenschaft angegeben wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
</dl>

 

 



