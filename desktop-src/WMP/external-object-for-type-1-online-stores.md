---
title: Externes Objekt für Onlineshops vom Typ 1
description: Externes Objekt für Onlineshops vom Typ 1
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Windows Media Player Onlineshops, externe Objekte
- Onlineshops, externe Objekte
- Geben Sie 1 Onlineshops, externe Objekte ein.
- externe Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7d95d2ca332b88edea73da2238374aeffc52e520d7bc0346eab9f4eb7a05f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649000"
---
# <a name="external-object-for-type-1-online-stores"></a>Externes Objekt für Onlineshops vom Typ 1

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **External-Objekt** stellt Funktionen für Webseiten bereit, die von einem Onlineshop bereitgestellt werden, der in Windows Media Player gehostet wird.

Das **External-Objekt** macht die folgenden Eigenschaften für Onlineshops vom Typ 1 verfügbar.



| Eigenschaft                                                                                  | Beschreibung                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | Ruft den Kontotyp des aktuellen Benutzers ab.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | Ruft die aktuelle Hervorhebungsfarbe der Schaltfläche für die Windows Media Player Benutzeroberfläche ab.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | Ruft die aktuelle Schaltflächenzeigerfarbe für die Windows Media Player Benutzeroberfläche ab.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | Ruft die aktuelle Schaltflächenschattenfarbe für die Windows Media Player Benutzeroberfläche ab.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | Ruft die aktuelle dunkel schattierte Farbe der Windows Media Player Benutzeroberfläche ab.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | Ruft die aktuelle hell schattierte Farbe der Windows Media Player Benutzeroberfläche ab.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | Ruft die aktuelle mittelschattierte Farbe der Windows Media Player Benutzeroberfläche ab.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | Ruft den Titel der Schaltfläche im Listenbereich (auch als Warenkorb bezeichnet) in Windows Media Player ab.                                     |
| [filter](external-filter.md)                                                             | Ruft den derzeit von Windows Media Player verwendeten Suchfilter ab.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | Gibt an, ob Windows Media Player Internet Explorer Verlauf ignorieren soll.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Ruft den Bezeichner eines bestimmten Medienelements ab, das derzeit in der Ansicht des Players angezeigt wird.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | Ruft eine [Bibliotheksspeicherort-Konstante](library-location-constants.md) ab, die den Typ der aktuellen Ansicht in Windows Media Player angibt. |
| [pluginRunning](external-pluginrunning.md)                                               | Ruft einen Wert ab, der angibt, ob das Plug-In des Onlineshops ausgeführt wird.                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | Ruft den Bezeichner des Medienelements ab, das derzeit in Windows Media Player ausgewählt ist.                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | Ruft den Typ des Medienelements ab, das derzeit in Windows Media Player ausgewählt ist.                                                 |
| [Aufgabe](external-task.md)                                                                 | Ruft den Namen des aktuellen Aufgabenbereichs ab.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Gibt an, ob der von der aktuellen Ermittlungsseite dargestellte Feed im Strukturansichtssteuerelement der lokalen Bibliothek angezeigt wird.          |
| [userLoggedIn](external-userloggedin.md)                                                 | Ruft einen Wert ab, der angibt, ob der Benutzer beim Onlineshop angemeldet ist.                                                          |
| [version](external-version.md)                                                           | Ruft die aktuelle Version von Windows Media Player ab.                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | Ruft Parameter ab, die der aktuellen Ansicht in Windows Media Player zugeordnet sind.                                                           |



 

Das **External-Objekt** macht die folgenden Methoden für Onlineshops vom Typ 1 verfügbar.



| Methode                                                            | Beschreibung                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | Fügt dem Listenbereich (auch als Warenkorb bezeichnet) in Windows Media Player Medienelemente hinzu.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Zeigt ein Dialogfeld an, damit der Benutzer versuchen kann, sich beim Onlineshop anzumelden.                                                 |
| [Authentifizieren](external-authenticate.md)                         | Initiiert einen Versuch, den Benutzer zu authentifizieren.                                                                               |
| [kaufen](external-buy.md)                                           | Initiiert den Kauf eines Satzes von Medienelementen.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | Informiert Windows Media Player, dass keine neue Ermittlungsseite angezeigt werden soll, obwohl sich die Ansicht im Player geändert hat. |
| [changeView](external-changeview.md)                             | Ändert die Ansicht in Windows Media Player.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | Ändert die Ansicht in Windows Media Player, um eine dynamisch vom Onlineshop generierte Liste anzuzeigen.                        |
| [Herunterladen](external-download.md)                                 | Initiiert den Download eines Satzes von Medienelementen.                                                                              |
| [Spielen](external-play.md)                                         | Weist Windows Media Player an, eine Reihe von Medienelementen wiederzuspielen.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Erstellt eine Wiedergabeliste aus den Medienelementen in der aktuellen Ansicht und speichert die Wiedergabeliste in der lokalen Bibliothek.                     |
| [Sendmessage](external-sendmessage.md)                           | Sendet eine Nachricht an das Plug-In des Onlineshops.                                                                               |
| [showPopup](external-showpopup.md)                               | Weist Windows Media Player an, eine Popupwebseite anzuzeigen. Das heißt, eine Webseite, die in einem separaten Fenster angezeigt wird.            |



 

Das **External-Objekt** macht die folgenden Ereignisse für Onlineshops vom Typ 1 verfügbar.



| Ereignis                                                                         | Beschreibung                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Tritt ein, wenn ein Aufruf der **External.ChangeView-Methode** zu einem Fehler führt.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Tritt ein, wenn ein Aufruf der **External.ChangeViewOnlineList-Methode** zu einem Fehler führt. |
| [OnColorChange](external-oncolorchange-event.md)                             | Tritt ein, wenn sich die Farbe der Windows Media Player Benutzeroberfläche ändert.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Tritt ein, wenn sich der Anmeldestatus des Benutzers ändert oder ein Anmeldeversuch fehlschlägt.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Tritt ein, wenn der Onlineshop die Verarbeitung einer Nachricht abgeschlossen hat.                         |
| [OnViewChange](external-onviewchange-event.md)                               | Tritt ein, wenn sich die Ansicht in Windows Media Player ändert.                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz für Typ 1-Onlineshops**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




