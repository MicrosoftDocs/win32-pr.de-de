---
description: Die folgende Liste enthält die cmspstream-Member.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Cmspstream-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131720"
---
# <a name="cmspstream-members"></a>Cmspstream-Member



| Memberart                     | Name                | BESCHREIBUNG                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                        | \*Mio. \_ pftm           | Zeiger auf den Free Threaded Marshaller.                                                                                                   |
| DWORD                           | m \_ dwstate          | Der aktuelle Zustand des Streams.                                                                                                           |
| HANDLE                          | m \_ had-Kleid         | Die Adresse, für die dieser Stream verwendet wird.                                                                                            |
| DWORD                           | Mio. \_ dwmediatype      | Der [**Medientyp**](tapimediatype--constants.md) dieses Streams (Audiodaten, Video usw.).                                                    |
| Terminal \_ Richtung             | m \_ Richtung        | Die [**Richtung**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) dieses Streams (eingehend oder ausgehend).                                                         |
| Cmspcallbase                    | \*m \_ pmspcallcenter       | Zeiger auf das-Objekt des Aufrufes.                                                                                                                |
| Igraphbuilder                   | \*m \_ pigraphbuilder | Zeiger auf Diagramm Objekt Schnittstellen.                                                                                                        |
| IMediaControl                   | \*m \_ pimediacontrol | Ein Zeiger auf die Medien Steuerungs Schnittstelle.                                                                                                    |
| Cmsparray <itterminal \*> | m- \_ Terminals        | Die Liste der Terminals im Stream.                                                                                                       |
| Cmspcritsection                 | m- \_ Sperre             | Die Sperre, die das Datenstrom Objekt schützt. Das Stream-Objekt sollte die Sperre nie abrufen und dann eine mspcallcenter-Methode, die möglicherweise sperrt, aufruft. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cmspstream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



