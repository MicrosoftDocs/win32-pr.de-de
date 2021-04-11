---
description: Im folgenden Code Fragment wird veranschaulicht, wie eine Multicast Adresse für eine Konferenz angefordert und festgelegt wird.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Abrufen einer Multicast Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128729"
---
# <a name="acquiring-a-multicast-address"></a>Abrufen einer Multicast Adresse

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Im folgenden Code Fragment wird veranschaulicht, wie eine Multicast Adresse für eine Konferenz angefordert und festgelegt wird.

Der Einfachheit halber zeigt dieses Fragment die Zuweisung einer Multicast Adresse zu einem Medien Element an. In der Aktualität werden die Auswahl eines Bereichs, die Multicast Adress Anforderung und die Zuweisung für jedes Medien Element, das an der Konferenz beteiligt ist, ausgeführt.

Dieses Fragment geht davon aus, dass bereits [eine Verbindung mit einem ILS-Server](connecting-to-an-ils-server.md) hergestellt wurde. Die hier gezeigten Vorgänge werden im Abschnitt "Ändern der Einstellungen bei Bedarf" unter [Erstellen einer Konferenzankündigung](creating-a-conference-announcement.md)durchgeführt.


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Multicast-com-Schnittstellen](multicast-com-interfaces.md)
</dt> <dt>

[**Imcastaddressallocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[**Imcastscope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[**Imcastleaseinfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[**Ienummcastscope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[**Itconfererceblob**](itconferenceblob.md)
</dt> <dt>

[**Itsdp**](itsdp.md)
</dt> <dt>

[**Itmediacollection**](itmediacollection.md)
</dt> <dt>

[**Ienumbstr**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[**ITmedia**](itmedia.md)
</dt> <dt>

[**Itconnection**](itconnection.md)
</dt> </dl>

 

 



