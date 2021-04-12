---
title: Zuordnung von ADSI-Schnittstellen zu den Netzwerk Verwaltungsfunktionen
description: Bei den Active Directory Service Interfaces (ADSI) handelt es sich um einen Satz von COM-Schnittstellen, die für den Zugriff auf die Funktionen der Verzeichnisdienste von unterschiedlichen Netzwerkanbietern
ms.assetid: dfa81c58-3ce4-40ee-8bfc-a19a13781992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ec1a1055d3d016bf8b7b1bd3f357810b7ddd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316431"
---
# <a name="mapping-adsi-interfaces-to-the-network-management-functions"></a>Zuordnung von ADSI-Schnittstellen zu den Netzwerk Verwaltungsfunktionen

Bei den Active Directory Service Interfaces (ADSI) handelt es sich um einen Satz von COM-Schnittstellen, die für den Zugriff auf die Funktionen der Verzeichnisdienste von unterschiedlichen Netzwerkanbietern ADSI stellt einen einzelnen Satz von Verzeichnisdienst Schnittstellen für die Verwaltung von Netzwerkressourcen in einer verteilten Computerumgebung dar.

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Schnittstellen Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie erreichen können, indem Sie bestimmte Netzwerk Verwaltungsfunktionen aufrufen.

In der folgenden Tabelle werden die Netzwerk Verwaltungsfunktionen und Funktionsgruppen sowie die ADSI-Schnittstellen aufgelistet, denen die Funktionen zugeordnet sind.



| Functions                                                                  | Schnittstellen                                                                                             |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Netfileaufumum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum), [ **netfilegetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | [**Iadsresource**](/windows/desktop/api/iads/nn-iads-iadsresource), [ **iadsfileserviceoperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations) |
| [Netzgruppen Herkunft](group-functions.md)\*                                          | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [Netlocalgroup](local-group-functions.md)\*                               | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [Netserver](server-functions.md)\*                                        | [**Iadscomputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                                                  |
| ["Nession"](session-functions.md)\*                                      | [**Iadssession**](/windows/desktop/api/iads/nn-iads-iadssession), [ **iadsfileserviceoperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)   |
| [NetShare](share-functions.md)\*                                          | [**Iadsfileshare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)                                                                |
| [Netzwererer](user-functions.md)\*                                            | [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser), [ **iadscomputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                   |
| ["Nettusermodals"](user-modal-functions.md)\*                                | [**Iadsdomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)                                                                      |



 

Weitere Informationen zu Verzeichnisdiensten und zum Programmieren mit ADSI finden Sie unter [Active Directory-Dienst Schnittstellen](/windows/desktop/ADSI/active-directory-service-interfaces-adsi). Informationen zu den benutzerdefinierten Eigenschaften, die der WinNT-Anbieter für die Benutzerklasse verfügbar macht, sowie zu den Eigenschaften Methoden der [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) -Schnittstelle, die der WinNT-Anbieter nicht unterstützt, finden Sie unter [ADSI WinNT Provider](/windows/desktop/ADSI/adsi-winnt-provider).

 

 