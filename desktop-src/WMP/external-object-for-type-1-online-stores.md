---
title: Externes Objekt für den Typ 1-Online Speicher
description: Externes Objekt für den Typ 1-Online Speicher
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Windows Media Player Online Stores, externe Objekte
- Online Stores, externe Objekte
- Typ 1 Online Stores, externe Objekte
- externe Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f50e5e6bfc98ea3669996b06fa4a4defb52452fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948028"
---
# <a name="external-object-for-type-1-online-stores"></a>Externes Objekt für den Typ 1-Online Speicher

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **externe** Objekt bietet Funktionen für Webseiten, die von einem Online Shop bereitgestellt werden und in Windows Media Player gehostet werden.

Das **externe** Objekt macht die folgenden Eigenschaften für den Typ 1 Online Stores verfügbar.



| Eigenschaft                                                                                  | BESCHREIBUNG                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [AccountType](external-accounttype.md)                                                   | Ruft den Kontotyp des aktuellen Benutzers ab.                                                                                          |
| [appcolorbuttonhighlight](external-appcolorbuttonhighlight.md)                           | Ruft die aktuelle Schaltflächen Hervorhebungs Farbe für die Windows Media Player-Benutzeroberfläche ab.                                                |
| [appcolorbuttonhoverface](external-appcolorbuttonhoverface.md)                           | Ruft die aktuelle Schaltflächen-Hover-Farbe für die Windows Media Player-Benutzeroberfläche ab.                                                    |
| [appcolorbuttonshadow](external-appcolorbuttonshadow.md)                                 | Ruft die aktuelle Schaltflächen Schatten Farbe für die Windows Media Player-Benutzeroberfläche ab.                                                   |
| [appcolordark](external-appcolordark.md)                                                 | Ruft die aktuelle dunkel schattierte Farbe der Windows Media Player-Benutzeroberfläche ab.                                                      |
| [appcolorlight](external-appcolorlight.md)                                               | Ruft die aktuelle helle schattierte Farbe der Windows Media Player-Benutzeroberfläche ab.                                                     |
| [appcolormedium](external-appcolormedium.md)                                             | Ruft die aktuelle mittelgroße schattierte Farbe der Windows Media Player-Benutzeroberfläche ab.                                                    |
| [Baskettitel](external-baskettitle.md)                                                   | Ruft den Titel der Schaltfläche im Listen Bereich (auch als Warenkorb bezeichnet) in Windows Media Player ab.                                     |
| [filter](external-filter.md)                                                             | Ruft den Suchfilter ab, der derzeit von Windows Media Player verwendet wird.                                                                    |
| [ignoreiehistory](external-ignoreiehistory.md)                                           | Gibt an, ob Windows Media Player den Internet Explorer-Verlauf ignorieren soll.                                                          |
| [librarylocationid](external-librarylocationid.md)                                       | Ruft den Bezeichner eines bestimmten Medien Elements ab, das momentan in der Ansicht des Players angezeigt wird.                                      |
| [librarylocationtype](external-librarylocationtype.md)                                   | Ruft eine [Bibliotheks Speicherort Konstante](library-location-constants.md) ab, die den Typ der aktuellen Ansicht in Windows-Media Player angibt. |
| [pluginrunning](external-pluginrunning.md)                                               | Ruft einen Wert ab, der angibt, ob das Plug-in des Online Stores ausgeführt wird.                                                          |
| [selecteditemid](external-selecteditemid.md)                                             | Ruft den Bezeichner des Medien Elements ab, das derzeit in Windows Media Player ausgewählt ist.                                           |
| [selecteditemtype](external-selecteditemtype.md)                                         | Ruft den Typ des Medien Elements ab, das derzeit in Windows Media Player ausgewählt ist.                                                 |
| [Task](external-task.md)                                                                 | Ruft den Namen des aktuellen Aufgabenbereichs ab.                                                                                             |
| [templatebingdisplayedinlocallibrary](external-templatebeingdisplayedinlocallibrary.md) | Gibt an, ob der von der aktuellen Ermittlungs Seite dargestellte Feed im Strukturansicht-Steuerelement der lokalen Bibliothek angezeigt wird.          |
| [userloggedin](external-userloggedin.md)                                                 | Ruft einen Wert ab, der angibt, ob der Benutzer am Online Store angemeldet ist.                                                          |
| [version](external-version.md)                                                           | Ruft die aktuelle Version von Windows Media Player ab.                                                                                   |
| [viewparameters](external-viewparameters.md)                                             | Ruft Parameter ab, die der aktuellen Ansicht in Windows Media Player zugeordnet sind.                                                           |



 

