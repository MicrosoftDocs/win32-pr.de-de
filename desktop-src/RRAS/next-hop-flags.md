---
title: Flags für den nächsten Hop
description: Flags für den nächsten Hop
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Nächste
- Flags für den nächsten Hop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dbad78f5f10d7a9d7bf42f694f7e2fb3109c03b92dccdb5f31697f5cf8988c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790393"
---
# <a name="next-hop-flags"></a>Flags für den nächsten Hop

## <a name="next-hop-state-flags"></a>Statusflags des nächsten Hops



| Konstante                     | Wert | BESCHREIBUNG                              |
|------------------------------|-------|------------------------------------------|
| RTM \_ NEXTHOP \_ STATE \_ CREATED | 0     | Gibt an, dass der nächste Hop erstellt wurde. |
| RTM \_ NEXTHOP \_ STATE \_ DELETED | 1     | Gibt an, dass der nächste Hop gelöscht wurde. |



 

## <a name="next-hop-flags"></a>Flags für den nächsten Hop



| Konstante                    | Wert  | BESCHREIBUNG                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM \_ NEXTHOP \_ FLAGS \_ REMOTE | 0x0001 | Dieser nächste Hop verweist auf ein Remoteziel, das nicht direkt erreichbar ist. Um den vollständigen Pfad abzurufen, muss der Client eine rekursive Suche ausführen. |
| RTM \_ NEXTHOP \_ FLAGS \_ DOWN   | 0x0002 | Dieses Flag ist für die zukünftige Verwendung reserviert.                                                                                                                 |



 

## <a name="next-hop-added"></a>Nächster Hop hinzugefügt



| Konstante                  | Wert | BESCHREIBUNG                 |
|---------------------------|-------|-----------------------------|
| RTM \_ NEXTHOP \_ CHANGE \_ NEW | 0x01  | Ein neuer nächster Hop wurde erstellt. |



 

 

 




