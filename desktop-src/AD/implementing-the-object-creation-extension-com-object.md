---
title: Implementieren des COM-Objekts für die Objekterstellungserweiterung
description: Eine Objekterstellungserweiterung ist ein COM-Objekt, das als In-Proc-Server implementiert wird. Sowohl primäre als auch sekundäre Objekterstellungserweiterungen müssen die IDsAdminNewObjExt-Schnittstelle implementieren.
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- Implementieren der COM-Objekt-AD-Erweiterung für die Objekterstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c1d7eb9d3e2fe80e721068f39746e08f0ecf5a1db721658c02ec52aca39687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187638"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>Implementieren des COM-Objekts für die Objekterstellungserweiterung

Eine Objekterstellungserweiterung ist ein COM-Objekt, das als In-Proc-Server implementiert wird. Sowohl primäre als auch sekundäre Objekterstellungserweiterungen müssen die [**IDsAdminNewObjExt-Schnittstelle**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) implementieren.

## <a name="implementing-idsadminnewobjext"></a>Implementieren von IDsAdminNewObjExt

Wenn der Objekterstellungs-Assistent erstellt wird, initialisiert er jede Objekterstellungserweiterung durch Aufrufen der [**IDsAdminNewObjExt::Initialize-Methode der**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) Erweiterung. Die **Initialize-Methode** stellt der Erweiterung Informationen zum Container, in dem das Objekt erstellt wird, den Klassennamen des neuen Objekts und Informationen zum Assistenten selbst zur Verfügung. Wenn der Objekterstellungs-Assistent gestartet wird, um ein neues Objekt aus einem vorhandenen Objekt zu erstellen, ist der *pADsCopySource-Parameter* nicht **NULL.** In diesem Fall sollte die Erweiterung versuchen, so viele Daten wie möglich aus dem zu kopierenden Objekt zu erhalten.

Nachdem die Erweiterung initialisiert wurde, wird die [**IDsAdminNewObjExt::AddPages-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) aufgerufen. Die Erweiterung muss dem Assistenten während dieser Methode die Seiten hinzufügen. Eine Assistentenseite wird erstellt, indem eine [**PROPSHEETPAGE-Struktur**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) auffüllt und diese Struktur dann an die [**CreatePropertySheetPage-Funktion übergeben**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) wird. Die Seite wird dann dem Assistenten durch Aufrufen der Rückruffunktion hinzugefügt, die im *Parameter lpfnAddPage* an **AddPages** übergeben wird.

Bevor die Erweiterungsseite angezeigt wird, [**wird IDsAdminNewObjExt::SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) aufgerufen. Dadurch wird der Erweiterung ein [**IADs-Schnittstellenzeiger**](/windows/desktop/api/iads/nn-iads-iads) für das zu erstellende Objekt zur Verfügung stellt.

Während die Seite des Assistenten angezeigt wird, sollte die Seite alle erforderlichen Benachrichtigungsmeldungen des Assistenten behandeln und darauf reagieren, z. B. [**PSN \_ SETACTIVE**](../controls/psn-setactive.md) und [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md).

Wenn der Benutzer alle Assistentenseiten schließt, zeigt der Assistent eine Seite "Fertig stellen" an, die eine Zusammenfassung der eingegebenen Daten enthält. Der Assistent ruft diese Daten ab, indem er die [**IDsAdminNewObjExt::GetSummaryInfo-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) für jede der Erweiterungen aufruft. Die **GetSummaryInfo-Methode** stellt einen **BSTR mit** den text-Daten zur Anzeige auf der Seite "Finish" (Fertig stellen) zur Seite . Eine Objekterstellungserweiterung muss keine Zusammenfassungsdaten liefern. In diesem Fall sollte **GetSummaryInfo** **E \_ NOTIMPL zurückgeben.** **GetSummaryInfo** wird nur einmal für jede Erweiterung und nicht pro Seite aufgerufen. Wenn die Objekterstellungserweiterung also mehr als eine Seite hinzufügt, muss die Erweiterung die Zusammenfassungsdaten in einer Zeichenfolge kombinieren.