Das **externe** Objekt macht die folgenden Methoden für den Typ 1 Online Stores verfügbar.



| Methode                                                            | BESCHREIBUNG                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| ["AddTo Basket"](external-addtobasket.md)                           | Fügt dem Listen Bereich (auch als Warenkorb bezeichnet) in Windows Media Player Medienelemente hinzu.                                          |
| [Anmelde Name](external-attemptlogin.md)                         | Zeigt ein Dialogfeld an, damit der Benutzer versuchen kann, sich beim Online Shop anzumelden.                                                 |
| [authenticate](external-authenticate.md)                         | Initiiert den Versuch, den Benutzer zu authentifizieren.                                                                               |
| [auf](external-buy.md)                                           | Initiiert den Erwerb eines Satzes von Medien Elementen.                                                                              |
| [cancelnavigate](external-cancelnavigate.md)                     | Informiert Windows Media Player, dass eine neue Ermittlungs Seite auch dann nicht angezeigt werden soll, wenn sich die Ansicht im Player geändert hat. |
| [changeView](external-changeview.md)                             | Ändert die Ansicht in Windows Media Player.                                                                                    |
| [changeviewonlinelist](external-changeviewonlinelist.md)         | Ändert die Ansicht in Windows Media Player, um eine Liste anzuzeigen, die dynamisch vom Online Store generiert wurde.                        |
| [Herunterladen](external-download.md)                                 | Initiiert das Herunterladen eines Satzes von Medien Elementen.                                                                              |
| [Theater](external-play.md)                                         | Weist Windows Media Player an, einen Satz von Medien Elementen wiederzugeben.                                                                 |
| [savecurrentviewdelibrary](external-savecurrentviewtolibrary.md) | Erstellt eine Wiedergabeliste aus den Medien Elementen in der aktuellen Ansicht und speichert die Wiedergabeliste in der lokalen Bibliothek.                     |
| [SendMessage](external-sendmessage.md)                           | Sendet eine Meldung an das Plug-in des Online Stores.                                                                               |
| [showPopup](external-showpopup.md)                               | Weist Windows Media Player an, eine Popup Webseite anzuzeigen. Das heißt, eine Webseite, die in einem separaten Fenster angezeigt wird.            |



 

Das **externe** Objekt macht die folgenden Ereignisse für den Onlinespeicher vom Typ 1 verfügbar.



| Ereignis                                                                         | BESCHREIBUNG                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Onchangeviewerror](external-onchangeviewerror-event.md)                     | Tritt auf, wenn ein Aufrufvorgang der **externen. changeView** -Methode zu einem Fehler führt.           |
| [Onchangeviewonlinelisterror](external-onchangeviewonlinelisterror-event.md) | Tritt auf, wenn ein Aufrufvorgang der **externen. changeviewonlinelist** -Methode zu einem Fehler führt. |
| [Oncolorchange](external-oncolorchange-event.md)                             | Tritt auf, wenn sich die Farbe der Windows Media Player-Benutzeroberfläche ändert.               |
| [Onloginchange](external-onloginchange-event.md)                             | Tritt auf, wenn der Anmeldestatus des Benutzers geändert wird oder wenn der Anmeldeversuch fehlschlägt.        |
| [Onsendmessagecomplete](external-onsendmessagecomplete-event.md)             | Tritt auf, wenn der Online Shop die Verarbeitung einer Nachricht abgeschlossen hat.                         |
| [OnViewChange](external-onviewchange-event.md)                               | Tritt auf, wenn die Sicht in Windows-Media Player geändert wird.                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 1-Onlineshops**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




