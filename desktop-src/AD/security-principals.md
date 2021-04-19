---
title: Sicherheitsprinzipale
description: In Windows 2000 ist ein Sicherheits Prinzipal ein Benutzer, eine Gruppe oder ein Computer \ 8212; eine Entität, die vom Sicherheitssystem erkannt wird.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- Sicherheits Prinzipale AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341831"
---
# <a name="security-principals"></a><span data-ttu-id="1cc58-104">Sicherheitsprinzipale</span><span class="sxs-lookup"><span data-stu-id="1cc58-104">Security Principals</span></span>

<span data-ttu-id="1cc58-105">In Windows 2000 ist ein Sicherheits Prinzipal ein Benutzer, eine Gruppe oder ein Computer – eine Entität, die vom Sicherheitssystem erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc58-105">In Windows 2000, a security principal is a user, group, or computer — an entity that the security system recognizes.</span></span> <span data-ttu-id="1cc58-106">Dies schließt sowohl menschliche Benutzer als auch autonome Prozesse ein.</span><span class="sxs-lookup"><span data-stu-id="1cc58-106">This includes human users as well as autonomous processes.</span></span> <span data-ttu-id="1cc58-107">Streng genommen kann das Sicherheitssystem den Unterschied zwischen den angemeldeten Benutzern und Prozessen, die auf dem Computer ausgeführt werden, nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="1cc58-107">Strictly speaking, the security system cannot tell the difference between users who are logged in and processes running on the computer.</span></span> <span data-ttu-id="1cc58-108">Sie sehen beide als Sicherheits Prinzipale mit Sicherheits Prinzipal Namen.</span><span class="sxs-lookup"><span data-stu-id="1cc58-108">It sees both as security principals with security principal names.</span></span>

<span data-ttu-id="1cc58-109">Benutzer, Gruppen und Computer werden als Objekte in Active Directory Domain Services erstellt und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1cc58-109">Users, groups, and computers are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="1cc58-110">Außerdem gibt es bekannte Sicherheits Prinzipale, die spezielle Identitäten darstellen, die vom Windows 2000-Sicherheitssystem definiert werden, wie z. b. "alle", "Lokales System", "Prinzipal selbst", "authentifizierter Benutzer", "Ersteller-Besitzer</span><span class="sxs-lookup"><span data-stu-id="1cc58-110">There are also well-known security principals that represent special identities defined by the Windows 2000 security system, such as Everyone, Local System, Principal Self, Authenticated User, Creator Owner, and so on.</span></span> <span data-ttu-id="1cc58-111">Objekte, die die bekannten Sicherheits Prinzipale darstellen, wie z. b. die anonyme Anmeldung, werden im Container WellKnown Security Principals unterhalb des Konfigurations Containers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1cc58-111">Objects representing the well-known security principals, such as Anonymous Logon, are stored in the WellKnown Security Principals container beneath the Configuration container.</span></span>

 

 




