---
title: Auswirkungen der Sicherheit auf Vorgänge in Active Directory Domain Services
description: Active Directory Domain Services Zugriffssteuerung verwenden, um den Zugriff auf Objekte, Eigenschaften und Vorgänge basierend auf der Identität des Benutzers zu gewähren oder zu verweigern, der den Zugriffsversuch versucht.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Sicherheitseffekte in Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8f5599afbc8552f9708fcfa953a069f429a152c4f0fff37546ffb7d9f6b809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188205"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>Auswirkungen der Sicherheit auf Vorgänge in Active Directory Domain Services

Active Directory Domain Services Zugriffssteuerung verwenden, um den Zugriff auf Objekte, Eigenschaften und Vorgänge basierend auf der Identität des Benutzers zu gewähren oder zu verweigern, der den Zugriffsversuch versucht. Wenn Ihre Anwendung an das Verzeichnis gebunden wird, wird sie mit bestimmten Benutzeranmeldeinformationen gebunden. Bei der Authentifizierung bestimmen diese Anmeldeinformationen den Sicherheitskontext Ihrer Anwendung. Unabhängig davon, ob es sich bei den Anmeldeinformationen um die Anmeldeinformationen des angemeldeten Benutzers, eines angegebenen Benutzers, eines Dienstkontos, eines Computerkontos oder eines nicht authentifizierten Benutzers (Gast/Alle) handelt, überprüft der Active Directory-Server das Recht des Benutzers, auf ein Objekt zu zugreifen, bevor ein Vorgang für dieses Objekt ausgeführt wird. Der Benutzer hat möglicherweise Zugriff auf ein bestimmtes Objekt, seine unteren Objekte, seine Eigenschaften oder Vorgänge für dieses Objekt, was bedeutet, dass Ihre Anwendung die potenziellen Fehler behandeln muss, die durch verweigerten Zugriff verursacht werden.

Weitere Informationen zu Sicherheitskontexten und den Auswirkungen der Zugriffssteuerung auf verschiedene Vorgänge finden Sie unter:

-   [Access Control und Lesevorgänge](access-control-and-read-operations.md)
-   [Access Control und Schreibvorgänge](access-control-and-write-operations.md)
-   [Access Control und Objekterstellung](access-control-and-object-creation.md)
-   [Access Control und Objektlöschung](access-control-and-object-deletion.md)

 

 




