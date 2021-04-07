---
title: Windows Media Player Online Stores
description: Windows Media Player Online Stores
ms.assetid: 81009d7b-5c2a-4447-a85e-138ab7834b7a
keywords:
- Windows Media Player Online Stores, Informationen zu
- Online Stores, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55046508b1e3a4d0a3a254fd294e5f271a2802f5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724075"
---
# <a name="windows-media-player-online-stores"></a>Windows Media Player Online Stores

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Windows Media Player stellt Funktionen bereit, mit denen die Anbieter von digitalen Medieninhalten ihre Dienste in Windows Media Player integrieren können. Die Integration zwischen dem Player und einem digitalen Online Medien Speicher bietet eine angenehme, umfassende Benutzerfreundlichkeit, einschließlich der Möglichkeit, Inhalte zu finden, Dateien herunterzuladen und zu verwalten, Inhalte wiederzugeben und Inhalte auf CDs oder Geräte zu kopieren.

## <a name="contacting-microsoft"></a>Kontaktaufnahme mit Microsoft

Wenn Sie möchten, dass Ihr digitaler Online Medien Speicher in Windows Media Player integriert wird, Sie aber noch keinen Kontakt mit Microsoft hergestellt haben, können Sie zunächst eine e-Mail an das virtuelle Windows Media Player Services-Team senden. Die e-Mail-Adresse des Teams lautet mpsvctm@microsoft.com .

## <a name="for-more-information"></a>Weitere Informationen

Technische Anleitungen zur Verwendung einer Vielzahl von Windows Media SDOs zum Erstellen eines Dienstanbieter, der lizenzierte Digital Media-Inhalte bietet, finden Sie im [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx) , und suchen Sie nach "Erstellen eines Windows Media Player 10-Abonnements Online Store".

## <a name="online-stores-in-windows-media-player-9-series"></a>Online Stores in Windows Media Player 9-Serie

In der Windows Media Player 9-Serie wurde das Konzept von Online Stores eingeführt. In der Windows Media Player 9-Serie konnten Online Store-Anbieter ihre Dienste in das **Premium-Dienst** Feature von Windows Media Player integrieren.

## <a name="online-stores-in-windows-media-player-10"></a>Online Stores in Windows Media Player 10

In Windows Media Player 10 wurden Premium-Dienste in Online Stores umbenannt, und die folgenden neuen Features wurden hinzugefügt:

-   Windows Media Player stellt bis zu drei Aufgabenbereiche für die Verwendung im Online Store bereit.
-   Wenn ein Benutzer in der Benutzeroberfläche des Players auswählt, um weitere Informationen zum Inhalt digitaler Medien anzuzeigen, ruft Windows Media Player im Online Store auf, um die Informationen bereitzustellen.
-   Wenn der Benutzer in der Benutzeroberfläche des Players einen Medien Eintrag kauft, ruft Windows Media Player im Online Store auf, um den Kauf abzuschließen.
-   Der Online Shop kann ein Plug-in bereitstellen, das Windows Media Player Unterstützung bei Digital Rights Management und die zeitliche Steuerung der Hintergrundverarbeitung aufruft.
-   Online Stores können mit der Windows Media Player-Einrichtung integriert werden.

## <a name="online-stores-in-windows-media-player-11"></a>Online Stores in Windows Media Player 11

Windows Media Player 11 führt einen neuen Online Musik Store ein, der tiefer in die Benutzeroberfläche des Players integriert ist. In Windows Media Player 11 wurden die folgenden neuen Features hinzugefügt, um diesen neuen Online Store zu unterstützen.

-   Windows Media Player lädt den Medienkatalog des Online Stores herunter, sodass der Benutzer den Inhalt des Online Stores schnell durchsuchen kann.
-   Windows Media Player zeigt den Musik Inhalt des Online Stores im Bibliotheksstruktur Ansicht-Steuerelement an.
-   Wenn der Benutzer die Benutzeroberfläche des Players navigiert, ruft der Spieler den Online Store auf, um Webseiten bereitzustellen, die die Benutzerfreundlichkeit verbessern.
-   Der Online Shop bietet ein Plug-in, das alle Aspekte der Kommunikation zwischen Windows Media Player und dem Online Store behandelt. Beispielsweise übernimmt das Plug-in den Anmelde Namen, die Lizenz Erneuerung, das Katalog Upgrade, das Herunterladen von Inhalten und den Einkauf von Inhalten.
-   Windows Media Player bietet eine verbesserte Kommunikation zwischen dem Player und Webseiten, die vom Online Store bereitgestellt und im Player gehostet werden.

## <a name="types-of-online-stores"></a>Typen von Online Stores

Es gibt zwei Arten von Online Stores: Typ 1 und Typ 2.

Ein Typ-1-Speicher bietet die erweiterte Integration in Windows Media Player. Es bietet einen herunterladbaren Musikkatalog und ist tief in die Benutzeroberfläche des Players integriert. Die Speicher vom Typ 1 werden von Windows Media Player 11 und höher unterstützt.