Wenn der Benutzer  auf der Seite "Fertig stellen" auf die Schaltfläche Fertig stellen klickt, ruft der Assistent jede [**der IDsAdminNewObjExt::WriteData-Methoden**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) der Erweiterung mit dem **DSA \_ NEWOBJ \_ CTX \_ PRECOMMIT-Kontext** auf. In diesem Fall sollte die Erweiterung die gesammelten Daten mithilfe der [**IADs::P ut-**](/windows/desktop/api/iads/nf-iads-iads-put) oder [**IADs::P utEx-Methode in die entsprechenden Eigenschaften**](/windows/desktop/api/iads/nf-iads-iads-putex) schreiben. Die [**IADs-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iads) wird der Erweiterung in der [**IDsAdminNewObjExt::SetObject-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) bereitgestellt. Die Erweiterung sollte die zwischengespeicherten Eigenschaften nicht durch Aufrufen von [**IADs::SetInfo übertragen.**](/windows/desktop/api/iads/nf-iads-iads-setinfo) Wenn alle Eigenschaften geschrieben wurden, committ die Primäre Objekterstellungserweiterung die Änderungen, indem **sie IADs::SetInfo aufruft.** Dies wird weiter unten ausführlicher erläutert.

Wenn ein Fehler auftritt, wird die Erweiterung über den Fehler und den Vorgang benachrichtigt, der beim Aufrufen der [**IDsAdminNewObjExt::OnError-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror) aufgetreten ist.

## <a name="implementing-a-primary-object-creation-wizard"></a>Implementieren eines Assistenten zum Erstellen primärer Objekte

Die Implementierung eines Assistenten zum Erstellen primärer Objekte ist identisch mit einem Assistenten zum Erstellen sekundärer Objekte, mit der Ausnahme, dass ein Assistent zum Erstellen primärer Objekte einige weitere Schritte ausführen muss.

Bevor die erste Seite verworfen wird, muss der Objekterstellungs-Assistent das temporäre Verzeichnisobjekt erstellen. Rufen Sie hierzu die [**IDsAdminNewObjPrimarySite::CreateNew-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) auf. Ein Zeiger auf die [**IDsAdminNewObjPrimarySite-Schnittstelle**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite) wird durch Aufrufen von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) mit **\_ IID-IDsAdminNewObjPrimarySite** auf der [**IDsAdminNewObj-Schnittstelle**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj) erhalten, die an [**IDsAdminNewObjExt::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize)übergeben wird. Die **CreateNew-Methode** erstellt ein neues temporäres Objekt und ruft [**IDsAdminNewObjExt::SetObject für**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) jede Erweiterung auf.

Wenn ein Objekterstellungs-Assistent mehr als eine Seite enthält, implementiert das System eine Seite "Fertig stellen", die eine Zusammenfassung der zu speichernden Objektinformationen anzeigt. Wenn  auf der Seite "Fertig stellen" auf die Schaltfläche Fertig stellen geklickt wird, wird vom System die [**IDsAdminNewObjExt::WriteData-Methode**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) der Objekterstellungserweiterung aufruft und dann ein Commit für das temporäre Objekt in den permanenten Speicher abgeschlossen. Wenn der Objekterstellungs-Assistent jedoch nur eine Seite enthält, enthält die Seite die  Schaltflächen **OK** und Abbrechen anstelle der Schaltflächen **Zurück,** **Weiter** und Abbrechen, die normalerweise in einem Assistenten gefunden werden, und es wird keine Seite "Fertig stellen" bereitgestellt.  Aus diesem Grund muss ein Assistent zum Erstellen von Einzelseitenobjekten [**IDsAdminNewObjPrimarySite::Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) aufrufen, um die Schreib- und Speichervorgänge durchzuführen. Eine Erweiterung zum Erstellen eines primären Einzelseitenobjekts sollte **Commit** als Antwort auf die [**PSN \_ WIZFINISH-Benachrichtigung**](../controls/psn-wizfinish.md) aufrufen.

Da andere Objekterstellungserweiterungen dem Assistenten Seiten hinzufügen können, weiß die Primäre Objekterstellungserweiterung möglicherweise nicht, ob der Assistent mehrere Seiten enthält. Dies ist aus zwei Gründen kein Problem: Wenn das System die Seite "Fertig stellen" implementiert, erhält die Primäre Objekterstellungserweiterung die [**PSN \_ WIZNEXT-Benachrichtigung**](../controls/psn-wiznext.md) anstelle der **PSN \_ WIZNEXT-Benachrichtigung.** Zweitens kann [**commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) nicht ohne Fehler ausgeführt werden, wenn der Assistent mehr als eine Seite enthält.

 

 