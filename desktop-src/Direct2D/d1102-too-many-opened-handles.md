---
title: D1102 zu viele geöffnete Handles
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Eine große Anzahl von nicht freigegebenen Schnittstellen wurde gefunden. Derzeit sind von dieser DLL nicht freigegebene Schnittstellen zugeordnet.
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
ms.openlocfilehash: baaa4c46850919aed50897583bfa68c9003bcf496ad884c68cfb57d3e8a90147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666351"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: Zu viele geöffnete Handles

Eine große Anzahl von nicht freigegebenen Schnittstellen wurde gefunden. Derzeit sind \[ *von* dieser DLL nicht \] freigegebene Schnittstellen zugeordnet.

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

Eine große Anzahl von Ressourcen wurde erstellt. Obwohl Direct2D keine Obergrenze für die Anzahl der verfügbaren Ressourcen (außer Arbeitsspeicher) hat, gibt die Debugschicht diese Informationsmeldung aus, wenn 1001 Liveobjekte, 2001 Liveobjekte oder 3001 Liveobjekte usw. auftreten, da dies auf einen Verlust in der Anwendung hindeuten kann.

 

 




