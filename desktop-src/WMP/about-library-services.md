---
title: Informationen zu Bibliotheksdiensten
description: Informationen zu Bibliotheksdiensten
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Windows Media Player,Library
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell,Bibliothek
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobiles ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobil, Bibliothek für Objektmodell
- Windows Media Player-Bibliothek, Informationen
- Windows Media Player Bibliothek, Dienste
- Bibliothek, Dienste
- library,about
- Versionen von Windows Media Player,Bibliotheksdienste
- Enumerationen, Bibliotheksdienste
- Ereignisse, Bibliotheksdienste
- Beispiele,Bibliotheksdienste
- Schnittstellen, Bibliotheksdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc6f073fa4c361f114589e080145a3cb3bb0a8c78736ba2dd1464332a7f7adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004512"
---
# <a name="about-library-services"></a>Informationen zu Bibliotheksdiensten

In früheren Versionen von Windows Media Player verwendete die Software für jeden Benutzer eine einzelne Bibliotheksdatenbank. Diese Datenbank wurde auf dem Computer des Benutzers gespeichert und konzeptionell an den Benutzer und eine bestimmte Instanz des Players gebunden.

Windows Media Player 11 werden die Konzepte mehrerer und Remotebibliotheken eingeführt. Zusätzlich zur standard- oder *lokalen*-Bibliothek können Windows Media Player nun Inhalte anzeigen, die von Bibliotheken auf anderen Computern abgerufen wurden, die mit einem Netzwerk verbunden sind. Dies kann auch andere Benutzer umfassen, die am selben Computer angemeldet sind. Der Player kann auch Bibliotheksansichten aus anderen Quellen anzeigen, z. B. MTP-fähige Geräte oder Daten-CDs. Aus Sicht des Endbenutzers bedeutet dies, dass digitale Medieninhalte, die sich an vielen verschiedenen Orten befinden, von mehreren Standorten aus verwaltet werden können, indem die gleiche vertraute Windows Media Player Benutzeroberfläche verwendet wird. Aus Sicht des Entwicklers bedeutet dies, dass Sie die COM-Schnittstellen des Windows Media Player SDK verwenden können, um die verfügbaren Bibliotheken aufzuzählen und sie dann wie die lokale Bibliothek in früheren Versionen zu verwenden.

Um die verfügbaren Bibliotheken aufzuzählen, verwenden Sie die **IWMPLibraryServices-Schnittstelle.** Diese Schnittstelle macht die [IWMPLibraryServices::getCountByType-Methode](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) verfügbar, die die Anzahl der Bibliotheken eines bestimmten Typs abruft. Bibliothekstypen werden durch die [WMPLibraryType-Enumeration](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) definiert. Diese Enumeration enthält einen Wert für die lokale Bibliothek wmpltLocal. Dies liegt daran, dass Sie mithilfe des Features "Bibliotheksdienste" immer mit der lokalen Bibliothek arbeiten können, indem **Sie IWMPLibraryServices** und die zugehörigen Schnittstellen verwenden.

> [!Note]  
> Die **WMPLibraryType-Enumeration** enthält den Wert wmpltRemote, der medienbibliotheken darstellt, die vom Netzwerk gemeinsam genutzt werden. Um auf diese freigegebenen Bibliotheken zugreifen zu können, muss das Player-Steuerelement im Remotemodus ausgeführt werden. Informationen zum Ausführen des Player-Steuerelements im Remotemodus finden Sie unter [Remoting des Windows Media Player Control](remoting-the-windows-media-player-control.md).

 

Nachdem Sie die Bibliotheksanzahl abgerufen haben, können Sie die Auflistung der verfügbaren Bibliotheken durchlaufen, indem [Sie wiederholt IWMPLibraryServices::getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) in einer Schleife aufrufen und bei jeder Iteration einen neuen Indexwert übergeben. Diese Methode ruft einen Zeiger auf eine [IWMPLibrary-Schnittstelle](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) ab, die die einzelne Bibliothek darstellt.

Nachdem Sie einen Zeiger auf **IWMPLibrary** abgerufen haben, können Sie [IWMPLibrary::get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) aufrufen, um einen Zeiger auf eine **IWMPMediaCollection-Schnittstelle** abzurufen. Mit diesem Schnittstellenzeiger können Sie ähnlich wie bei der Verwendung der lokalen Bibliothek mit einer einzelnen Bibliothek arbeiten. Sie können auch eine Zeichenfolge abrufen, die den Namen der Bibliothek enthält, indem Sie [IWMPLibrary::get \_ name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name)aufrufen. Dies ist hilfreich, wenn Sie den Bibliotheksnamen dem Benutzer anzeigen müssen. Sie können [IWMPLibrary::get \_ type](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) aufrufen, um den **WMPLibraryType** einer bestimmten Bibliothek abzurufen.

