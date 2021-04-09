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
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a><span data-ttu-id="d08ba-104">Auswirkungen der Sicherheit auf Vorgänge in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="d08ba-104">How Security Affects Operations in Active Directory Domain Services</span></span>

<span data-ttu-id="d08ba-105">Active Directory Domain Services die Zugriffs Steuerung verwenden, um den Zugriff auf Objekte, Eigenschaften und Vorgänge basierend auf der Identität des Benutzers, der den Zugriffs Versuch ausführt, zu gewähren oder zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="d08ba-105">Active Directory Domain Services use access control to grant or deny access to objects, properties, and operations based on the identity of the user performing the access attempt.</span></span> <span data-ttu-id="d08ba-106">Wenn Ihre Anwendung an das Verzeichnis gebunden wird, wird Sie an bestimmte Benutzer Anmelde Informationen gebunden.</span><span class="sxs-lookup"><span data-stu-id="d08ba-106">When your application binds to the directory, it binds with specific user credentials.</span></span> <span data-ttu-id="d08ba-107">Bei der Authentifizierung bestimmen diese Anmelde Informationen den Sicherheitskontext Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d08ba-107">When authenticated, these credentials determine your application's security context.</span></span> <span data-ttu-id="d08ba-108">Unabhängig davon, ob es sich bei den Anmelde Informationen um die Anmelde Informationen des angemeldeten Benutzers, einen angegebenen Benutzer, ein Dienst Konto, ein Computer Konto oder einen nicht authentifizierten Benutzer handelt (Guest/any), überprüft der Active Directory Server das Recht des Benutzers, auf ein Objekt zuzugreifen, bevor für dieses Objekt ein Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d08ba-108">Regardless of whether the credentials are those of the logged-on user, a specified user, a service account, a computer account, or an unauthenticated user (Guest/Everyone), the Active Directory server verifies the user's right to access an object before any operation is performed on that object.</span></span> <span data-ttu-id="d08ba-109">Der Benutzer kann auf ein bestimmtes Objekt, seine untergeordneten Elemente, seine Eigenschaften oder Vorgänge für dieses Objekt zugreifen, was bedeutet, dass die Anwendung die potenziellen Fehler behandeln muss, die durch den verweigerten Zugriff verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="d08ba-109">The user may, or may not, have access to a particular object, its children, its properties, or operations on that object, which means that your application must handle the potential errors caused by denied access.</span></span>

<span data-ttu-id="d08ba-110">Weitere Informationen zu Sicherheits Kontexten und den Auswirkungen der Zugriffs Steuerung auf verschiedene Vorgänge finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="d08ba-110">For more information about security contexts and the effects of access control on various operations, see:</span></span>

-   [<span data-ttu-id="d08ba-111">Access Control-und Lesevorgänge</span><span class="sxs-lookup"><span data-stu-id="d08ba-111">Access Control and Read Operations</span></span>](access-control-and-read-operations.md)
-   [<span data-ttu-id="d08ba-112">Access Control-und Schreibvorgänge</span><span class="sxs-lookup"><span data-stu-id="d08ba-112">Access Control and Write Operations</span></span>](access-control-and-write-operations.md)
-   [<span data-ttu-id="d08ba-113">Access Control und Objekt Erstellung</span><span class="sxs-lookup"><span data-stu-id="d08ba-113">Access Control and Object Creation</span></span>](access-control-and-object-creation.md)
-   [<span data-ttu-id="d08ba-114">Löschen von Access Control und Objekten</span><span class="sxs-lookup"><span data-stu-id="d08ba-114">Access Control and Object Deletion</span></span>](access-control-and-object-deletion.md)

 

 




