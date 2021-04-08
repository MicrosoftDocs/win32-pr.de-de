---
title: Ermittlungs Seiten
description: Ermittlungs Seiten
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Windows Media Player Online Stores, Ermittlungs Seiten
- Online Stores, Ermittlungs Seiten
- Typ 1 Online Stores, Ermittlungs Seiten
- Windows Media Player-Bibliothek, Ermittlungs Seiten
- Bibliothek, Ermittlungs Seiten
- Ermittlungs Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349b0e7238aa6d59b56f9035a3c02a5b3ff7b7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723517"
---
# <a name="discovery-pages"></a>Ermittlungs Seiten

Wenn es sich bei dem aktiven Onlinespeicher um einen Speicher vom Typ 1 handelt, wird in Windows Media Player der Inhalt des Stores in der Benutzeroberfläche angezeigt. Das Bibliotheksstruktur Ansicht-Steuerelement verfügt über einen Knoten für den Online Shop. Wenn der Benutzer auf den Knoten oder auf einen seiner untergeordneten Knoten klickt, zeigt Windows Media Player Inhalt aus dem Online Store im Detailbereich an.

Wenn der Benutzer mit Online Store-Inhalten im Strukturansicht-Steuerelement oder im Detailbereich interagiert, zeigt Windows Media Player Webseiten, die als *Discovery Pages* bezeichnet werden, im Online Store an. Discovery Pages bieten zusätzliche Informationen über die Musik, wenn der Benutzer den Katalog des Online Stores durchsucht. Ermittlungs Seiten kommunizieren mit Windows-Media Player über die Eigenschaften, Methoden und Ereignisse des [externen Objekts](external-object-for-type-1-online-stores.md).

Jedes Mal, wenn Windows Media Player seine Ansicht des Online Store-Inhalts ändert, wird [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)aufgerufen, das durch das Plug-in des Online Stores implementiert wird, um die URL der Ermittlungs Seite zu erhalten, die mit der neuen Ansicht angezeigt werden soll.

Die Ansicht des Online Store-Inhalts in Windows Media Player ist durch fünf Informationen gekennzeichnet: Task, Location Type, Location ID, Selected Item Type und Selected Item ID. Windows Media Player stellt diese fünf Elemente an die **GetTemplate** -Methode in den Parametern *Task*, *Location*, *pContext*, *clicklocation* und *pclickcontext* bereit. Diese fünf Elemente werden von Windows Media Player den Ermittlungs Seiten in den Eigenschaften " *Task*", " *librarylocationtype*", " *librarylocationid*", " *selecteditemtype*" und " *selecteditemid* " des **externen** Objekts zur Verfügung gestellt. Weitere Informationen dazu, wie Windows Media Player seine Ansicht von Online Store-Inhalten angibt, finden Sie unter [Location and Selected item](location-and-selected-item.md).

Zusätzlich zum Aktivieren einer Ermittlungs Seite für die Kommunikation mit Windows Media Player ermöglicht das **externe** Objekt der Ermittlungs Seite, mit dem Plug-in für den Onlinespeicher zu kommunizieren. Wenn dies der Fall ist, fungiert Windows Media Player als Brücke zwischen der Ermittlungs Seite und dem Plug-in. So kann z. b. auf der Ermittlungs Seite [extern. SendMessage](external-sendmessage.md) aufgerufen werden, um eine benutzerdefinierte Nachricht an das Plug-in zu senden. Windows Media Player empfängt diesen Methodenaufruf und ruft wiederum [iwmpcontentpartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) auf, um die Nachricht an das Plug-in zu übergeben. Wenn das Plug-in die Verarbeitung der Nachricht abgeschlossen hat, wird [iwmpcontentpartnercallback:: sendmessagecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)aufgerufen. Windows Media Player benachrichtigt die Ermittlungs Seite dann durch das Ausführen des [externen. onsendmessagecomplete](external-onsendmessagecomplete-event.md) -Ereignisses.

Das **externe** Objekt bietet auch eine Möglichkeit, eine Ermittlungs Seite mit einer anderen Ermittlungs Seite zu kommunizieren. Wenn das Skript auf einer Ermittlungs Seite [extern. changeView](external-changeview.md)aufruft, kann das Skript eine Zeichenfolge im *viewparams* -Parameter angeben. Windows Media Player interpretiert die *viewparameterzeichenfolge* nicht, aber die Zeichenfolge wird auf der nächsten Ermittlungs Seite in der Eigenschaft [extern. viewparameters](external-viewparameters.md) verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 




