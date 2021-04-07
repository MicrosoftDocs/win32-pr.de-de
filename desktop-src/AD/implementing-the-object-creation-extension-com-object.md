---
title: Implementieren des COM-Objekts für die Objekt Erstellungs Erweiterung
description: Eine Objekt Erstellungs Erweiterung ist ein COM-Objekt, das als in-proc-Server implementiert wird. Sowohl primäre als auch sekundäre Objekt Erstellungs Erweiterungen müssen die idsadminnewobjext-Schnittstelle implementieren.
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- Implementieren der Objekt Erstellungs Erweiterung com-Objekt AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c1a9da94caa300c1277cf6f6030357ca9d573d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038749"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>Implementieren des COM-Objekts für die Objekt Erstellungs Erweiterung

Eine Objekt Erstellungs Erweiterung ist ein COM-Objekt, das als in-proc-Server implementiert wird. Sowohl primäre als auch sekundäre Objekt Erstellungs Erweiterungen müssen die [**idsadminnewobjext**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) -Schnittstelle implementieren.

## <a name="implementing-idsadminnewobjext"></a>Implementieren von idsadminnewobjext

Beim Erstellen des Objekterstellungs-Assistenten wird jede Erweiterung zum Erstellen von Objekten initialisiert, indem die [**idsadminnewobjext:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) -Methode der Erweiterung aufgerufen wird. Die **Initialize** -Methode stellt der Erweiterung Informationen über den Container zur Verfügung, in dem das Objekt erstellt wird, den Klassennamen des neuen Objekts und Informationen zum Assistenten selbst. Wenn der Objekterstellungs-Assistent gestartet wird, um ein neues-Objekt aus einem vorhandenen-Objekt zu erstellen, ist der *padscopysource* -Parameter nicht **null**. In diesem Fall sollte die Erweiterung versuchen, so viele Daten wie möglich aus dem Objekt abzurufen, das kopiert wird.

