---
description: Beschreibt den Prozess eines Netzwerk-E/A-Vorgangs unter Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Beschreibung eines Netzwerk-E/A-Vorgangs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d872f8eaf6f9a90ab313e6a7b17e3fe93073cdb13e5b039e401de41287f1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150821"
---
# <a name="description-of-a-network-io-operation"></a>Beschreibung eines Netzwerk-E/A-Vorgangs

Die folgende Abbildung veranschaulicht den Prozess eines Netzwerk-E/A-Vorgangs unter Windows.

![Netzwerk-E/A-Vorgang unter Fenstern](images/fig4.png)

Wenn eine Anwendung eine Datei-E/A-Funktion aufruft, um auf eine Datei auf einem Remotecomputer zuzugreifen, treten die folgenden Ereignisse auf:

-   Die E/A-Anforderung wird von einem [Netzwerkumleitungsor](network-redirectors.md)abgefangen, der auch einfach als Umleitung bezeichnet wird, auf dem lokalen Computer. Dies wird in der obigen Abbildung durch den durchgezogenen Pfeil zwischen der Anwendung und dem Client-Redirector dargestellt.
-   Der Redirector erstellt ein Datenpaket, das alle Informationen über die Anforderung enthält, und sendet es an den Server, auf dem sich die Datei befindet. Dies wird in der obigen Abbildung durch den durchgezogenen Pfeil zwischen dem Clientumleitungs- und dem Server-Redirector dargestellt.
-   Der Redirector auf dem Server empfängt das Paket vom Client, authentifiziert den Zugriff auf die datei, die für die E/A-Anforderung erforderlich ist, und führt die Anforderung im Auftrag des Clients aus, wenn sie authentifiziert ist. Falls nicht, wird ein Fehlercode an den Redirector auf dem Client zurückgegeben. Dies wird in der vorherigen Abbildung durch den gekrümmten Durchlaufpfeil zwischen dem Server-Redirector und der Datei dargestellt.
-   Wenn die Anforderung ausgeführt wurde, sendet der Redirector auf dem Server alle Daten, die sich aus der E/A-Anforderung ergeben, zusammen mit einer Erfolgsbenachrichtigung an den Redirector auf dem Client. Dies wird in der obigen Abbildung durch den gepunkteten Pfeil zwischen dem Server und dem Client-Redirector dargestellt.
-   Der Redirector auf dem Client empfängt das Paket vom Server und übergibt die Daten im Paket zusammen mit einer Erfolgsbenachrichtigung an die Anwendung. Dies wird in der obigen Abbildung durch den gepunkteten Pfeil zwischen dem Client-Redirector und der Anwendung dargestellt.

Windows können eine Vielzahl von Netzwerkprotokollen verwenden, um einen Netzwerk-E/A-Vorgang auszuführen, einschließlich [Microsoft SMB-Protokoll und CIFS-Protokollübersicht](microsoft-smb-protocol-and-cifs-protocol-overview.md) und NFS.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | Beschreibung                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Unterschiede bei der lokalen E/A und der Netzwerk-E/A](differences-in-local-and-network-i-o.md)<br/> | Unterschiede zwischen lokalen E/A- und Netzwerk-E/A auf Windows.<br/> |
| [Netzwerkumleitung](network-redirectors.md)<br/>                                   | Beschreibt die Funktionalität eines Netzwerk-Redirectors.<br/>      |



 

 

 




