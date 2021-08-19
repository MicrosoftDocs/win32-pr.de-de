---
title: ACF-Attribute für die Fehler- und Ausnahmebehandlung
description: Verwenden Sie die folgenden Attribute für die Fehlerbehandlung.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF MIDL , Attribute, Fehler- und Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f780145854a463da9a983c7dccbb24b01c2eca16437bf1254f93ec34def5395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384426"
---
# <a name="error-and-exception-handling-acf-attributes"></a>ACF-Attribute für die Fehler- und Ausnahmebehandlung

Verwenden Sie die folgenden Attribute für die Fehlerbehandlung.



| attribute                                                                | Verwendung                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ Comm-Statusfehlerstatus**](comm-status.md)[**\_**](fault-status.md) | Lassen Sie ihre Clientanwendung Ausnahmen ordnungsgemäß behandeln, indem Kommunikations- und Serverfehler als Parameterwerte an den Client zurückgegeben werden. Die Clientanwendung kann dann die RPC-Laufzeitfunktion [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) aufrufen, um eine Fehlermeldung an den Benutzer weiterzuleiten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Importieren von Dateien und Typbibliotheken](importing-files-and-type-libraries.md)
</dt> </dl>

 

 