---
title: D1102 zu viele geöffnete Handles
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Eine große Anzahl nicht veröffentlichter Schnittstellen wurde gefunden. Aktuell sind von dieser DLL nicht freigegebene Schnittstellen zugeordnet.
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
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718053"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: zu viele geöffnete Handles

Eine große Anzahl nicht veröffentlichter Schnittstellen wurde gefunden. Derzeit sind \[  \] von dieser DLL zahlreiche nicht freigegebene Schnittstellen zugeordnet.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*einigen*
</dt> <dd>

Die Anzahl der nicht veröffentlichten Schnittstellen, die von dieser DLL zugewiesen wurden.

</dd> </dl> 

|             |         |
|-------------|---------|
| Fehlerstufe | Warnung |



 

## <a name="possible-causes"></a>Mögliche Ursachen

Es wurde eine große Anzahl von Ressourcen erstellt. Obwohl Direct2D über keine Obergrenze für die Anzahl der verfügbaren Ressourcen (mit Ausnahme des Speichers) verfügt, gibt die debugschicht diese Informations Meldung aus, wenn 1001 Live-Objekte, 2001 Live-Objekte oder 3001 Live-Objekte usw. auftreten, da dies auf einen Fehler in der Anwendung hindeuten könnte.

 

 




