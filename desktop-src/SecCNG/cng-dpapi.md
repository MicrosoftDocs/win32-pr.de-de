---
description: Microsoft hat die DPAPI (Data Protection Application Programming Interface) in Windows 2000 eingeführt.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG-DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344871"
---
# <a name="cng-dpapi"></a>CNG-DPAPI

Microsoft hat die DPAPI (Data Protection Application Programming Interface) in Windows 2000 eingeführt. Die API besteht aus zwei Funktionen: " [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) " und " [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata)". DPAPI ist Teil von CryptoAPI und wurde für Entwickler gedacht, die sehr wenig über die Verwendung von Kryptografie wussten. Die beiden Funktionen können verwendet werden, um statische Daten auf einem einzelnen Computer zu verschlüsseln und zu entschlüsseln.

Cloud Computing erfordert jedoch häufig, dass auf einem Computer verschlüsselte Inhalte auf einem anderen Computer entschlüsselt werden. Daher hat Microsoft ab Windows 8 die Idee erweitert, eine relativ unkomplizierte API zu verwenden, um cloudszenarien abzudecken. Diese neue API mit dem Namen "DPAPI-ng" ermöglicht es Ihnen, geheime Schlüssel (Schlüssel, Kenn Wörter, Schlüsselmaterial) und Nachrichten sicher zu teilen, indem Sie Sie für einen Satz von Prinzipalen schützen, die verwendet werden können, um Sie nach entsprechender Authentifizierung und Autorisierung auf unterschiedlichen Computern zu schützen. Die folgenden Prinzipale werden zurzeit unterstützt:

-   Eine Gruppe in einer Active Directory Gesamtstruktur.
-   Webanmelde Informationen.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Schutz Anbieter](protection-providers.md)
-   [Schutz Deskriptoren](protection-descriptors.md)
-   [Geschütztes Daten Format](protected-data-format.md)

DPAPI-ng basiert auf der Cryptography Next Generation (CNG) und umfasst die folgenden Funktionen:

-   [**Ncryptkreateschutzdescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [**Ncryptcloseschutzdescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [**Ncryptprotectsecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [**Ncryptqueryschutzdescriptor Name**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [**Ncryptregisterschutzdescriptor Name**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [**Ncryptstreamclose**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [**Ncryptstreamopentoprotect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [**Ncryptstreamopentounprotect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [**Ncryptstreamupdate**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [**Ncryptunprotectsecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
