---
title: Ermittlungsseiten
description: Ermittlungsseiten
ms.assetid: deb0cbf9-b7e1-4ce6-8241-b9199129515a
keywords:
- Windows Media Player Onlineshops, Ermittlungsseiten
- Onlineshops, Ermittlungsseiten
- Geben Sie 1 Onlineshops ein, Ermittlungsseiten
- Windows Media Player Bibliothek, Ermittlungsseiten
- Bibliothek, Ermittlungsseiten
- Ermittlungsseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe29ed5d3948bbdcd6f36239938e3a4e552362318b6ec48658e85895cb58d163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997340"
---
# <a name="discovery-pages"></a>Ermittlungsseiten

Wenn der aktive Onlineshop ein Store vom Typ 1 ist, zeigt Windows Media Player den Inhalt des Geschäfts auf der Benutzeroberfläche an. Das Bibliotheksstrukturansicht-Steuerelement verfügt über einen Knoten für den Onlineshop. Wenn der Benutzer auf diesen Knoten oder eines seiner Unterknoten klickt, zeigt Windows Media Player Inhalte aus dem Onlineshop im Detailbereich an.

Während der Benutzer mit Onlinespeicherinhalten im Strukturansichtssteuerelement oder im Detailbereich interagiert, zeigt Windows Media Player Webseiten an, die vom Onlineshop als *Ermittlungsseiten* bezeichnet werden. Ermittlungsseiten bieten zusätzliche Informationen zur Musik, während der Benutzer den Katalog des Onlineshops durchsucht. Ermittlungsseiten kommunizieren mit Windows Media Player über die Eigenschaften, Methoden und Ereignisse des [externen Objekts](external-object-for-type-1-online-stores.md).

Wenn Windows Media Player die Ansicht der Inhalte des Onlineshops ändert, ruft sie [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)auf, die vom Plug-In des Onlineshops implementiert wird, um die URL der Ermittlungsseite abzurufen, die mit der neuen Ansicht angezeigt werden soll.

Die Ansicht des Onlinespeicherinhalts in Windows Media Player ist durch fünf Informationen gekennzeichnet: Task, Standorttyp, Standort-ID, ausgewählter Elementtyp und ausgewählte Element-ID. Windows Media Player stellt diese fünf Elemente für die **GetTemplate-Methode** in den Parametern *task,* *location,* *pContext,* *clickLocation* und *pClickContext* bereit. Windows Media Player macht diese fünf Elemente für Ermittlungsseiten in den *Eigenschaften*, *libraryLocationType,* *libraryLocationID,* *selectedItemType* und *selectedItemID* des **External-Objekts** verfügbar. Weitere Informationen dazu, wie Windows Media Player die Ansicht des Onlinespeicherinhalts angibt, finden Sie unter [Speicherort und Ausgewähltes Element.](location-and-selected-item.md)

Zusätzlich zur Aktivierung einer Ermittlungsseite für die Kommunikation mit Windows Media Player ermöglicht das **External-Objekt** einer Ermittlungsseite die Kommunikation mit dem Plug-In des Onlineshops. In diesem Fall fungiert Windows Media Player als Brücke zwischen der Ermittlungsseite und dem Plug-In. Beispielsweise kann die Ermittlungsseite [External.sendMessage](external-sendmessage.md) aufrufen, um eine benutzerdefinierte Nachricht an das Plug-In zu senden. Windows Media Player empfängt diesen Methodenaufruf und ruft wiederum [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage) auf, um die Nachricht an das Plug-In zu übergeben. Wenn das Plug-In die Verarbeitung der Nachricht abgeschlossen hat, ruft es [IWMPContentPartnerCallback::SendMessageComplete auf.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) Windows Media Player benachrichtigt dann die Ermittlungsseite, indem das [External.OnSendMessageComplete-Ereignis](external-onsendmessagecomplete-event.md) ausgegeben wird.

Das **Externe** Objekt bietet auch eine Möglichkeit für eine Ermittlungsseite, mit einer anderen Ermittlungsseite zu kommunizieren. Wenn das Skript auf einer Ermittlungsseite [External.changeView](external-changeview.md)aufruft, kann das Skript eine Zeichenfolge im *ViewParams-Parameter* angeben. Windows Media Player interpretiert die *ViewParams-Zeichenfolge* nicht, macht die Zeichenfolge jedoch für die nächste Ermittlungsseite in der [External.viewParameters-Eigenschaft](external-viewparameters.md) verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 




