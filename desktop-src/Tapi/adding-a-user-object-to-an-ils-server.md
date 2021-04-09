---
description: Das folgende Code Fragment veranschaulicht das Veröffentlichen eines Benutzer Objekts in einem ILS-Server. Nachdem ein Benutzerobjekt veröffentlicht wurde, können Remote Parteien das User-Objekt verwenden, um Aufrufe an den angegebenen Benutzer vorzunehmen.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Hinzufügen eines Benutzer Objekts zu einem ILS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750784"
---
# <a name="adding-a-user-object-to-an-ils-server"></a>Hinzufügen eines Benutzer Objekts zu einem ILS-Server

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Das folgende Code Fragment veranschaulicht das Veröffentlichen eines Benutzer Objekts in einem ILS-Server. Nachdem ein Benutzerobjekt veröffentlicht wurde, können Remote Parteien das User-Objekt verwenden, um Aufrufe an den angegebenen Benutzer vorzunehmen.

Dieses Fragment geht davon aus, dass bereits [eine Verbindung mit einem ILS-Server](connecting-to-an-ils-server.md) hergestellt wurde.


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Itdirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**Itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[**Itdirecteryobjectuser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



