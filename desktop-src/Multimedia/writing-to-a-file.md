---
title: Schreiben in eine Datei
description: Schreiben in eine Datei
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf46125d9da8b9e5e0668f504028db8b011c99c780b545f9ea99accc0a9ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891770"
---
# <a name="writing-to-a-file"></a>Schreiben in eine Datei

Sie können ergänzende Informationen in eine Datei schreiben, die mit Schreibberechtigungen geöffnet wurde, indem Sie die [**FUNKTION AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) verwenden. Diese Funktion kopiert die Informationen aus einem von der Anwendung bereitgestellten Puffer und platziert sie in einem oder mehreren Blöcken in der Datei. Der "INFO"-Block ist ein gängiger SCHREIB-Blocktyp, in dem die Funktion ergänzende Informationen speichert. Eine Beschreibung der PROTOKOLLDATEIen und ihrer Datenblöcke finden Sie unter [Resource Interchange File Format Services](resource-interchange-file-format-services.md).

 

 




