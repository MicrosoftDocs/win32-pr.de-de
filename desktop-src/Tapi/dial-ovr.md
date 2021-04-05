---
description: Mit Dial-Vorgängen kann eine Anwendung zusätzliche Ziffern für eine zuvor erstellte Sitzung senden. Ein Beispiel für die Verwendung einer partiellen Wahl ist das Wählen einer Erweiterung. Partielle Unterschiede werden manchmal auch als Inkrementelles oder verzögertes Einwähl bezeichnet.
ms.assetid: 1dfaefd7-f8dd-451e-af18-249c89bdb517
title: Dial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c603d8e846694b4728d1b5ad4c887be34fbac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750777"
---
# <a name="dial"></a>Dial

Mit Dial-Vorgängen kann eine Anwendung zusätzliche Ziffern für eine zuvor erstellte Sitzung senden. Ein Beispiel für die Verwendung einer partiellen Wahl ist das Wählen einer Erweiterung. Partielle Unterschiede werden manchmal auch als Inkrementelles oder verzögertes Einwähl bezeichnet.

Wenn die angegebene Adresse unvollständig ist, kann die Unterscheidung einiger Ziffern verzögert werden, indem ein Semikolon (;) am Ende der Zahl. Anschließend wird ein Wähl Vorgang verwendet, um zusätzliche Adressdaten für die vorhandene Sitzung zu senden, z. b. die Adresse einer Partei, an die der-Befehl übertragen wird.

Jeder Dienstanbieter sollte eine Wähl Zeichenfolge ablehnen, die das enthält **?** ein, und lassen Sie die Anwendung nach Bedarf bearbeiten. Die Anwendung kann z. b. partielle Wähl Zeichen verwenden, um die Zeichenfolge zu wählen, bis zu, aber ohne den **?** , und zeigen Sie dann ein Dialogfeld an, um den Benutzer zu signalisieren, wann der Rest der Wählzeichenfolge gewählt werden soll.

Ein weiterer Grund für eine Anwendung, die partielle Unterstützung zu verwenden, ist, wenn der Dienstanbieter mindestens eines der Befehlsstatus Erkennungs-Steuerzeichen nicht unterstützt. Diese Zeichen, die in einer DFÜ-Adresse vorkommen können, sind W (warten auf den wählbaren Ton); @ (auf stille Antwort warten); und $ (warten Sie, bis die Eingabeaufforderung für die Aufruf Karte angezeigt wird). Diese und alle anderen Zeichen, die in Adress Zeichenfolgen verwendet werden, werden in den untergeordneten [Adressen](address-ovr.md)ausführlicher erläutert.

Der Anbieter gibt an, welche "von ihm unterstützten wählzeichenfolgenmodifizierer" warten. Eine TAPI 2-Anwendung findet diese Daten im **dwdevcapflags** -Member der [**linedevcaps**](/windows/win32/api/tapi/ns-tapi-linedevcaps) -Struktur, die von [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)zurückgegeben wird. Eine TAPI 3-Anwendung [**Ruft itaddresscapability:: get \_ addresscapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) mit *addresscap* auf, das auf den **AC \_ devcapflags** -Member der [**Adress \_ Funktion**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)festgelegt ist.

Die Anwendung kann für nicht unterstützte Zeichen oder als Teil der Initiierung einer Sitzung die "RAW"-Zeichenfolge übergeben. Wenn die Zeichenfolge einen nicht unterstützten Modifizierer oder ein "?" enthält, gibt der Anbieter einen Fehler zurück, der angibt, welcher änderungsmodifizierer zuerst innerhalb der Zeichenfolge aufgetreten ist:

-   lineerr- \_ dialabrechnung
-   lineerr- \_ dialquiet
-   lineerr- \_ dialdialtone
-   lineerr- \_ dialprompt

Die Anwendung kann dann den Bezeichner in der Zeichenfolge suchen, die Ziffern links neben dem Modifizierer ablegen, ein Semikolon anfügen und eine Sitzung mithilfe der partiellen Adresse initiieren. Der Rest der Zeichenfolge kann mit dem Dial-Vorgang gesendet werden.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Siehe [**linedial**](/windows/win32/api/tapi/nf-tapi-linedial).

**TAPI 3. x:** Siehe [**itbasiccallcontrol::D IAL**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial).

 

 
