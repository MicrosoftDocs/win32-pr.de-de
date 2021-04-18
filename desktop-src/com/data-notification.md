---
title: Daten Benachrichtigung
description: Objekte, die Daten aus einer externen Quelle nutzen, müssen manchmal informiert werden, wenn sich Daten in dieser Quelle ändern.
ms.assetid: 286a1ecf-5255-4443-a17d-5ffa55ed0be1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49df9e6bb7d9b15192473b18114fe7fcd69ecedf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106338495"
---
# <a name="data-notification"></a>Daten Benachrichtigung

Objekte, die Daten aus einer externen Quelle nutzen, müssen manchmal informiert werden, wenn sich Daten in dieser Quelle ändern. Beispielsweise muss ein Aktien Ticker-Band-Viewer, der auf Daten in einem Arbeitsblatt basiert, benachrichtigt werden, wenn sich die Daten ändern, um die Anzeige zu aktualisieren. Ebenso benötigt ein Verbund Dokument Informationen zu Datenänderungen in seinen eingebetteten Objekten, damit es seine Daten Caches aktualisieren kann. In solchen Fällen, in denen das dynamische Aktualisieren von Daten wünschenswert ist, benötigen Datenquellen einen Mechanismus, mit dem Daten Consumer von Änderungen benachrichtigt werden, wenn Sie auftreten, ohne dass die Consumer dazu verpflichtet werden, alles zu löschen, um Ihre Daten zu aktualisieren. Im Idealfall kann ein Konsumierende Objekt bei seiner Freizeit eine aktualisierte Kopie anfordern, um benachrichtigt zu werden, dass eine Änderung in der Datenquelle aufgetreten ist.

Der Mechanismus von com für die Behandlung von asynchronen Benachrichtigungen dieses Typs ist ein Objekt, das als "Hinweis Senke [**" bezeichnet wird. hierbei**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)handelt es sich um ein beliebiges COM-Objekt, das eine Schnittstelle mit dem Namen Consumer von Daten implementieren **IAdviseSink**. Sie registrieren sich für den Empfang von Benachrichtigungen, indem Sie einen Zeiger an das relevante Datenobjekt übergeben.

Die [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) -Schnittstellen stellen die folgenden Methoden für den Empfang von asynchronen Benachrichtigungen bereit:



| Methode                                                      | Benachrichtigt die Empfehlung-Senke, dass                                            |
|-------------------------------------------------------------|--------------------------------------------------------------------------|
| [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)<br/> | Die Daten des aufrufenden Objekts wurden geändert.<br/>                        |
| [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)<br/> | Die Anweisungen zum Zeichnen des aufrufenden Objekts haben sich geändert.<br/> |
| [**Onrename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)<br/>         | Der Moniker des aufrufenden Objekts hat sich geändert.<br/>                     |
| [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)<br/>             | Das aufrufende Objekt wurde im permanenten Speicher gespeichert.<br/>      |
| [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)<br/>           | Das aufrufenden Objekt wurde geschlossen.<br/>                           |



 

Wie die Tabelle zeigt, macht die [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) -Schnittstelle Methoden zum Benachrichtigen der Hinweis Senke anderer Ereignisse als Änderungen in den Daten des aufrufenden Objekts verfügbar. Das aufrufende Objekt kann die Senke auch benachrichtigen, wenn sich die Art und Weise ändert, in der sich das Objekt selbst zeichnet, oder es umbenannt, gespeichert oder geschlossen wird. Diese anderen Benachrichtigungen werden hauptsächlich oder vollständig im Zusammenhang mit Verbund Dokumenten verwendet, obwohl der Benachrichtigungs Mechanismus identisch ist. Weitere Informationen zu Verbund Dokument Benachrichtigungen finden Sie unter "Verbund Dokumente".

Um die Empfehlung-Senke zu nutzen, muss eine Datenquelle [**IDataObject::D-Empfehlung**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dadvise), [**IDataObject::D UN-Empfehlung**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dunadvise)und [**IDataObject:: enumdrat**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise)implementieren. Ein Datenconsumer Ruft den **dempfehlung** -Thread auf, um ein Datenobjekt zu benachrichtigen, dass es benachrichtigt werden soll, wenn sich die Daten des Objekts ändern. Das Konsumierende Objekt ruft die **dunempfehlung** -Methode auf, um diese Verbindung zu beenden. Alle interessierten Parteien können die **enumdadvisory** -Methode aufrufen, um die Anzahl der Objekte zu erlernen, die über eine Beratungs Verbindung mit einem Datenobjekt verfügen.

Wenn sich Daten an der Quelle ändern, ruft das Datenobjekt [**IAdviseSink:: OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) für alle Datenconsumer auf, die sich für den Empfang von Benachrichtigungen registriert haben. Um Beratungs Verbindungen nachzuverfolgen und das Versenden von Benachrichtigungen zu verwalten, basieren Datenquellen auf einem Objekt, das als Daten Anmelde *Inhaber* bezeichnet wird. Sie können einen eigenen Daten anrathalter erstellen, indem Sie die [**idataadvisegholder**](/windows/desktop/api/ObjIdl/nn-objidl-idataadviseholder) -Schnittstelle implementieren. Oder Sie können com das tun, indem Sie die Hilfsfunktion [**createdataadvicholder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenübertragung](data-transfer.md)
</dt> </dl>

 

