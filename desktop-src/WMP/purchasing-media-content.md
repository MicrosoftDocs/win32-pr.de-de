---
title: Erwerb von Medieninhalten
description: Erwerb von Medieninhalten
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player Onlineshops,Erwerb von Medieninhalten
- Onlineshops,Kaufen von Medieninhalten
- Typ 1 Onlineshops,Erwerb von Medieninhalten
- Windows Media Player,Käufe von Medieninhalten
- Onlineshops,Käufe von Medieninhalten
- 'Typ 1: Onlineshops,Käufe von Medieninhalten'
- Medieninhalt,Kaufen
- Erwerb von Medieninhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc830d4b1351b7649343f1f76f347c89da9a8ed9ceffedc3663c3156be6b7ead
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995640"
---
# <a name="purchasing-media-content"></a>Erwerb von Medieninhalten

Wenn Windows Media Player In der Bibliotheksstrukturansicht Musikinhalte anzeigt, enthält die Benutzeroberfläche Elemente, auf die der Benutzer klicken kann, um den Inhalt zu erwerben. Beispielsweise kann der Benutzer auf eine Schaltfläche klicken, um einen einzelnen Titel zu kaufen oder ein ganzes Album zu kaufen.

Wenn es sich bei dem aktiven Onlineshop um einen Store vom Typ 1 handelt, hat Windows Media Player Zugriff auf Titel-, Album- und Listenpreise im Katalog des Onlineshops. Bei diesen Preisen im Katalog handelt es sich um Zeichenfolgen, deren Format nur vom Onlineshop verstanden wird. Windows Media Player keine Preiszeichenfolgen interpretiert. Sie werden lediglich in Benutzeroberflächenelementen wie Schaltflächen kaufen angezeigt.

Wenn Windows Media Player einen Kauf für eine Reihe von Medienelementen einrichten, übergibt er die IDs und Preise der Medienelemente an das Inhaltspartner-Plug-In, indem [es IWMPContentPartner::CanBuySilent aufruft.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent) An diesem Punkt kann das Plug-In die vom Player bereitgestellten Preise überprüfen. Dies sind die Preise, die der Benutzer zu zahlen erwartet. das heißt, die Preise, die der Player dem Benutzer angezeigt hat. Basierend auf den vom Player bereitgestellten Medien-IDs und Preisen berechnet das Plug-In einen Gesamtpreis, den es im *Parameter bstrTotalPrice* an den Player zurückgibt. Die Preise, die der Player an **CanBuySilent** übergibt, stellen dem Plug-In Informationen zur Verfügung, aber sie machen das Plug-In nicht dazu verpflichtet, einen bestimmten Gesamtpreis zurückgibt. Das Plug-In kann den Gesamtpreis nach Be dafür berechnen.

Zusätzlich zur Berechnung des Gesamtpreises eines Kaufs bestimmt **CanBuySilent,** ob die Käufe im Hintergrund fortgesetzt werden können. das heißt, ohne ein Dialogfeld anzuzeigen. Wenn **CanBuySilent** **True** zurückgibt, Windows Media Player den Text auf der Schaltfläche Kaufen einfach so ändern, dass der Benutzer aufgefordert wird, den Kauf zu bestätigen. Wenn **CanBuySilent** **False** zurückgibt, Windows Media Player ein Dialogfeld angezeigt, in dem der Benutzer aufgefordert wird, den Kauf zu bestätigen. Das Dialogfeld stellt dem Benutzer Informationen zur Verfügung, die den Kauf wie anzahl der Albums, die Anzahl einzelner Titel und den Gesamtpreis (wie vom Plug-In zurückgegeben) zusammenfassen.

Nachdem der Benutzer den Kauf bestätigt hat, ruft der Player [IWMPContentPartner::Buy auf.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy) Dieser Methodenaufruf stellt dem Plug-In die gleiche Inhaltscontainerliste wie **CanBuySilent zur.** Beim Aufrufen **von Kaufen** stellt Windows Media Player auch ein Cookie (einfach einen **DWORD-Wert,** eindeutig für die Sitzung) zur Identifizierung der Transaktion zur Anwendung. Wenn die Transaktion abgeschlossen ist, muss das Plug-In [IWMPContentPartnerCallback::BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete)aufrufen und dabei den ursprünglichen Cookiewert für den *dwBuyCookie-Parameter* übergeben, um den Player zu benachrichtigen, dass die Transaktion abgeschlossen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch für Onlineshops vom Typ 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