Type 2 Stores, die von der Windows Media Player 9-Serie und höher unterstützt werden, haben zwei Unterkategorien: Commerce Stores und Music Stores.

Ein Commerce Store bietet die grundlegendsten Möglichkeiten, indem er bis zu drei Dienstaufgaben Bereiche bereitstellt, in denen die Webseiten des Stores angezeigt werden.

Ein Musik Store bietet eine stärker integrierte Benutzerfunktion als ein Handelsgeschäft. In einem Musik Store können Benutzer auf Schaltflächen und Links in Windows-Media Player (außerhalb der Webseiten, die im Store bereitgestellt werden) klicken, um Aktionen wie das Kaufen einer CD oder DVD, das erhalten von weiteren Informationen zu einem bestimmten Medien Element oder das Anzeigen des Info Center-Ansichts Bereichs auszuführen. In jedem Fall ruft Windows Media Player den aktuellen Musikspeicher auf, um diese Anforderungen zu verarbeiten.

> [!Note]  
> Einige Dokumente beziehen sich auf Commerce Stores als einfache kommerzielle Dienste und beziehen sich auf Music Stores als integrierte Musikdienste.

 

In der folgenden Tabelle sind die verfügbaren Funktionen für die verschiedenen Arten von Online Stores aufgeführt.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Typ 2 Commerce Store</th>
<th>Typ 2 Music Store</th>
<th>Typ 1-Speicher</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aufgabenbereiche zum Erstellen von Diensten
<blockquote>
[!Note]<br />
Windows Media Player 10 verfügt über bis zu drei Dienstaufgaben Bereiche. Windows Media Player 11 verfügt nur über eine.
</blockquote>
<br/></td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Ändern Sie die Darstellung des Stores, indem Sie Attribute wie Schaltflächen Farbe, Task leisten Farbe und Schaltflächen Text ändern.</td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Fügen Sie dem Windows Media Player Online Store-Menü und der Taskleiste Logo Bilder hinzu.</td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Navigieren Sie von HtmlView zum Online Store.</td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Verarbeiten von Windows Media Player-Anforderungen zum Erwerb einer CD oder DVD.</td>
<td>Nein</td>
<td>Ja</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Verarbeiten Sie Windows-Media Player Anforderungen, um umfangreiche Albuminformationen bereitzustellen.</td>
<td>Nein</td>
<td>Ja</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Stellen Sie die Info Center-Ansichts Webseite bereit.</td>
<td>Nein</td>
<td>Ja</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Anpassen des Windows Media Player-Setups zum Angeben eines anfänglichen Online Stores.</td>
<td>Nein</td>
<td>Ja</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Stellen Sie ein Plug-in bereit, das <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice"><strong>iwmpabonneptionservice</strong></a>implementiert.
<blockquote>
[!Note]<br />
In Windows Media Player 10 und höher kann dieses Plug-in auch <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2"><strong>IWMPSubscriptionService2</strong></a>implementieren.
</blockquote>
<br/></td>
<td>Nein</td>
<td>Ja</td>
<td>Nein</td>
</tr>
<tr class="even">
<td>Bereitstellen eines musikkatalogs, der von Windows heruntergeladen wird Media Player</td>
<td>Nein</td>
<td>Nein</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Stellen Sie angepasste Webseiten und Kontextmenüs bereit, die auf der Benutzeroberfläche des Players in der Benutzeroberfläche des Benutzers basieren.</td>
<td>Nein</td>
<td>Nein</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Stellen Sie ein Plug-in bereit, das <a href="/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner"><strong>iwmpcontentpartner</strong></a>implementiert.</td>
<td>Nein</td>
<td>Nein</td>
<td>Ja</td>
</tr>
</tbody>
</table>



 

Der Rest der Dokumentation zu Online Stores ist in die folgenden Abschnitte unterteilt.



| `Section`                                                                                                                              | BESCHREIBUNG                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Willkommens-Kit für Online Stores](online-stores-welcome-kit.md)                                                                           | Enthält Informationen zum Bereitstellen eines digitalen Online Medien Stores in Windows Media Player.             |
| [Typ 1 Online Stores](type-1-online-stores.md)                                                                                     | Enthält Informationen zu-, Führungs-und Bezugs Abschnitten für Onlinespeicher vom Typ 1.                                             |
| [Typ 2 Online Stores](type-2-online-stores.md)                                                                                     | Enthält Informationen zu den Abschnitten, Anleitungen und verweisen für den Typ 2 Online Stores.                                             |
| [Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind](information-common-to-type-1-and-type-2-online-stores.md)                   | Enthält Informationen, die für den Onlinespeicher Type 1 und Type 2 gelten.                                          |
| [Aktualisieren von Lizenzen für Filialen mit dem PlaysForSure-Logo](refreshing-licenses-for-stores-that-have-the-playsforsure-logo.md) | Enthält Informationen dazu, wie Online-Stores, die nicht in Media Player Windows integriert sind, Lizenzen aktualisieren können. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player SDK**](windows-media-player-sdk.md)
</dt> </dl>

 

 





