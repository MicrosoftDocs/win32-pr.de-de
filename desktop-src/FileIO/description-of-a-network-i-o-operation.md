---
description: Beschreibt den Vorgang eines Netzwerk-e/a-Vorgangs unter Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Beschreibung eines Netzwerk-e/a-Vorgangs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345799"
---
# <a name="description-of-a-network-io-operation"></a>Beschreibung eines Netzwerk-e/a-Vorgangs

In der folgenden Abbildung wird der Vorgang eines Netzwerk-e/a-Vorgangs unter Windows veranschaulicht.

![Netzwerk-e/a-Vorgang unter Windows](images/fig4.png)

Wenn eine Anwendung eine Datei-e/a-Funktion aufruft, um auf eine Datei auf einem Remote Computer zuzugreifen, treten die folgenden Ereignisse auf:

-   Die e/a-Anforderung wird von einem [Netzwerkredirector](network-redirectors.md), auch als Redirector bezeichnet, auf dem lokalen Computer abgefangen. Dies wird in der obigen Abbildung durch den voll tonpfeil zwischen der Anwendung und dem clientredirector dargestellt.
-   Der Redirector erstellt ein Datenpaket, das alle Informationen über die Anforderung enthält, und sendet es an den Server, auf dem sich die Datei befindet. Dies wird in der obigen Abbildung durch den voll tonpfeil zwischen dem clientredirector und dem serverredirector dargestellt.
-   Der Redirector auf dem Server empfängt das Paket vom Client, authentifiziert den Zugriff auf die Datei, die für die e/a-Anforderung erforderlich ist, und führt bei der Authentifizierung die Anforderung im Auftrag des Clients aus. Wenn dies nicht der Fall ist, wird an den Redirector auf dem Client ein Fehlercode zurückgegeben. Dies wird in der obigen Abbildung durch den gekrümmten voll tonpfeil zwischen dem Server Redirector und der Datei dargestellt.
-   Wenn die Anforderung ausgeführt wurde, sendet der Redirector auf dem Server alle Daten, die sich aus der e/a-Anforderung ergeben, sowie eine Erfolgs Benachrichtigung an den Redirector auf dem Client. Dies wird in der obigen Abbildung durch den gepunkteten Pfeil zwischen dem Server und dem clientredirector dargestellt.
-   Der Redirector auf dem Client empfängt das Paket vom Server und übergibt die Daten im Paket zusammen mit einer Erfolgs Benachrichtigung an die Anwendung. Dies wird in der obigen Abbildung durch den gepunkteten Pfeil zwischen dem clientredirector und der Anwendung dargestellt.

Windows kann eine Vielzahl von Netzwerkprotokollen verwenden, um einen Netzwerk-e/a-Vorgang auszuführen, einschließlich der [Übersicht über das Microsoft SMB-Protokoll und CIFS-Protokoll](microsoft-smb-protocol-and-cifs-protocol-overview.md) und NFS.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | BESCHREIBUNG                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Unterschiede in lokalen und Netzwerk-e/a](differences-in-local-and-network-i-o.md)<br/> | Unterschiede zwischen lokalem e/a und Netzwerk-e/a unter Windows.<br/> |
| [Netzwerkredirectors](network-redirectors.md)<br/>                                   | Beschreibt die Funktionalität eines Netzwerkredirector.<br/>      |



 

 

 




