---
title: D1104 – Möglicher Verlust
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Die Factory wurde freigegeben, aber die daraus erstellte Schnittstelle ist noch aktiv. Es ist zwar gültig, Ressourcen nach der Freigabe der Factory freizugeben, aber diese Bedingung kann auf einen Speicherverlust hindeuten.
keywords:
- D1104 Possible Leak Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548675"
---
# <a name="d1104-possible-leak"></a>D1104: Möglicher Verlust

Die \[ *Factory* \] wurde veröffentlicht, aber die von ihr erstellte \[ *Schnittstellenschnittstelle* \] ist noch aktiv. Es ist zwar gültig, Ressourcen nach der Freigabe der Factory freizugeben, aber diese Bedingung kann auf einen Speicherverlust hindeuten.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*Fabrik*
</dt> <dd>

Die Adresse der Factory, die freigegeben wurde.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*
</dt> <dd>

Die Adresse der Schnittstelle, die in der *Factory* erstellt wurde.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Fehlerstufe | Information |



 

## <a name="possible-causes"></a>Mögliche Ursachen

Die Factory wurde freigegeben, aber die daraus erstellte Schnittstelle ist noch aktiv.

 

 




