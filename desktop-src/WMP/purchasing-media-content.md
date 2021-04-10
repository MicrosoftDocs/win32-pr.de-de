---
title: Erwerben von Medieninhalten
description: Erwerben von Medieninhalten
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player Online Stores, Erwerb von Medieninhalten
- Online Stores, Erwerb von Medieninhalten
- Typ 1 Online Stores, Einkauf von Medieninhalten
- Windows Media Player Online Stores, Käufe von Medieninhalten
- Online Stores, Käufe von Medieninhalten
- Typ 1 Online Stores, Käufe von Medieninhalten
- Medieninhalt, Einkauf
- erwerben von Medieninhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948415"
---
# <a name="purchasing-media-content"></a>Erwerben von Medieninhalten

Wenn in Windows Media Player Musikinhalte in der Bibliotheksstruktur Ansicht angezeigt werden, enthält die Benutzeroberfläche Elemente, auf die der Benutzer klicken kann, um den Inhalt zu kaufen. Beispielsweise kann der Benutzer auf eine Schaltfläche klicken, um einen einzelnen Song zu kaufen oder ein gesamtes Album zu kaufen.

Wenn es sich bei dem aktiven Online Store um einen Speicher vom Typ 1 handelt, hat Windows Media Player Zugriff auf die Preise für Nachverfolgung, Album und Liste im Katalog des Online Stores. Diese Preise im Katalog sind Zeichen folgen, die ein Format aufweisen, das nur vom Online Store verstanden wird. Die Preis Zeichenfolgen werden von Windows Media Player nicht interpretiert. Sie zeigt Sie lediglich in Benutzeroberflächen Elementen wie z. b. Schaltflächen kaufen an.

Wenn Windows Media Player einen Kauf für einen Satz von Medien Elementen einrichtet, übergibt er die IDs und Preise der Medienelemente an das Plug-in für den Inhalts Partner, indem [iwmpcontentpartner:: canbuysilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent)aufgerufen wird. An diesem Punkt kann das Plug-in die vom Spieler bereitgestellten Preise überprüfen. Dies sind die Preise, die der Benutzer für die Zahlung erwartet. Das heißt, die Preise, die dem Benutzer angezeigt werden. Basierend auf den vom Player bereitgestellten Medien-IDs und Preisen berechnet das Plug-in einen Gesamtpreis, der an den Player im *bstrautotalprice* -Parameter zurückgegeben wird. Durch die Preise, die der Player an **canbuysilent** übergibt, wird das Plug-in mit Informationen versehen, aber das Plug-in wird nicht zum Zurückgeben eines bestimmten Gesamtpreises verpflichtet. Das Plug-in kann den Gesamtpreis berechnen, wie er passt.

Zusätzlich zum Berechnen des Gesamtpreises eines Kaufs bestimmt **canbuysilent** , ob der purchace unbeaufsichtigt fortfahren kann. Das heißt, ohne ein Dialogfeld anzuzeigen. Wenn **canbuysilent** " **true**" zurückgibt, ändert Windows Media Player einfach den Text auf der Schaltfläche "kaufen", um den Benutzer zur Bestätigung des Kaufs aufzufordern. Wenn **canbuysilent** **false** zurückgibt, zeigt Windows Media Player ein Dialogfeld an, in dem der Benutzer aufgefordert wird, den Kauf zu bestätigen Das Dialogfeld stellt dem Benutzerinformationen zur Verfügung, die den Kauf wie die Anzahl der Alben, die Anzahl der einzelnen Spuren und den Gesamtpreis (wie vom Plug-in zurückgegeben) zusammenfasst.

Nachdem der Benutzer den Kauf bestätigt hat, ruft der Spieler [iwmpcontentpartner:: Buy](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)auf. Dieser Methodenaufrufe stellt das Plug-in mit der gleichen Inhalts Container Liste wie **canbuysilent** bereit. Beim Aufrufen von " **kaufen**" stellt Windows-Media Player auch ein Cookie (einfach einen **DWORD** -Wert, der für die Sitzung eindeutig ist) bereit, mit dem das Plug-in die Transaktion identifizieren kann. Wenn die Transaktion abgeschlossen ist, muss das Plug-in [iwmpcontentpartnercallback:: buycomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete)aufrufen und dabei den ursprünglichen Cookie-Wert für den *dwbuycookie* -Parameter übergeben, um den Player zu benachrichtigen, dass die Transaktion abgeschlossen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für den Typ 1 Online Stores**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




