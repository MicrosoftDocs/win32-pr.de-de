---
title: D1109 Draw Failure
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Fehler bei einem Draw-Aufruf durch ein Renderziel
keywords:
- D1109 Draw Failure Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b1d30d0b33cbeb053e37f9e52c3948009a19692dbe1c53eedab9dfd6623726a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814790"
---
# <a name="d1109-draw-failure"></a>D1109: Draw Failure

Ein Draw-Aufruf durch eine fehlerhafte \[ *Renderzielressource.* \] Tags \[ *tag1*, *tag2* \] .

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Ressource*
</dt> <dd>

Die Adresse des Renderziels.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Der erste Tagwert (weitere Informationen finden Sie unter [**SetTags).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Der zweite Tagwert (weitere Informationen finden Sie unter [**SetTags).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Fehlerstufe | Warnung |



 

## <a name="possible-causes"></a>Mögliche Ursachen

Es gibt viele Gründe, warum ein Draw-Aufruf fehlschlagen kann. Weitere Informationen finden Sie in der Direct2D SDK-Dokumentation für die Methode, bei der ein Fehler aufgetreten ist.

 

 