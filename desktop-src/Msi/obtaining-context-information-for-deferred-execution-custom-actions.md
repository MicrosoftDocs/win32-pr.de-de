---
description: Da das Installationsskript außerhalb der Installationssitzung ausgeführt werden kann, in der es geschrieben wurde, ist die Sitzung während der Ausführung des Installations Skripts möglicherweise nicht mehr vorhanden.
ms.assetid: 13174c5d-c810-4b5d-9d1e-60ed30b8c44d
title: Abrufen von Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13cd956509a5b8a4c92e0a53bfa455154a59bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753513"
---
# <a name="obtaining-context-information-for-deferred-execution-custom-actions"></a>Abrufen von Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung

Da das Installationsskript außerhalb der Installationssitzung ausgeführt werden kann, in der es geschrieben wurde, ist die Sitzung während der Ausführung des Installations Skripts möglicherweise nicht mehr vorhanden. In diesem Fall sind die ursprünglichen Sitzungs Handles und Eigenschaften, die während der Installations Sequenz festgelegt werden, für eine benutzerdefinierte Aktion der verzögerten Ausführung nicht verfügbar. Alle Funktionen, die ein Sitzungs handle erfordern, sind auf einige Methoden beschränkt, die Kontextinformationen abrufen können, oder andere Eigenschaften, die während der Skriptausführung benötigt werden, müssen in das Installationsskript geschrieben werden. Beispielsweise übergeben verzögerte benutzerdefinierte Aktionen, die Dynamic Link Libraries (DLLs) aufzurufen, ein Handle, das nur zum Abrufen einer sehr begrenzten Menge von Informationen verwendet werden kann. Auf Funktionen, die kein Sitzungs handle erfordern, kann über eine verzögerte benutzerdefinierte Aktion zugegriffen werden.

Benutzerdefinierte Aktionen der verzögerten Ausführung sind auf das Aufrufen der folgenden Funktionen beschränkt, die ein Handle erfordern.



| Funktion                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)       | Unterstützt eine begrenzte Anzahl von Eigenschaften, wenn Sie mit [benutzerdefinierten Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md)verwendet wird: die customaktiondata-Eigenschaft, die [**ProductCode**](productcode.md) -Eigenschaft und die [**UserSID**](usersid.md) -Eigenschaft [Benutzerdefinierte COMMIT-Aktionen](commit-custom-actions.md) können die [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) -Funktion nicht zum Abrufen der [**ProductCode**](productcode.md) -Eigenschaft verwenden. Benutzerdefinierte COMMIT-Aktionen können die customaktiondata-Eigenschaft zum Abrufen des Produktcodes verwenden.<br/> |
| [**Msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)     | Unterstützt eine begrenzte Anzahl von Eigenschaften, wenn Sie mit [benutzerdefinierten Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md)verwendet wird: die Eigenschaften customaktiondata und ProductCode.                                                                                                                                                                                                                                                                                                                                                      |
| [**Msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)               | Beim Aufrufen von [benutzerdefinierten Aktionen für verzögerte Ausführung](deferred-execution-custom-actions.md), [Commit für benutzerdefinierte Aktionen](commit-custom-actions.md)oder Zurücksetzen von [benutzerdefinierten Aktionen](rollback-custom-actions.md)gibt [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) true oder false zurück, wenn es angefordert wird, die Modusparameter msirunmode \_ , geplant, msirunmode \_ Commit oder msirunmode Rollback zu überprüfen \_ . Anforderungen zum Überprüfen anderer Parameter des Testlaufs aus einer verzögerten, Commit-oder Rollback-benutzerdefinierten Aktion gibt false zurück.<br/>                       |
| [**Msigetlanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage)       | Die numerische Sprach-ID für das aktuelle Produkt. [Benutzerdefinierte COMMIT-Aktionen](commit-custom-actions.md) können die [**msigetlanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) -Funktion nicht verwenden. Benutzerdefinierte COMMIT-Aktionen können die customaktiondata-Eigenschaft verwenden, um die numerische Sprach-ID zu erhalten.<br/>                                                                                                                                                                                                                                                           |
| [**Msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) | Verarbeitet Fehler-oder Fortschrittsmeldungen von der benutzerdefinierten Aktion.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Für eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, ist das install [**Session**](session-object.md) -Objekt erforderlich. Dies ist vom Typ **Sitzungs Objekt** , und das Installationsprogramm fügt es dem Skript mit dem Namen "Session" an. Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben wurde, eine der folgenden Methoden oder Eigenschaften des **Session** -Objekts verwenden, um den Kontext abzurufen.



