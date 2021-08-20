---
description: Die folgende Liste enthält die CMSPStream-Member.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: CMSPStream-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2607131e231ec23fb17bd2585de81c33a15b1ce80fb51ade206c9721b9f734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117947034"
---
# <a name="cmspstream-members"></a>CMSPStream-Member



| Memberart                     | Name                | Beschreibung                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                        | \*m \_ pFTM           | Zeiger auf den Freithread-Marshaller.                                                                                                   |
| DWORD                           | m \_ dwState          | Der aktuelle Zustand des Streams.                                                                                                           |
| HANDLE                          | m \_ hAddress         | Die Adresse, für die dieser Stream verwendet wird.                                                                                            |
| DWORD                           | m \_ dwMediaType      | Der [**Medientyp**](tapimediatype--constants.md) dieses Streams (Audio, Video usw.).                                                    |
| \_TERMINALRICHTUNG             | \_m-Richtung        | Die [**Richtung**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) dieses Streams (eingehend oder ausgehend).                                                         |
| CMSPCallBase                    | \*m \_ pMSPCall       | Zeiger auf das Aufrufobjekt.                                                                                                                |
| IGraphBuilder                   | \*m \_ pIGraphBuilder | Zeiger auf Graphobjektschnittstellen.                                                                                                        |
| IMediaControl                   | \*m \_ pIMediaControl | Zeiger auf die Mediensteuerungsschnittstelle.                                                                                                    |
| CMSPArray <ITTerminal \*> | m \_ Terminals        | Die Liste der Terminals im Stream.                                                                                                       |
| CMSPCritSection                 | \_m-Sperre             | Die Sperre, die das Streamobjekt schützt. Das Streamobjekt sollte nie die Sperre erhalten und dann eine MSPCall-Methode aufrufen, die möglicherweise gesperrt wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



