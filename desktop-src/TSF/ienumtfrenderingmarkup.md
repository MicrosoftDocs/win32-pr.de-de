---
title: Ienumtfrenderingmarkup-Schnittstelle
description: Die ienumtfrenderingmarkup-Schnittstelle wird von TSF Manager implementiert und von Anwendungen verwendet. Diese Schnittstelle kann von itfcontextrenderingmarkup GetRenderingMarkup abgerufen werden und listet die renderingmarkup-Informationen auf.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- Ienumtfrenderingmarkup Interface Text Services-Framework
- Ienumtfrenderingmarkup Interface Text Services-Framework, beschrieben
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039401"
---
# <a name="ienumtfrenderingmarkup-interface"></a>Ienumtfrenderingmarkup-Schnittstelle

Die **ienumtfrenderingmarkup** -Schnittstelle wird von TSF Manager implementiert und von Anwendungen verwendet. Diese Schnittstelle kann von [itfcontextrenderingmarkup:: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) abgerufen werden und listet die renderingmarkup-Informationen auf.



| Ienumtfrenderingmarkup-Methoden            | BESCHREIBUNG                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Klonen](ienumtfrenderingmarkup-clone.md) | Die **ienumtfrenderingmarkup:: Clone** -Methode erstellt eine Kopie des Enumeratorobjekts.                                                                  |
| [Nächste](ienumtfrenderingmarkup-next.md)   | Die **ienumtfrenderingmarkup:: Next** -Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.          |
| [Zurücksetzen](ienumtfrenderingmarkup-reset.md) | Die **ienumtfrenderingmarkup:: Reset** -Methode setzt das Enumeratorobjekt zurück, indem die aktuelle Position an den Anfang der enumerationssequenz verschoben wird. |
| [Skip](ienumtfrenderingmarkup-skip.md)   | Die **ienumtfrenderingmarkup:: Skip** -Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.          |



 

## <a name="members"></a>Member

Die **ienumtfrenderingmarkup** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Schnittstelle befindet sich derzeit nicht in den öffentlichen Header Dateien. Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.

 

 

 