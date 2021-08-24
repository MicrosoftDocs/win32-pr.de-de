---
description: Microsoft hat die Anwendungsprogrammierschnittstelle für den Datenschutz (Data Protection Application Programming Interface, DPAPI) in Windows 2000 eingeführt.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0273522580c806caa5fe7848ff32a2017cfb37c4499dee21f5a3787ecae57b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908629"
---
# <a name="cng-dpapi"></a>CNG DPAPI

Microsoft hat die Anwendungsprogrammierschnittstelle für den Datenschutz (Data Protection Application Programming Interface, DPAPI) in Windows 2000 eingeführt. Die API besteht aus zwei Funktionen: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) DPAPI ist Teil von CryptoAPI und wurde für Entwickler konzipiert, die sehr wenig über die Verwendung der Kryptografie wussten. Die beiden Funktionen können verwendet werden, um statische Daten auf einem einzelnen Computer zu verschlüsseln und zu entschlüsseln.

Cloud Computing erfordert jedoch häufig, dass inhalte, die auf einem Computer verschlüsselt sind, auf einem anderen entschlüsselt werden. Daher erweiterte Microsoft ab Windows 8 die Idee, eine relativ unkomplizierte API zu verwenden, um Cloudszenarien zu umfassen. Mit dieser neuen API namens DPAPI-NG können Sie Geheimnisse (Schlüssel, Kennwörter, Schlüsselmaterial) und Nachrichten sicher freigeben, indem Sie sie für eine Reihe von Prinzipalen schützen, mit denen sie nach ordnungsgemäßer Authentifizierung und Autorisierung auf verschiedenen Computern nicht mehr geschützt werden können. Die folgenden Prinzipale werden derzeit unterstützt:

-   Eine Gruppe in einer Active Directory-Gesamtstruktur.
-   Webanmeldeinformationen.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Schutzanbieter](protection-providers.md)
-   [Schutzdeskriptoren](protection-descriptors.md)
-   [Geschütztes Datenformat](protected-data-format.md)

DPAPI-NG basiert auf Cryptography Next Generation (CNG) und umfasst die folgenden Funktionen:

-   [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [**NCryptCloseProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [**NCryptProtectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [**NCryptQueryProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [**NCryptStreamClose**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [**NCryptStreamOpenToProtect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [**NCryptStreamOpenToUnprotect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [**NCryptStreamUpdate**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [**NCryptUnprotectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
