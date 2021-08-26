---
description: 'Das Anforderungsobjekt wird mit COM CoCreateInstance erstellt und macht eine Schnittstelle verfügbar: ITRequest.'
ms.assetid: 1e4c71ce-6846-4e64-9346-455ed82aa458
title: Anforderungsobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcf6da101c3642ffe31b05efb18279a79bcfc28ed24af7a959f3275d9cbc4f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905890"
---
# <a name="request-object"></a>Anforderungsobjekt

Das Anforderungsobjekt wird mit COM **CoCreateInstance** erstellt und macht eine Schnittstelle verfügbar: [**ITRequest.**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest) Diese Schnittstelle macht die [**MakeCall-Methode**](/windows/desktop/api/tapi3if/nf-tapi3if-itrequest-makecall) verfügbar, die einer TAPI 3-Anwendung die Verwendung der unterstützten Telefonie ermöglicht. Die telefongestützte Telefonie bietet telefoniefähige Anwendungen mit einem einfachen Mechanismus zum Tätigen von Telefonanrufen, ohne dass der Entwickler die Telefonie vollständig literatieren muss.

Beispielsweise kann eine Tabellenkalkulationsanwendung mithilfe der unterstützten Telefonie eine Schaltfläche "Anruf tätigen" hinzufügen, ohne die komplexeren Steuerelemente zu implementieren, die in einer vollständigen TAPI-Anwendung verfügbar sind.

Weitere Informationen finden Sie in der [Übersicht über die unterstützte Telefonie.](assisted-telephony-overview.md)

 

 



