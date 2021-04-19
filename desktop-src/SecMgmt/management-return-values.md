---
description: Listet die Werte auf, die von Sicherheits Verwaltungsfunktionen zurückgegeben werden.
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: Rückgabewerte der Sicherheitsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2c67b79d03896960f7eb9a8631e1cd268284e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356973"
---
# <a name="security-management-return-values"></a>Rückgabewerte der Sicherheitsverwaltung

Die Rückgabewerte der Sicherheitsverwaltung umfassen Folgendes:

-   [Anlagen Rückgabewerte](#attachment-return-values)
-   [Rückgabewerte der LSA-Richtlinien Funktion](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>Anlagen Rückgabewerte

Das Sicherheitskonfigurations-Toolset unterstützt die folgenden **scestatus** -Rückgabecodes. Diese Werte werden von den Unterstützungsfunktionen der Anlage und den Funktionen zurückgegeben, die beim Schreiben einer Anlagen-Engine oder eines Snap-Ins implementiert werden.



| Wert                            | BESCHREIBUNG                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| scestatus- \_ Erfolg               | Die Funktion wurde erfolgreich ausgeführt.                                                                          |
| Ungültiger scestatus- \_ \_ Parameter    | Einer der Parameter, die an die Funktion übertragen wurden, war ungültig.                                      |
| scestatus- \_ Datensatz wurde \_ nicht \_ gefunden.    | Der angegebene Datensatz wurde in der Sicherheitsdatenbank nicht gefunden.                                     |
| scestatus \_ ungültige \_ Daten         | Die Funktion ist fehlgeschlagen, weil einige Daten ungültig waren.                                             |
| scestatus- \_ Objekt ist \_ vorhanden.        | Das Objekt ist bereits vorhanden.                                                                       |
| scestatus- \_ Puffer \_ zu \_ klein    | Der Puffer, der an die Funktion zum Empfangen von Daten übermittelt wird, ist nicht groß genug, um alle Daten zu empfangen. |
| scestatus- \_ Profil wurde \_ nicht \_ gefunden.   | Das angegebene Profil wurde nicht gefunden.                                                             |
| scestatus-fehlerhaftes \_ \_ Format           | Das Format ist ungültig.                                                                         |
| scestatus \_ nicht \_ ausreichend \_ Ressource | Es ist nicht genügend Arbeitsspeicher vorhanden.                                                                    |
| scestatus- \_ Zugriff \_ verweigert        | Der Aufrufer verfügt nicht über ausreichende Berechtigungen, um diese Aktion abzuschließen.                          |
| scestatus \_ - \_ Löschvorgang löschen          | Das angegebene Element kann von der Funktion nicht gelöscht werden.                                                   |
| scestatus- \_ Präfix \_ Überlauf      | Ein Präfix Überlauf ist aufgetreten.                                                                      |
| scestatus \_ - \_ Fehler          | Ein unbekannter Fehler ist aufgetreten.                                                               |
| scestatus wird \_ bereits \_ ausgeführt      | Der Dienst wird schon ausgeführt.                                                                  |
| scestatus- \_ Dienst wird \_ nicht \_ unterstützt. | Der angegebene Dienst wird nicht unterstützt.                                                          |
| scestatus- \_ mod \_ nicht \_ gefunden       | Eine in der Registrierung aufgeführte Anlagen-Engine-dll wurde entweder nicht gefunden oder kann nicht geladen werden.      |
| scestatus- \_ Ausnahme \_ auf dem \_ Server | Auf dem Server ist eine Ausnahme aufgetreten.                                                             |



 

## <a name="lsa-policy-function-return-values"></a>Rückgabewerte der LSA-Richtlinien Funktion

Die meisten Richtlinien der [*lokalen Sicherheits Autorität*](/windows/desktop/SecGloss/l-gly) (LSA) geben einen NTSTATUS-Wert zurück, um den Erfolg oder Misserfolg anzuzeigen. Die verschiedenen NTSTATUS-Werte werden in der Datei "NTSTATUS. h" definiert, die mit dem Microsoft Windows Driver Development Kit (DDK) verteilt wird.

Verwenden Sie die [**lsantstatustowinerror**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) -Funktion, um einen NTSTATUS-Rückgabewert in einen Windows-Fehlercode zu konvertieren.

In der folgenden Tabelle sind die NTSTATUS-Werte aufgelistet, die von jeder LSA-Funktion zurückgegeben werden können. (In den Rückgabewert Abschnitten für einige der LSA-Funktionen sind zusätzliche Fehlercodes aufgeführt, die von der Funktion zurückgegeben werden können.) Diese Tabelle listet auch den Windows-Fehlercode auf, der den einzelnen NTSTATUS-Werten entspricht.



| NTSTATUS-Code (Windows-Fehlercode)                                        | Bedeutung                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Status \_ erfolgreich (Fehler bei \_ Erfolg)<br/>                               | Die Funktion war erfolgreich.                                                                                                            |
| Status \_ Zugriff \_ verweigert (Fehler \_ Zugriff \_ verweigert)<br/>                 | Der Aufrufer verfügt nicht über die erforderlichen Zugriffsrechte, um den Vorgang abzuschließen.                                                                  |
| Status \_ unzureichende \_ Ressourcen (Fehler \_ keine \_ System \_ Ressourcen)<br/> | Es sind nicht genügend Systemressourcen vorhanden (z. b. Arbeitsspeicher, um Puffer zuzuordnen), um den-Vorgang abzuschließen.                                        |
| Status \_ interner \_ DB- \_ Fehler (Fehler \_ interner DB- \_ \_ Fehler)<br/>       | Die LSA-Datenbank enthält interne Inkonsistenzen.                                                                                    |
| \_ungültiger \_ handle-handle (Fehler \_ ungültiges \_ handle)<br/>               | Gibt an, dass ein Objekt oder ein RPC-Handle im verwendeten [*Kontext*](/windows/desktop/SecGloss/c-gly) nicht gültig ist.     |
| Status \_ ungültiger \_ Serverstatus \_ (Fehler \_ ungültiger \_ Server \_ Zustand)<br/> | Gibt an, dass der LSA-Server zurzeit deaktiviert ist.                                                                                         |
| \_ungültiger \_ Parameter Status (Fehler bei \_ ungültigem \_ Parameter)<br/>         | Einer der Parameter ist ungültig.                                                                                                     |
| Status \_ keine \_ solche \_ Berechtigung (Fehler \_ bei \_ dieser Berechtigung \_ )<br/>       | Gibt an, dass eine angegebene Berechtigung nicht vorhanden ist.                                                                                         |
| Status \_ Objekt \_ Name \_ nicht \_ gefunden (Fehler \_ Datei \_ nicht \_ gefunden)<br/>     | Ein Objekt in der LSA-Richtlinien Datenbank wurde nicht gefunden. Das Objekt wurde möglicherweise je nach Typ entweder nach SID oder nach Name angegeben. |
| Status \_ nicht erfolgreich (Fehler bei Fehler \_ gen \_ )<br/>                     | Generischer Fehler, wie z. b. RPC-Verbindungsfehler.                                                                                        |



 

 

