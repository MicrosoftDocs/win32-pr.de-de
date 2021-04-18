---
title: Informationen zu Bibliothek Diensten
description: Informationen zu Bibliothek Diensten
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player Bibliothek, Informationen zu
- Windows Media Player-Bibliothek, Dienste
- Bibliothek, Dienste
- Bibliothek, Informationen zu
- Versionen von Windows Media Player, Bibliothek Dienste
- Enumerationen, Bibliotheksdienste
- Ereignisse, Bibliotheksdienste
- Beispiele, Bibliotheksdienste
- Schnittstellen, Bibliotheksdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743efc8ae5cb464aa38655314c52112bc9541de6
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106337637"
---
# <a name="about-library-services"></a>Informationen zu Bibliothek Diensten

In früheren Versionen von Windows Media Player hat die Software für jeden Benutzer eine einzelne Bibliotheks Datenbank verwendet. Diese Datenbank wurde auf dem Computer des Benutzers gespeichert und ist konzeptionell an den Benutzer und eine bestimmte Instanz des Players gebunden.

Windows Media Player 11 führt die Konzepte mehrerer-und-Remote Bibliotheken ein. Nun können Windows-Media Player zusätzlich zu der Standard-oder *lokalen* Bibliothek von Windows-Inhalt anzeigen, der von Bibliotheken auf anderen Computern abgerufen wird, die mit einem Netzwerk verbunden sind. dazu gehören möglicherweise andere Benutzer, die am gleichen Computer angemeldet sind. Der Player kann auch Bibliotheks Ansichten aus anderen Quellen, z. b. mtp-aktivierten Geräten oder Daten-CDs, anzeigen. Aus Sicht des Endbenutzers bedeutet dies, dass der Inhalt digitaler Medien, der sich an vielen unterschiedlichen Stellen befindet, über dieselbe, vertraute Windows Media Player-Benutzeroberfläche von mehreren Standorten aus verwaltet werden kann. Aus der Sicht des Entwicklers bedeutet dies, dass Sie die Windows Media Player SDK-com-Schnittstellen verwenden können, um die verfügbaren Bibliotheken aufzulisten und Sie dann wie die lokale Bibliothek in früheren Versionen zu verwenden.

Um die verfügbaren Bibliotheken aufzulisten, verwenden Sie die **iwmplibraryservices** -Schnittstelle. Diese Schnittstelle macht die [iwmplibraryservices:: getzählbytype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) -Methode verfügbar, die die Anzahl der Bibliotheken eines bestimmten Typs abruft. Bibliothekstypen werden von der [wmplibrarytype](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) -Enumeration definiert. Diese Enumeration enthält einen Wert für die lokale Bibliothek, wmpltlocal. Dies liegt daran, dass die Funktion "Bibliotheksdienste" Ihnen immer ermöglicht, mit der lokalen Bibliothek zu arbeiten, indem Sie **iwmplibraryservices** und die zugehörigen Schnittstellen verwenden.

> [!Note]  
> Die **wmplibrarytype** -Enumeration enthält den Wert wmpltreapte, der vom Netzwerk freigegebene Medienbibliotheken darstellt. Um auf diese freigegebenen Bibliotheken zuzugreifen, muss das Player-Steuerelement im Remote Modus ausgeführt werden. Weitere Informationen zum Ausführen des Player-Steuer Elements im Remote Modus finden Sie unter [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).

 

Nachdem Sie die Anzahl der Bibliotheken abgerufen haben, können Sie die Auflistung der verfügbaren Bibliotheken durchlaufen, indem Sie in einer Schleife wiederholt [iwmplibraryservices:: getlibrarybytype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) aufrufen und bei jeder Iterationen einen neuen Indexwert übergeben. Diese Methode ruft einen Zeiger auf eine [iwmplibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) -Schnittstelle ab, die die jeweilige Bibliothek darstellt.

Nachdem Sie einen Zeiger auf **iwmplibrary** abgerufen haben, können Sie [iwmplibrary:: get \_ mediacollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) aufrufen, um einen Zeiger auf eine **iwmpmediacollection** -Schnittstelle abzurufen. Mit diesem Schnittstellen Zeiger können Sie mit einer einzelnen Bibliothek arbeiten, ähnlich wie bei Verwendung der lokalen Bibliothek. Sie können auch eine Zeichenfolge mit dem Namen der Bibliothek abrufen, indem Sie [iwmplibrary:: get \_ Name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name)aufrufen. Dies ist hilfreich, wenn Sie den Namen der Bibliothek dem Benutzer anzeigen müssen. Sie können den [ \_ Typ iwmplibrary:: Get](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) aufrufen, um den **wmplibrarytype** einer bestimmten Bibliothek abzurufen.

