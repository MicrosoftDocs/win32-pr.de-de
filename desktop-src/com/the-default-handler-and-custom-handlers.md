---
title: Standardhandler und benutzerdefinierte Handler
description: Standardhandler und benutzerdefinierte Handler
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d7c0cbcff81ed8c0aa1e23d4b6713b33943e6ef925a0a22cb06f7102877eda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103748"
---
# <a name="the-default-handler-and-custom-handlers"></a>Standardhandler und benutzerdefinierte Handler

Der Standardhandler, eine von OLE bereitgestellte Implementierung, wird von den meisten Anwendungen als Handler verwendet. Eine Anwendung implementiert einen benutzerdefinierten Handler, wenn die Funktionen des Standardhandlers nicht ausreichen. Ein benutzerdefinierter Handler kann entweder den Standardhandler vollständig ersetzen oder Teile der von ihm zur Verfügung stellenden Funktionalität verwenden, wenn dies angemessen ist. Im letzteren Fall wird der Anwendungshandler als Aggregatobjekt implementiert, das aus einem neuen Steuerelementobjekt und dem Standardhandler besteht. Kombinationsanwendungs-/Standardhandler werden auch als *In-Process-Handler bezeichnet.* Der *Remotinghandler wird* für Objekte verwendet, denen in der Systemregistrierung keine CLSID zugewiesen ist oder die keinen angegebenen Handler haben. Von einem Handler für diese Objekttypen ist nur die Übergeben von Informationen über die Prozessgrenze erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Objekthandler](object-handlers.md)
</dt> </dl>

 

 




