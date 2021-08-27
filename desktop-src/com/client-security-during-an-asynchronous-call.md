---
title: Clientsicherheit während eines asynchronen Aufrufs
description: Clientsicherheit während eines asynchronen Aufrufs
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4c25e17712d0164938f3de9895d1e6b02582f2d86cba9957297e23aa4e7f1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071040"
---
# <a name="client-security-during-an-asynchronous-call"></a>Clientsicherheit während eines asynchronen Aufrufs

Der von MIDL erstellte Proxy-Manager für Objekte, die das Standardmäßige Marshalling verwenden, implementiert die [**IClientSecurity-Schnittstelle.**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) Clients können die Sicherheit gemarshallter Aufrufe verwalten, indem **sie IClientSecurity** für das Aufrufobjekt abfragen und Sicherheitseinstellungen abrufen oder ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines asynchronen Aufrufs](making-an-asynchronous-call.md)
</dt> </dl>

 

 




