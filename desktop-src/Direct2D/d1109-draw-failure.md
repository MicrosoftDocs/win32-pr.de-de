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
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549965"
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

 

 