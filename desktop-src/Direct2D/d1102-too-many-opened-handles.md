---
title: D1102 zu viele geöffnete Handles
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Es wurde eine große Anzahl von nicht freigegebenen Schnittstellen gefunden. Derzeit sind von dieser DLL nicht freigegebene Schnittstellen zugeordnet.
keywords:
- D1102 zu viele geöffnete Handles Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548685"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: Zu viele geöffnete Handles

Es wurde eine große Anzahl von nicht freigegebenen Schnittstellen gefunden. Derzeit sind \[ *von* dieser DLL nicht \] freigegebene Schnittstellen zugeordnet.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*Anzahl*
</dt> <dd>

Die Anzahl von nicht freigegebenen Schnittstellen, die von dieser DLL zugeordnet werden.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Fehlerstufe | Warnung |



 

## <a name="possible-causes"></a>Mögliche Ursachen

Eine große Anzahl von Ressourcen wurde erstellt. Obwohl Direct2D keine Obergrenze für die Anzahl der verfügbaren Ressourcen (außer Arbeitsspeicher) hat, gibt die Debugebene diese Informationsmeldung aus, wenn 1001 Liveobjekte, 2001 Liveobjekte oder 3001 Liveobjekte usw. auftreten, da dies auf einen Verlust in der Anwendung hinweisen kann.

 

 