Nachdem die Erweiterung initialisiert wurde, wird die [**idsadminnewobjext:: addPages**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) -Methode aufgerufen. Die Erweiterung muss dem Assistenten während dieser Methode die Seite oder Seiten hinzufügen. Eine Assistenten Seite wird erstellt, indem Sie eine [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) -Struktur ausfüllen und diese Struktur dann an [**die Funktion "**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) die Funktion" "von" | Die Seite wird dann durch Aufrufen der Rückruffunktion, die an **addPages** im *lpfnaddpage* -Parameter übergeben wird, dem Assistenten hinzugefügt.

Vor dem Anzeigen der Erweiterungs Seite wird " [**idsadminnewobjext::**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) Server" aufgerufen. Dadurch wird der Erweiterung ein [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstellen Zeiger für das Objekt bereitstellt, das erstellt wird.

Während die Seite des Assistenten angezeigt wird, sollte die Seite alle erforderlichen Assistenten Benachrichtigungs Meldungen wie z. b. " [**PSN \_ SETACTIVE**](../controls/psn-setactive.md) " und " [**PSN" \_ Next**](../controls/psn-wiznext.md)behandeln und darauf reagieren.

Wenn der Benutzer alle Assistenten Seiten abschließt, zeigt der Assistent eine Seite "Fertigstellen" an, die eine Zusammenfassung der eingegebenen Daten bereitstellt. Der Assistent ruft diese Daten ab, indem er die [**idsadminnewobjext:: getsummaryinfo**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) -Methode für jede der Erweiterungen aufruft. Die **getsummaryinfo** -Methode stellt ein **BSTR** bereit, das die Textdaten enthält, die auf der Seite "Fertigstellen" angezeigt werden. Eine Objekt Erstellungs Erweiterung muss keine Zusammenfassungs Daten bereitstellen. In diesem Fall sollte **getsummaryinfo** **E \_ notimpl** zurückgeben. **Getsummaryinfo** wird nur einmal für jede Erweiterung aufgerufen, nicht für jede Seite. wenn die Objekt Erstellungs Erweiterung also mehr als eine Seite hinzufügt, muss die Erweiterung die Zusammenfassungs Daten in einer Zeichenfolge kombinieren.

Wenn der Benutzer auf der Seite "Fertigstellen" auf die Schaltfläche **Fertig** stellen klickt, ruft der Assistent jede der [**idsadminnewobjext:: schreitedata**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) -Methoden der Erweiterung mit dem **DSA \_ newobj \_ ctx- \_ vorCOMMIT** -Kontext auf. Wenn dies auftritt, sollte die Erweiterung die gesammelten Daten mithilfe der [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) -Methode oder der [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) -Methode in die entsprechenden Eigenschaften schreiben. Die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstelle wird der Erweiterung in der [**idsadminnewobjext::**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) Server-Methode bereitgestellt. Die Erweiterung sollte die zwischengespeicherten Eigenschaften nicht durch Aufrufen von " [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)" ausführen. Wenn alle Eigenschaften geschrieben wurden, führt die primäre Objekt Erstellungs Erweiterung einen Commit für die Änderungen durch Aufrufen von **IADs:: SetInfo** durch. Dies wird im folgenden ausführlicher erläutert.

Wenn ein Fehler auftritt, wird die Erweiterung über den Fehler benachrichtigt, und während des Vorgangs ist Sie aufgetreten, als die [**idsadminnewobjext:: OnError**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror) -Methode aufgerufen wird.

## <a name="implementing-a-primary-object-creation-wizard"></a>Implementieren eines primären Objekterstellungs-Assistenten

Die Implementierung eines Assistenten für die Erstellung von primären Objekten ist mit dem Assistenten für die Erstellung sekundärer Objekte identisch, mit dem Unterschied, dass ein primärer Objekterstellungs-Assistent einige weitere Schritte

Bevor die erste Seite verworfen wird, muss der Objekterstellungs-Assistent das temporäre Verzeichnis Objekt erstellen. Um dies zu erreichen, müssen Sie die [**idsadminnewobjprimarysite:: kreatenew**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) -Methode aufrufen. Ein Zeiger auf die [**idsadminnewobjprimarysite**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite) -Schnittstelle wird durch Aufrufen von " [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) " mit **IID " \_ idsadminnewobjprimarysite** " in der Schnittstelle " [**idsadminnewobj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj) " abgerufen, die an " [**idsadminnewobjext:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize)" übergeben wird. Die **kreatenew** -Methode erstellt ein neues temporäres Objekt und ruft [**idsadminnewobjext:: SetObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) für jede Erweiterung auf.

Wenn ein Objekterstellungs-Assistent mehr als eine Seite enthält, implementiert das System eine Seite "Fertigstellen", auf der eine Zusammenfassung der zu speichernden Objektinformationen angezeigt wird. Wenn Sie auf die Schaltfläche **Fertig** stellen auf der Seite "Fertigstellen" klicken, ruft das System jede der [**idsadminnewobjext:: schreitedata**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) -Methode der Objekt Erstellungs Erweiterung auf und führt dann ein Commit für das temporäre Objekt in den persistenten Speicher aus. Wenn der Objekterstellungs-Assistent jedoch nur eine Seite enthält, enthält die Seite die Schaltflächen **OK** und **Abbrechen** anstelle der Schaltflächen **zurück**, **weiter** und **Abbrechen** , die normalerweise in einem Assistenten gefunden werden, und es wird keine Seite "Fertigstellen" bereitgestellt. Aus diesem Grund muss ein Erweiterungs-Assistent für eine Einzelseiten-Objekt Erstellung [**idsadminnewobjprimarysite:: Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) zum Ausführen der Schreib-und Speichervorgänge aufruft. Eine einseitige Erweiterung für das primäre Objekt Erstellungs Erweiterung sollte " **Commit** " als Antwort auf die " [**PSN \_ witzfinish**](../controls/psn-wizfinish.md) "-Benachrichtigung aufruft.

Da andere Erweiterungen zum Erstellen von Objekten dem Assistenten Seiten hinzufügen können, weiß die primäre Objekt Erstellungs Erweiterung möglicherweise nicht, ob im Assistenten mehr als eine Seite vorhanden ist. Dies ist aus zwei Gründen kein Problem: Wenn das System z. b. die Seite "Fertigstellen" implementiert, empfängt die primäre Objekt Erstellungs Erweiterung die " [**PSN- \_ dernext**](../controls/psn-wiznext.md) "-Benachrichtigung anstelle der " **PSN- \_ weiter** -Benachrichtigung". Im zweiten Fall schlägt [**Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) unnötig fehl, wenn der Assistent mehr als eine Seite enthält.

 

 