Sie können das [IWMPEvents3:: libraryconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) -Ereignis behandeln, um zu ermitteln, wann eine Bibliothek verfügbar ist, und das [IWMPEvents3:: librarydisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) -Ereignis, um zu erfahren, wann eine Bibliothek die Verbindung trennt. Jedes dieser Ereignisse stellt einen **iwmplibrary** -Zeiger bereit, der die Bibliothek darstellt, die verbunden oder getrennt ist. Sie können [iwmplibrary:: isidentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) anrufen, um zu bestimmen, ob die Bibliothek, die verbunden oder getrennt ist, eine zurzeit verwendete Bibliothek ist.

Es gibt einige wichtige Unterschiede bei der Arbeit mit einer Bibliothek, die über die **iwmplibraryservices** -Schnittstelle abgerufen wird, im Vergleich zum Arbeiten mit einer Bibliothek, die mithilfe von [iwmpcore:: get \_ mediacollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection)abgerufen wurde. Es liegen folgende Unterschiede vor:

-   Sie können Abfrageergebnisse in der Regel viel schneller aus Bibliotheken abrufen, die über **iwmplibraryservices** abgerufen werden. (Dies setzt voraus, dass andere Faktoren, z. b. Netzwerk-und Festplattenzugriffs Zeiten, gleich sind.)
-   Die Liste der Metadaten-Attribute für Medienelemente, die von Bibliotheken verfügbar sind, die über **iwmplibraryservices** abgerufen werden, ist in der Regel eine Teilmenge der in der lokalen Bibliothek verfügbaren Metadatenattribute, [die über](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)
-   Wenn Sie die lokale Bibliothek über **iwmplibraryservices** abrufen, sind dieselben Attribute für ihre Verwendung verfügbar, wenn Sie die lokale Bibliothek über **iwmpcore** abrufen. Allerdings können Sie Abfrageergebnisse für die am häufigsten verwendeten Attribute viel schneller abrufen.
-   Sie sollten Zeichen folgen Auflistungen verwenden, um Benutzeroberflächen Elemente zu erstellen, wenn Sie mit Bibliotheken arbeiten, die über **iwmplibraryservices** abgerufen werden. Beispielsweise können Sie mit [IWMPMediaCollection2:: getstringcollectionbyquery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) eine benutzerdefinierte Abfrage (die durch die **iwmpquery** -Schnittstelle dargestellt wird) verwenden, um eine Zeichen folgen Auflistung abzurufen.
-   Remote Bibliotheken, die über die **iwmplibraryservices** -Schnittstelle abgerufen werden, sind möglicherweise nicht immer mit der aktuellen Player Instanz verbunden. Dies bedeutet, dass es wichtig ist, die Ereignisse **libraryconnect** und **librarydisconnect** zu behandeln, um zu ermitteln, wann die Bibliotheks Verfügbarkeit geändert wird, und um das [IWMPEvents3:: stringcollectionchange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) -Ereignis zu behandeln, um zu erfahren, wann Zeichen folgen Auflistungen zum Anzeigen von Benutzeroberflächen Elementen hinzugefügt oder daraus entfernt werden. Sie sollten auch **stringcollectionchange** -Ereignisse für die lokale Bibliothek aus ähnlichen Gründen verarbeiten.

Es ist wichtig zu verstehen, dass sich Zeichen folgen Auflistungen für eine bestimmte Bibliothek jederzeit ändern können. Eine Zeichen folgen Auflistung ist möglicherweise leer, wenn Sie Sie zum ersten Mal abrufen, wie im Fall einer Bibliothek, die vor kurzem verbunden war, der Player aber noch nicht seinen Inhalt aufgelistet hat. Umgekehrt kann eine Zeichen folgen Auflistung bereits alle benötigten Informationen enthalten. In diesem Fall erhalten Sie möglicherweise nie ein **stringcollectionchange** -Ereignis, da der Inhalt der Bibliothek vollständig aufgezählt wurde, bevor Sie die Abfrage erstellt haben, und nichts anderes geändert wird.

Um die Benutzeroberfläche auf dem neuesten Stand zu halten, müssen Sie daher den Inhalt der Zeichen folgen Auflistung auflisten, wenn Sie die **iwmpstringcollection** -Schnittstelle abrufen und das **stringcollectionchange** -Ereignis behandeln, um über Updates zu informieren, wenn Sie auftreten.

## <a name="sample"></a>Beispiel

Das Beispiel mit dem Namen wmpml veranschaulicht, wie Sie mit Bibliothek Diensten arbeiten. Weitere Informationen zu Windows Media Player SDK-Beispielen finden Sie unter [Beispiele](samples.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Bibliothek**](about-the-library.md)
</dt> <dt>

[**Informationen zum Query-Objekt**](about-the-query-object.md)
</dt> <dt>

[**IWMPEvents3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Iwmplibrary-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[**Iwmplibrary-Schnittstelle (VB und c#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Iwmplibraryservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[**Iwmplibraryservices-Schnittstelle (VB und c#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Iwmpstringcollection-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[**Iwmpstringcollection-Schnittstelle (VB und c#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Iwmpquery-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[**Iwmpquery-Schnittstelle (VB und c#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Arbeiten mit der Bibliothek**](working-with-the-library.md)
</dt> </dl>

 

 




