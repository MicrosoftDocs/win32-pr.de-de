---
title: Bibliotheks Integration
description: Bibliotheks Integration
ms.assetid: 6ff1b379-983b-4cd7-8142-27523a7a03e7
keywords:
- Windows Media Player Online Stores, Bibliotheks Integration
- Online Stores, Bibliotheks Integration
- Typ 1 Online Stores, Bibliotheks Integration
- Windows Media Player Online Stores, Aufgabenbereiche
- Online Stores, Aufgabenbereiche
- Typ 1 Online Stores, Aufgabenbereiche
- Windows Media Player, Aufgabenbereiche
- Windows Media Player-Bibliothek, Integration
- Bibliothek, Integration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5353aba7099acd2dfd08596be7ffd43503bdad91
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389891"
---
# <a name="library-integration"></a>Bibliotheks Integration

Die Windows Media Player-Benutzeroberfläche ist in Featurebereiche unterteilt, die als *Aufgaben* Bereiche bezeichnet werden, die die verschiedenen Funktionen des Programms auf hoher Ebene Kapseln. Hierzu gehören die Aufgabenbereiche " **Bibliothek**", " **Synchronisieren**" und " **Brennen** " (u.a.). Der Aufgabenbereich " **Bibliothek** " ermöglicht es Benutzern, mit der Bibliothek zu arbeiten. im Aufgabenbereich " **Synchronisieren** " können Benutzer digitale Mediendateien mit einem tragbaren Gerät synchronisieren. der Aufgabenbereich " **Burn** " ermöglicht Benutzern das Brennen digitaler Mediendateien auf eine CD oder DVD.

> [!Note]  
> Der Aufgabenbereich **Bibliothek** wird manchmal auch als Aufgabenbereich **Durchsuchen** bezeichnet.

 

Jeder dieser Aufgabenbereiche verfügt über ein gewisses Maß an Integration in die Bibliothek. Wenn der Benutzer beispielsweise Musik auf eine CD brennen möchte, ist es sinnvoll, die zu löschender Musik auszuwählen, indem Sie die Bibliothek durchsuchen und einfach Medienelemente in eine Liste ziehen und dort ablegen. Dies bedeutet, dass Benutzer einen Online Store-Katalog anzeigen und verwenden können, der vollständig in die Bibliothek integriert ist, wenn Sie in den Aufgabenbereichen **Bibliothek**, **Sync** und **Brennen** arbeiten. Die [wmptasktype](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype) -Enumeration enthält Werte, die diese drei Aufgabenbereiche darstellen, sodass Sie Programm gesteuert identifiziert werden können.

Jeder dieser drei Aufgabenbereiche ist in drei Hauptbereiche unterteilt. Der erste Teil ist das Bibliotheksstruktur Ansicht-Steuerelement. Dieses Steuerelement stellt dem Benutzer eine hierarchische Ansicht der Windows Media Player-Bibliothek bereit, einschließlich der Kategorisierungsfunktionen nach Gesang, Interpreten, Album usw. Der zweite Aufgabenbereich ist der Detailbereich. Dieser Bereich enthält ausführliche Informationen, die entsprechend der Kategorie angeordnet sind, die derzeit im Strukturansicht-Steuerelement der Bibliothek ausgewählt ist. Wenn der Benutzer z. b. in der Struktur **Ansicht auf die Titel geklickt hat** , werden im Detailbereich die derzeit in der Bibliothek angezeigten Titel Titel zusammen mit anderen Informationen, wie z. b. Länge und Titel des Albums, angezeigt. Der dritte Teil ist der Listen Bereich oder der *Warenkorb*. Benutzer können Medienelemente per Drag & Drop auf den Warenkorb verschieben, um Listen zu erstellen, z. b. Wiedergabelisten, Synchronisierungs Listen und Verbrauchs Listen.

Wenn ein Online Store-Katalog in die Bibliothek integriert ist, wird der Online Shop als Kategorie oder *Knoten* der obersten Ebene im Strukturansicht-Steuerelement der Bibliothek angezeigt. (Für den Benutzer ist jeweils nur ein Online Store-Katalog sichtbar.) Wenn ein Benutzer sich entscheidet, den Online Store-Katalog durch Klicken auf den Knoten anzuzeigen, werden im Detailbereich Informationen über die Musik im Online Store-Katalog angezeigt. Dies schließt Musik ein, die der Benutzer gekauft oder gemietet hat, und auch Musik, die der Benutzer noch nicht erworben hat.

Der Online Store-Knoten der obersten Ebene verfügt über eine Reihe von untergeordneten Knoten, die von Windows Media Player bereitgestellt werden. Beispielsweise verfügt der Online Store-Knoten der obersten Ebene unter anderem über die untergeordneten Knoten Radio, Artist und Album. Der Online Store-Knoten der obersten Ebene kann auch bis zu acht benutzerdefinierte untergeordnete Knoten enthalten, die vom Online Store bereitgestellt werden. In Windows Media Player wird ein benutzerdefinierter untergeordneter Knoten für jede Liste erstellt, die über einen Listen Bezeichner im Bereich von 0 bis 7 verfügt. Der Online Shop gibt den Bezeichner einer Liste in der [list.csv](list-csv.md) Datei an, die Teil des Katalog Katalogs ist.

Windows Media Player Ruft ein Symbol für jeden der benutzerdefinierten Struktur Knoten des Online Stores durch Aufrufen von [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)ab und übergibt cplistidische im *bstrinfoname* -Parameter.

Wenn der Benutzer durch den Katalog navigiert, führt Windows Media Player den Aufruf von **iwmpcontentpartner:: getiteminfo** aus, um Metadaten aus dem Content Partner-Plug-in über die Musik Elemente abzurufen, die der Benutzer auswählt. Diese Metadaten stellen dem Player Informationen zur Verfügung, damit der Spieler Details zu den Katalog Elementen anzeigen kann. Wenn der Benutzer z. b. ein Album auswählt, ruft Windows Media Player die Album-Art-URL ab, sodass der Benutzer das Albumcover-Grafik sehen kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> </dl>

 

 




