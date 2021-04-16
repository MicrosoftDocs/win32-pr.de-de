---
title: Endpunktadresse
description: Eine Endpunkt Adresse stellt die Adresse eines Dienstanbieter im Netzwerk dar.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Endpunkt Adresse Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104553922"
---
# <a name="endpoint-address"></a>Endpunktadresse

Eine Endpunkt Adresse stellt die Adresse eines Dienstanbieter im Netzwerk dar. Wenn Sie einen [Kanal](channel.md)öffnen, indem Sie die [**wsopenchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) -Funktion aufrufen, müssen Sie die Endpunkt Adresse des Dienstanbieter bereitstellen, mit dem Sie kommunizieren möchten, sowie den Kanal angeben, den Sie öffnen möchten.


Eine Endpunkt Adresse besteht aus folgendem:

-   eine [URL](url.md)
-   ein Satz von Headern (optional)
-   ein Satz von Erweiterungen (optional)
-   eine optionale [Identität](endpoint-identity.md) , die die Sicherheitsidentität des Diensts darstellt.

Wenn eine Nachricht adressiert wird, wird die URL zum "to"-Header der Nachricht. Alle Header, die Teil der Endpunkt Adresse sind, werden ebenfalls der Nachricht hinzugefügt.

![Diagramm, das anzeigt, dass Endpunkt Adress Header zu einer Nachricht hinzugefügt werden.](images/endpointaddress.png)

Kanäle adressiert automatisch alle gesendeten Nachrichten mithilfe der [**WS- \_ Endpunkt \_ Adress**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) Struktur, die an [**wsopkanchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)übermittelt wurde. Sie können auch die [**wsaddressmessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) -Funktion verwenden, um dieses Standardverhalten zu überschreiben.

Wenn die [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) als Parameter übergeben wird, erstellen die [**wsopenchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) -und [**wsopenserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) -Funktionen eine Kopie des **WS- \_ Endpunkt \_ Adress** Parameters im Arbeitsspeicher, und ihre Größe ist auf 65536 Bytes begrenzt. [**Wsaddressmessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) weist diese Einschränkung nicht auf, da es nicht erforderlich ist, eine Kopie des **WS- \_ Endpunkt \_ Adress** Parameters zu erstellen.

Die Erweiterungen, die im Feld **Erweiterungen** der [**WS- \_ Endpunkt \_ Adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) angegeben werden, werden nicht für die Adressierung der Nachricht verwendet. stattdessen handelt es sich um einen Erweiterbarkeits Mechanismus, der verwendet werden kann, um zusätzliche Informationen (z. b. Metadaten) über den Dienst bereitzustellen. Allgemeine Erweiterungen können mit der [**wsleseendpointadressssextension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) -Funktion gelesen werden.

Das optionale Identitäts Feld der Endpunkt Adresse kann z. b. den DNS-Namen des Computers enthalten, auf dem der Dienst ausgeführt wird, oder den UPN des Windows-Kontos, unter dem der Dienst ausgeführt wird. Das Identitäts Feld wird nicht zur Adressierung der Nachricht verwendet, kann jedoch zum Abrufen eines Sicherheits Tokens für den Dienst (z. b. zum Abrufen eines Kerberos-Tickets für den UPN des Ziels) und zum Überprüfen der Identität der Dienst Antworten verwendet werden (z

Endpunkt Adressen können mithilfe der [Serialisierung](serialization.md) gelesen und geschrieben werden, wobei der WS-Endpunkt- **\_ \_ \_ Adresstyp** Enumerationswert vom [**WS- \_ Typ**](/windows/desktop/api/WebServices/ne-webservices-ws_type)ist. Hinweis Wenn Sie eine Endpunkt Adresse serialisieren möchten, müssen Sie die Version der Spezifikation kennen, die für die Adressierungs Header verwendet wird, wie in der Enumeration der [**WS- \_ Adressierungs \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) angegeben.

 

 




