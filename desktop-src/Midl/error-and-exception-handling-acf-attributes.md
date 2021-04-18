---
title: Fehler-und Ausnahmebehandlung von ACF-Attributen
description: Verwenden Sie die folgenden Attribute für die Fehlerbehandlung.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- ACF-Mittell, Attribute, Fehler-und Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340268"
---
# <a name="error-and-exception-handling-acf-attributes"></a>Fehler-und Ausnahmebehandlung von ACF-Attributen

Verwenden Sie die folgenden Attribute für die Fehlerbehandlung.



| Attribut                                                                | Verbrauch                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_**](comm-status.md)[**\_ Status Fehlerstatus** von "comm"](fault-status.md) | Lassen Sie zu, dass die Client Anwendung Ausnahmen ordnungsgemäß behandelt, indem Sie als Parameterwerte Kommunikations-und Server Fehler an den Client zurückgeben. Die Client Anwendung kann dann die RPC-Lauf Zeitfunktion [**dceerrorinqtext**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) aufzurufen, um eine Fehlermeldung an den Benutzer weiterzuleiten. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Importieren von Dateien und Typbibliotheken](importing-files-and-type-libraries.md)
</dt> </dl>

 

 