Sie können das [IWMPEvents3::LibraryConnect-Ereignis](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) behandeln, um zu wissen, wann eine Bibliothek verfügbar wird, und das [IWMPEvents3::LibraryDisconnect-Ereignis,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) um zu wissen, wann eine Bibliothek getrennt wird. Jedes dieser Ereignisse stellt einen **IWMPLibrary-Zeiger** bereit, der die Bibliothek darstellt, die verbunden oder getrennt wurde. Sie können [IWMPLibrary::isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) aufrufen, um zu bestimmen, ob es sich bei der Bibliothek, die verbunden oder getrennt wurde, um eine Bibliothek handelt, die Sie derzeit verwenden.

Es gibt einige wichtige Unterschiede bei der Arbeit mit einer Bibliothek, die über die **IWMPLibraryServices-Schnittstelle** abgerufen wurde, im Vergleich zur Arbeit mit einer Bibliothek, die mithilfe von [IWMPCore::get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection)abgerufen wurde. Es liegen folgende Unterschiede vor:

-   Abfrageergebnisse können in der Regel viel schneller aus Bibliotheken abgerufen werden, die über **IWMPLibraryServices** abgerufen werden. (Dies setzt voraus, dass andere Faktoren, z. B. Netzwerk- und Festplattenzugriffszeiten, gleich sind.)
-   Die Liste der Metadatenattribute für Medienelement, die von Bibliotheken verfügbar sind, die über **IWMPLibraryServices** abgerufen werden, ist in der Regel eine Teilmenge derjenigen, die aus der lokalen Bibliothek verfügbar sind, die über [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)abgerufen wurde.
-   Wenn Sie die lokale Bibliothek über **IWMPLibraryServices** abrufen, stehen ihnen alle Attribute zur Verfügung, die Sie auch beim Abrufen der lokalen Bibliothek über **IWMPCore** verwenden können. Allerdings können Sie Abfrageergebnisse für die am häufigsten verwendeten Attribute viel schneller abrufen.
-   Sie sollten Zeichenfolgenauflistungen verwenden, um Benutzeroberflächenelemente zu erstellen, wenn Sie mit Bibliotheken arbeiten, die über **IWMPLibraryServices** abgerufen wurden. Mit [IWMPMediaCollection2::getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) können Sie beispielsweise eine benutzerdefinierte Abfrage (dargestellt durch die **IWMPQuery-Schnittstelle)** verwenden, um eine Zeichenfolgenauflistung abzurufen.
-   Remotebibliotheken, die über die **IWMPLibraryServices-Schnittstelle** abgerufen werden, sind möglicherweise nicht immer mit der aktuellen Player-Instanz verbunden. Dies bedeutet, dass es wichtig ist, die **Ereignisse LibraryConnect** und **LibraryDisconnect** zu behandeln, um zu wissen, wann sich die Bibliotheksverfügbarkeit ändert, und das [IWMPEvents3::StringCollectionChange-Ereignis](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) zu behandeln, um zu wissen, wann Zeichenfolgen den Zeichenfolgenauflistungen hinzugefügt oder daraus entfernt werden, die Sie zum Anzeigen von Benutzeroberflächenelementen verwenden. Aus ähnlichen Gründen sollten Sie auch **StringCollectionChange-Ereignisse** für die lokale Bibliothek behandeln.

Es ist wichtig zu verstehen, dass Zeichenfolgenauflistungen für eine bestimmte Bibliothek jederzeit geändert werden können. Eine Zeichenfolgenauflistung kann beim ersten Abrufen leer sein, wie im Fall einer Bibliothek, die vor Kurzem verbunden wurde, aber der Player noch nicht ihren Inhalt aufzählt. Im Gegensatz dazu enthält eine Zeichenfolgenauflistung möglicherweise bereits alle benötigten Informationen. In diesem Fall erhalten Sie möglicherweise nie ein **StringCollectionChange-Ereignis,** da der Inhalt der Bibliothek vollständig aufzählt wurde, bevor Sie Ihre Abfrage erstellt haben und sich nichts anderes ändert.

Daher müssen Sie die Inhalte der Zeichenfolgenauflistung aufzählen, wenn Sie die **IWMPStringCollection-Schnittstelle** abrufen, und das **StringCollectionChange-Ereignis** behandeln, um informationen zu Updates zu erhalten, wenn sie auftreten.

## <a name="sample"></a>Beispiel

Das Beispiel mit dem Namen WMPML veranschaulicht die Arbeit mit Bibliotheksdiensten. Weitere Informationen zu Windows Media Player SDK-Beispielen finden Sie unter [Beispiele.](samples.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Bibliothek**](about-the-library.md)
</dt> <dt>

[**Informationen zum Abfrageobjekt**](about-the-query-object.md)
</dt> <dt>

[**IWMPEvents3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**IWMPLibrary-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[**IWMPLibrary-Schnittstelle (VB und C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**IWMPLibraryServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[**IWMPLibraryServices-Schnittstelle (VB und C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[**IWMPStringCollection-Schnittstelle (VB und C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPQuery-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[**IWMPQuery-Schnittstelle (VB und C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 




