---
description: Während Windows Sockets-Dienstanbietern das Implementieren von Sockets als IFS-Objekte (installierbare File System) empfehlen, werden von der Winsock-Architektur auch Dienstanbieter unterstützt, deren Sockethandles keine IFS-Objekte sind.
ms.assetid: ed5e10f4-fa17-4a07-9cac-43767915b8e9
title: Deskriptorzuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095301798eb850fc4eb63e1939712379b5ead85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357334"
---
# <a name="descriptor-allocation"></a>Deskriptorzuordnung

Während Windows Sockets-Dienstanbietern das Implementieren von Sockets als IFS-Objekte (installierbare File System) empfehlen, werden von der Winsock-Architektur auch Dienstanbieter unterstützt, deren Sockethandles keine IFS-Objekte sind. Anbieter mit IFS-Handles geben dies über das XP1 \_ IFS \_ Handles-Attribut Bit in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur an. (Hinweis: XP1 \_ \_Das IFS Handles-Attribut Bit war nicht in Release 2.0.8 der API-Spezifikation enthalten, wurde aber bereits über den Errata-Mechanismus hinzugefügt.) Winsock SPI-Clients können Anbieter nutzen, deren socketdeskriptoren IFS-Handles sind, indem Sie diese Deskriptoren mit standardmäßigen Windows-e/a-Funktionen wie "read [File](/windows/win32/api/fileapi/nf-fileapi-readfile) " und " [Write File](/windows/win32/api/fileapi/nf-fileapi-writefile)" verwenden.

Wenn ein IFS-Anbieter einen neuen socketdeskriptor erstellt, ist es obligatorisch, dass der Anbieter [**wpumodifyifshandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) aufruft, bevor der neue Handle für einen Windows Sockets SPI-Client bereitgestellt wird. Diese Funktion nimmt einen Anbieter Bezeichner und einen vorgeschlagenen IFS-Handle vom Anbieter als Eingabe an und gibt ein (möglicherweise) geändertes Handle zurück. Der IFS-Anbieter muss nur das geänderte Handle für seinen Client bereitstellen, und alle Anforderungen vom Client verweisen nur auf dieses geänderte handle. Es ist garantiert, dass das geänderte Handle nicht vom vorgeschlagenen handle unterschieden wird, soweit es sich um das Betriebssystem handelt. Daher wählt der Dienstanbieter in den meisten Fällen einfach nur das geänderte Handle in der gesamten internen Verarbeitung aus. Der Zweck dieser Änderungs Funktion besteht darin, dass der Ws2- \_32.dll den Prozess der Identifizierung des mit einem bestimmten Socket verknüpften Dienstanbieters erheblich optimieren kann.

Anbieter, die keine IFS-Handles zurückgeben, müssen \_ über den [**wpuanatesockethandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) -Befehl ein gültiges Handle vom Ws2-32.dll erhalten. Der nonifs-Anbieter muss dem Client nur ein von Windows Sockets 2.DLL bereitgestelltes handle anbieten, und alle Anforderungen vom Client verweisen nur auf diese Handles. Um die Implementierung von Dienstanbietern zu erleichtern, ist einer der Eingabeparameter, die von einem Anbieter in **wpukreatesockethandle** bereitgestellt werden, ein DWORD-Kontextwert. Der Ws2 \_ -32.dll ordnet diesen Kontextwert dem zugeordneten Sockethandle zu und ermöglicht einem Dienstanbieter das Abrufen des Kontext Werts zu einem beliebigen Zeitpunkt durch den Aufruf von [**wpuquerysockethandlecontext**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuquerysockethandlecontext) . Eine typische Verwendung dieses Kontext Werts wäre das Speichern eines Zeigers auf eine vom Dienstanbieter beibegebener Datenstruktur, die zum Speichern von socketstatusinformationen verwendet wird.

 

 
