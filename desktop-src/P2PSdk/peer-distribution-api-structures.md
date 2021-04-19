---
description: Der Microsoft Peer Distribution-Dienst unterstützt die folgenden Strukturen.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Peer Distribution-API-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348616"
---
# <a name="peer-distribution-api-structures"></a>Peer Distribution-API-Strukturen

Der Microsoft Peer Distribution-Dienst unterstützt die folgenden Strukturen.



| Struktur                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ grundlegende \_ Informationen zum Peer-dist-Client**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | Gibt an, ob viele Clients gleichzeitig denselben Inhalt herunterladen.                                                                                                                                                                                             |
| [**\_Inhalts Kennzeichen für Peer-dist \_**](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | Enthält ein vom Client bereitgestelltes Tag, das ein Eingabe Wert für " [**Peer-distclientopencontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)" ist. Das Tag ist dem Inhalts Segment zugeordnet und wird in Content Management-APIs wie z. b. " [**Peer-distclientflushcontent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent)" verwendet. |
| [**Peer-dist- \_ Veröffentlichungs \_ Optionen**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | Enthält Veröffentlichungs Optionen, einschließlich der API-Versionsinformationen und möglicher Optionsflags.                                                                                                                                                                                           |
| [**Peer \_ Abruf \_ Optionen**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | Enthält die Version der abzurufenden Inhaltsinformationen.                                                                                                                                                                                                                                 |
| [**peerdist- \_ Status \_ Informationen**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | Enthält Informationen zum aktuellen Status und zu den Funktionen des BranchCache-Dienstanbieter auf dem lokalen Computer.                                                                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Peer Distribution-API-Referenz](peer-distribution-api-reference.md)
</dt> </dl>

 

 



