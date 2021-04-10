---
title: Flags für den nächsten Hop
description: Flags für den nächsten Hop
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Nächste
- Flags für den nächsten Hop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037448"
---
# <a name="next-hop-flags"></a>Flags für den nächsten Hop

## <a name="next-hop-state-flags"></a>Statusflags für den nächsten Hop



| Konstante                     | Wert | BESCHREIBUNG                              |
|------------------------------|-------|------------------------------------------|
| RTM- \_ nexthop- \_ Status \_ erstellt | 0     | Gibt an, dass der nächste Hop erstellt wurde. |
| RTM- \_ nexthop- \_ Status \_ gelöscht | 1     | Gibt an, dass der nächste Hop gelöscht wurde. |



 

## <a name="next-hop-flags"></a>Flags für den nächsten Hop



| Konstante                    | Wert  | BESCHREIBUNG                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM- \_ nexthop- \_ Flags \_ Remote | 0x0001 | Der nächste Hop verweist auf ein Remote Ziel, das nicht direkt erreichbar ist. Zum Abrufen des vollständigen Pfads muss der Client eine rekursive Suche durchführen. |
| RTM- \_ nexthop- \_ Flags \_   | 0x0002 | Dieses Flag ist für die zukünftige Verwendung reserviert.                                                                                                                 |



 

## <a name="next-hop-added"></a>Nächster Hop hinzugefügt



| Konstante                  | Wert | BESCHREIBUNG                 |
|---------------------------|-------|-----------------------------|
| RTM- \_ nexthop- \_ Änderung \_ neu | 0x01  | Ein neuer nächster Hop wurde erstellt. |



 

 

 




