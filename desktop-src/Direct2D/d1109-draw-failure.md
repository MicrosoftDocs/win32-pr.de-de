---
title: D1109 Draw-Fehler
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Fehler bei einem zeichnen-Befehl durch ein Renderziel.
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
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730080"
---
# <a name="d1109-draw-failure"></a>D1109: Zeichnen-Fehler

Ein zeichnen-Befehl durch die Ressource eines Renderziels ist fehlgeschlagen \[  \] . Tags \[ *Tag1*, *Tag2* \] .

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Ressource*
</dt> <dd>

Die Adresse des Renderziels.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*Tag1*
</dt> <dd>

Der erste Tagwert (Weitere Informationen finden Sie unter [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*Tag2*
</dt> <dd>

Der zweite Tagwert (Weitere Informationen finden Sie unter [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).

</dd> </dl> 

|             |         |
|-------------|---------|
| Fehlerstufe | Warnung |



 

## <a name="possible-causes"></a>Mögliche Ursachen

Es gibt viele Gründe, warum ein zeichnen-Befehl fehlschlagen kann. Weitere Informationen finden Sie in der Direct2D SDK-Dokumentation für die fehlgeschlagene Methode.

 

 