| Name                                                           | BESCHREIBUNG                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Mode-Eigenschaft**](session-mode.md)                          | Gibt true für msirunmode \_ nur geplant zurück.                                                                                       |
| [**Property-Eigenschaft (Session-Objekt)**](session-session.md)  | Gibt die customaktiondata-Eigenschaft, die [**ProductCode**](productcode.md) -Eigenschaft oder die [**UserSID**](usersid.md) -Eigenschaft zurück.        |
| [**Language-Eigenschaft (Session-Objekt)**](session-language.md) | Gibt die numerische Sprach-ID der Installationssitzung zurück.                                                                           |
| [**Message-Methode**](session-message.md)                      | Wird aufgerufen, um Fehler und den Fortschritt zu behandeln.                                                                                              |
| [**Installereigenschaft**](session-installer.md)                | Gibt das übergeordnete-Objekt zurück, das für Funktionen ohne Sitzung verwendet wird, z. b. Registrierungs Zugriff und installerkonfigurationsverwaltung. |



 

Eigenschaftswerte, die zum Zeitpunkt der Verarbeitung der Installations Sequenz in das Skript festgelegt werden, sind möglicherweise zum Zeitpunkt der Skriptausführung nicht verfügbar. Nur die folgenden eingeschränkten Eigenschaften sind während der Skriptausführung immer für benutzerdefinierte Aktionen zugänglich.



| Eigenschaftenname                      | BESCHREIBUNG                                                                                                                                                                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Customaktiondata                   | Wert, wenn die benutzerdefinierte Aktion in der Sequenz Tabelle verarbeitet wird. Die customaktiondata-Eigenschaft ist nur für benutzerdefinierte Aktionen mit verzögerter Ausführung verfügbar. Sofortige benutzerdefinierte Aktionen haben keinen Zugriff auf diese Eigenschaft. |
| [**ProductCode**](productcode.md) | Eindeutiger Code für das Produkt, eine [GUID](guid.md) -Zeichenfolge.                                                                                                                                                         |
| [**UserSID**](usersid.md)         | Wird vom Installationsprogramm auf die Sicherheits-ID (SID) des Benutzers festgelegt.                                                                                                                                                   |



 

Wenn für die benutzerdefinierte Aktion verzögerte Ausführung andere Eigenschaften Daten erforderlich sind, müssen die zugehörigen Werte im Installationsskript gespeichert werden. Dies kann mithilfe einer zweiten benutzerdefinierten Aktion erfolgen.

**So schreiben Sie den Wert einer Eigenschaft in das Installationsskript für die Verwendung während einer benutzerdefinierten Aktion für eine verzögerte Ausführung**

1.  Fügen Sie eine kleine benutzerdefinierte Aktion in die Installations Sequenz ein, mit der die zu berücksichtigende Eigenschaft auf eine Eigenschaft festgelegt wird, die denselben Namen wie die benutzerdefinierte Aktion der verzögerten Wenn beispielsweise der Primärschlüssel für die benutzerdefinierte Aktion für die verzögerte Ausführung "myaction" lautet, legen Sie eine Eigenschaft mit dem Namen "myaction" auf die X-Eigenschaft fest, die Sie abrufen müssen. Sie müssen die Eigenschaft "myaction" in der Installations Sequenz vor der benutzerdefinierten Aktion "myaction" festlegen. Obwohl eine beliebige Art von benutzerdefinierter Aktion die Kontext Daten festlegen kann, ist die einfachste Methode, eine benutzerdefinierte Aktion für die Eigenschaften Zuweisung zu verwenden (z. b. [benutzerdefinierter Aktionstyp 51](custom-action-type-51.md)).
2.  Zum Zeitpunkt der Verarbeitung der Installations Sequenz schreibt das Installationsprogramm den Wert der Eigenschaft X in das Ausführungs Skript als Wert der Eigenschaft customaktiondata.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Eigenschafts Verweis](property-reference.md)
</dt> </dl>

 

 




