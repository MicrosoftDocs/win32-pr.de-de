---
title: Bibliotheks Speicherort Konstanten
description: Bibliotheks Speicherort Konstanten
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Windows Media Player Online Stores, Bibliotheks Speicherort Konstanten
- Online Stores, Bibliotheks Speicherort Konstanten
- Typ 1 Online Stores, Bibliotheks Speicherort Konstanten
- Windows Media Player Online Stores, Standorte
- Online Stores, Standorte
- Typ 1 Online Stores, Standorte
- Windows Media Player Library, Location-Konstanten
- Bibliothek, Location-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cbb297831acce9724988309880390cdcbe1894
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390053"
---
# <a name="library-location-constants"></a>Bibliotheks Speicherort Konstanten

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die Bibliotheks Speicherort Konstanten sind globale Zeichen folgen Variablen, die in "Contentpartner. h" definiert sind. Sie werden von bestimmten Methoden der [iwmpcontentpartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) -und [iwmpcontentpartnercallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback) -Schnittstellen und von bestimmten Methoden des [externen](external-object-for-type-1-online-stores.md) Objekts verwendet. Diese Konstanten werden verwendet, um die folgenden Typen anzugeben.

-   Bibliotheks Location Type: Dies ist der Typ der Bibliotheks Ansicht, die von Windows Media Player angezeigt wird. Der Player zeigt z. b. möglicherweise eine Ansicht eines bestimmten Albums (g \_ szcpalbumid) oder die Ansicht aller Genres (g \_ szallcpgenreids) an.
-   Ausgewählter Elementtyp: Dies ist der Typ des Elements, das in der Bibliotheks Ansicht ausgewählt wurde. Beispielsweise kann der Benutzer ein bestimmtes Album (g \_ szcpalbumid) in der Ansicht aller Alben auswählen.
-   Listentyp: Dies ist der Typ der Liste, die vom Plug-in für den Inhalts Partner angefordert wird. Beispielsweise kann das Plug-in von Windows Media Player aufgefordert werden, eine Liste von Elementen bereitzustellen, die einer bestimmten Wiedergabeliste zugeordnet sind (g \_ szcplistid).
-   List Item Type: der Typ des einzelnen Listen Elements, das vom Inhalts Partner-Plug-in angefordert wird. Beispielsweise kann das Plug-in von Windows Media Player aufgefordert werden, die Liste der Spuren (g \_ szcptrackid) in einer bestimmten Wiedergabeliste anzugeben.

In der folgenden Tabelle werden der Name und der Wert der einzelnen Konstanten und eine kurze Beschreibung des Speicher Orts oder-Typs der Bibliothek angezeigt. In C-oder C++-Code, der mit der Header Datei Contentpartner. h kompiliert wird, können Sie entweder den Namen oder den Wert einer Konstanten verwenden. Die Verwendung des Namens ist vorzuziehen, da der Compiler falsche Schreibweise erkennt. In Skripts (z. b. beim Aufrufen der Methoden des [externen](external-object-for-type-1-online-stores.md) Objekts) ist es nicht möglich, den Namen einer Konstanten zu verwenden. Sie müssen den-Wert verwenden.



| Name                              | Wert                        | Speicherort oder Typ                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ szunknownlocation              | Unknownlocation              | Ein Satz von Spuren, der weder ein Album noch eine Wiedergabeliste ist. Windows Media Player verwendet diese Konstante auch im seltenen Fall, dass ein gültiger Speicherort nicht ermittelt werden kann. |
| g \_ szrootlocation                 | Rootlocation                 | Der oberste Knoten im Strukturansicht-Steuerelement der Bibliothek                                                                                                                      |
| g \_ szflyoutmenu                   | Flyoutmenu                   | Das Flyout-Menü des aktuellen Online Stores                                                                                                                             |
| g \_ szonlinestore                  | OnlineStore                  | Alle Online Stores                                                                                                                                                  |
| g \_ szcplistid                     | Cplistid                     | Eine einzelne Liste                                                                                                                                                 |
| g \_ szallcplistids                 | Allcplistids                 | Alle Listen                                                                                                                                                          |
| g \_ szcptrackid                    | Cptrackid                    | Eine einzelne Spur                                                                                                                                                |
| g \_ szallcptrackids                | Allcptrackids                | Alle Spuren                                                                                                                                                         |
| g \_ szcpartistid                   | Cpartistid                   | Ein einzelner Künstler                                                                                                                                               |
| g \_ szallcpartistids               | Allcpartistids               | Alle Künstler                                                                                                                                                        |
| g \_ szcpalbumid                    | Cpalbumid                    | Ein einzelnes Album                                                                                                                                                |
| g \_ szallcpalbumids                | Allcpalbumids                | Alle Alben                                                                                                                                                         |
| g \_ szcpgenreid                    | Cpgenreid                    | Ein einzelnes Genre                                                                                                                                                |
| g \_ szallcpgenreids                | Allcpgenreids                | Alle Genres                                                                                                                                                         |
| g \_ szcpalbumsubgenreid            | Cpalbumsubgenreid            | Ein einzelnes Subgenre                                                                                                                                             |
| g \_ szallcpalbumsubgenreids        | Allcpalbumsubgenreids        | Alle Subgenres                                                                                                                                                      |
| g \_ szreleasedateyear              | Releasedateyear              | Ein einzelnes Jahr, in dem Katalog Inhalte freigegeben wurden                                                                                                               |
| g \_ szallreleasedateyears          | Allreleasedateyears          | Alle Jahre, zu denen Katalog Inhalte freigegeben wurden                                                                                                                        |
| g \_ szcpradioid                    | Cpradioid                    | Ein einzelner Options Strom                                                                                                                                         |
| g \_ szallcpradioids                | Allcpradioids                | Alle Funk Datenströme                                                                                                                                                  |
| g \_ szauthor                       | Autor                       | Ein einzelner Autor                                                                                                                                               |
| g \_ szallauthors                   | Allauthors                   | Alle Autoren                                                                                                                                                        |
| g \_ szwmparametrialrating             | Wmpartalbewertung             | Eine einzelne Eltern Bewertung                                                                                                                                      |
| g \_ szallwmparameentalratings         | Allwmparametrialratings         | Alle Eltern Bewertungen                                                                                                                                               |
| g \_ szusereffectiveratingstars     | Usereffectiveratingstars     | Eine individuelle Benutzer Bewertung, gemessen als Anzahl von Sternen                                                                                                           |
| g \_ szallusereffectiveratingstarss | Allusereffectiveratingstarss | Alle Benutzerbewertungen                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Extern. AddIn-Korb**](external-addtobasket.md)
</dt> <dt>

[**Extern. kaufen**](external-buy.md)
</dt> <dt>

[**Extern. changeView**](external-changeview.md)
</dt> <dt>

[**Extern. changeviewonlinelist**](external-changeviewonlinelist.md)
</dt> <dt>

[**Extern. Download**](external-download.md)
</dt> <dt>

[**Extern. librarylocationtype**](external-librarylocationtype.md)
</dt> <dt>

[**Extern. Play**](external-play.md)
</dt> <dt>

[**Iwmpcontentpartner:: GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**Iwmpcontentpartner:: getlistcontents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**Iwmpcontentpartner:: GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**Iwmpcontentpartner:: InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**Iwmpcontentpartnercallback:: changeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




