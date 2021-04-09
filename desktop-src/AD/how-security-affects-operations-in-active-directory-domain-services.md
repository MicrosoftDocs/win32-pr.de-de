---
title: Auswirkungen der Sicherheit auf Vorgänge in Active Directory Domain Services
description: Active Directory Domain Services die Zugriffs Steuerung verwenden, um den Zugriff auf Objekte, Eigenschaften und Vorgänge basierend auf der Identität des Benutzers, der den Zugriffs Versuch ausführt, zu gewähren oder zu verweigern.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Sicherheits Effekte in Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855423"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>Auswirkungen der Sicherheit auf Vorgänge in Active Directory Domain Services

Active Directory Domain Services die Zugriffs Steuerung verwenden, um den Zugriff auf Objekte, Eigenschaften und Vorgänge basierend auf der Identität des Benutzers, der den Zugriffs Versuch ausführt, zu gewähren oder zu verweigern. Wenn Ihre Anwendung an das Verzeichnis gebunden wird, wird Sie an bestimmte Benutzer Anmelde Informationen gebunden. Bei der Authentifizierung bestimmen diese Anmelde Informationen den Sicherheitskontext Ihrer Anwendung. Unabhängig davon, ob es sich bei den Anmelde Informationen um die Anmelde Informationen des angemeldeten Benutzers, einen angegebenen Benutzer, ein Dienst Konto, ein Computer Konto oder einen nicht authentifizierten Benutzer handelt (Guest/any), überprüft der Active Directory Server das Recht des Benutzers, auf ein Objekt zuzugreifen, bevor für dieses Objekt ein Vorgang ausgeführt wird. Der Benutzer kann auf ein bestimmtes Objekt, seine untergeordneten Elemente, seine Eigenschaften oder Vorgänge für dieses Objekt zugreifen, was bedeutet, dass die Anwendung die potenziellen Fehler behandeln muss, die durch den verweigerten Zugriff verursacht werden.

Weitere Informationen zu Sicherheits Kontexten und den Auswirkungen der Zugriffs Steuerung auf verschiedene Vorgänge finden Sie unter:

-   [Access Control-und Lesevorgänge](access-control-and-read-operations.md)
-   [Access Control-und Schreibvorgänge](access-control-and-write-operations.md)
-   [Access Control und Objekt Erstellung](access-control-and-object-creation.md)
-   [Löschen von Access Control und Objekten](access-control-and-object-deletion.md)

 

 




