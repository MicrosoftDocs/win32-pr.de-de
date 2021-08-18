---
title: Speicherortkonstanten der Bibliothek
description: Speicherortkonstanten der Bibliothek
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Windows Media Player Onlineshops, Speicherortkonstanten der Bibliothek
- Onlineshops, Speicherortkonstanten der Bibliothek
- Typ 1 Onlineshops, Speicherortkonstanten der Bibliothek
- Windows Media Player Onlineshops, Standorte
- Onlineshops, Standorte
- Geben Sie 1 Onlineshops, Standorte ein.
- Windows Media Player Bibliothek, Speicherortkonstanten
- Bibliothek, Speicherortkonstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a677f405ff36030647618a83bd0b8b952dae254a756cebc48e4c3210e5fcde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135363"
---
# <a name="library-location-constants"></a>Speicherortkonstanten der Bibliothek

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die Speicherortkonstanten der Bibliothek sind globale Zeichenfolgenvariablen, die in contentpartner.h definiert sind. Sie werden von bestimmten Methoden der [Schnittstellen IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) und [IWMPContentPartnerCallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback) sowie von bestimmten Methoden des [externen](external-object-for-type-1-online-stores.md) Objekts verwendet. Diese Konstanten werden verwendet, um die folgenden Typen anzugeben.

-   Bibliotheksspeicherorttyp: Dies ist der Typ der Bibliotheksansicht, die von Windows Media Player angezeigt wird. Beispielsweise zeigt der Player möglicherweise eine Ansicht eines bestimmten Albums (g \_ szCPKategorieID) oder die Ansicht aller Genre (g \_ szAllCPGenreIDs) an.
-   Ausgewählter Elementtyp: Dies ist der Typ des in der Bibliotheksansicht ausgewählten Elements. Beispielsweise kann der Benutzer ein bestimmtes Album (g \_ szCPLädtID) in der Ansicht aller Alben auswählen.
-   Listentyp: Dies ist der Typ der Liste, die vom Inhaltspartner-Plug-In angefordert wird. Beispielsweise kann Windows Media Player das Plug-In bitten, eine Liste von Elementen zu liefern, die einer bestimmten Wiedergabeliste zugeordnet sind (g \_ szCPListID).
-   Listenelementtyp: Der Typ des einzelnen Listenelements, das vom Inhaltspartner-Plug-In angefordert wird. Beispielsweise kann Windows Media Player das Plug-In bitten, die Liste der Spuren (g \_ szCPTrackID) in einer bestimmten Wiedergabeliste zu liefern.

Die folgende Tabelle enthält den Namen und wert jeder Konstante sowie eine kurze Beschreibung des Speicherorts oder Typs der Bibliothek. In C- oder C++-Code, der mit der Headerdatei contentpartner.h kompiliert wird, können Sie entweder den Namen oder den Wert einer Konstante verwenden. Die Verwendung des Namens ist vorzuziehen, da der Compiler Rechtschreibfehler erkennt. Im Skript (z. B. beim Aufrufen der Methoden des [externen](external-object-for-type-1-online-stores.md) Objekts) können Sie den Namen einer Konstante nicht verwenden. Sie müssen den Wert verwenden.



| Name                              | Wert                        | Speicherort oder Typ                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ szUnknownLocation              | UnknownLocation              | Eine Reihe von Spuren, die weder ein Album noch eine Wiedergabeliste sind. Windows Media Player verwendet diese Konstante auch im seltenen Fall, dass sie keinen gültigen Speicherort bestimmen kann. |
| g \_ szRootLocation                 | RootLocation                 | Der oberste Knoten im Bibliotheksstrukturansicht-Steuerelement                                                                                                                      |
| g \_ szFlyoutMenu                   | FlyoutMenu                   | Flyoutmenü des aktuellen Onlineshops                                                                                                                             |
| g \_ szOnlineStore                  | OnlineStore                  | Alle Onlineshops                                                                                                                                                  |
| g \_ szCPListID                     | CPListID                     | Eine einzelne Liste                                                                                                                                                 |
| g \_ szAllCPListIDs                 | AllCPListIDs                 | Alle Listen                                                                                                                                                          |
| g \_ szCPTrackID                    | CPTrackID                    | Eine einzelne Spur                                                                                                                                                |
| g \_ szAllCPTrackIDs                | AllCPTrackIDs                | Alle Spuren                                                                                                                                                         |
| g \_ szCPArtistID                   | CPArtistID                   | Ein einzelner Interpret                                                                                                                                               |
| g \_ szAllCPArtistIDs               | AllCPArtistIDs               | Alle Interpreten                                                                                                                                                        |
| g \_ szCPIedID                    | CPIedID                    | Ein einzelnes Album                                                                                                                                                |
| g \_ szAllCPObjektiDs                | AllCPBeständeIDs                | Alle Alben                                                                                                                                                         |
| g \_ szCPGenreID                    | CPGenreID                    | Ein einzelnes Genre                                                                                                                                                |
| g \_ szAllCPGenreIDs                | AllCPGenreIDs                | Alle"-1600                                                                                                                                                         |
| g \_ szCPIedSubGenreID            | CPIedSubGenreID            | Ein einzelner Untergenerre                                                                                                                                             |
| g \_ szAllCPKategorieSubGenreIDs        | AllCPKategorieSubGenreIDs        | Alle Untergenres                                                                                                                                                      |
| g \_ szReleaseDateYear              | ReleaseDateYear              | Ein einzelnes Jahr, in dem Kataloginhalte veröffentlicht wurden                                                                                                               |
| g \_ szAllReleaseDateYears          | AllReleaseDateYears          | Alle Jahre, in denen Kataloginhalte veröffentlicht wurden                                                                                                                        |
| g \_ szCPRadioID                    | CPRadioID                    | Ein einzelner Radiostream                                                                                                                                         |
| g \_ szAllCPRadioIDs                | AllCPRadioIDs                | Alle Radiostreams                                                                                                                                                  |
| g \_ szAuthor                       | Autor                       | Ein einzelner Autor                                                                                                                                               |
| g \_ szAllAuthors                   | AllAuthors                   | Alle Autoren                                                                                                                                                        |
| g \_ szWMParentalRating             | WMParentalRating             | Eine individuelle Elternbewertung                                                                                                                                      |
| g \_ szAllWMParentalRatings         | AllWMParentalRatings         | Alle Bewertungen von Eltern                                                                                                                                               |
| g \_ szUserEffectiveRatingStars     | UserEffectiveRatingStars     | Eine individuelle Benutzerbewertung, gemessen als Anzahl von Sternen                                                                                                           |
| g \_ szAllUserEffectiveRatingStarss | AllUserEffectiveRatingStarss | Alle Benutzerbewertungen                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**External.addToBasket**](external-addtobasket.md)
</dt> <dt>

[**External.buy**](external-buy.md)
</dt> <dt>

[**External.changeView**](external-changeview.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.download**](external-download.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External.play**](external-play.md)
</dt> <dt>

[**IWMPContentPartner::GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**IWMPContentPartner::InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**IWMPContentPartnerCallback::ChangeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




