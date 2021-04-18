---
description: Nachdem Sie ein Handle für eine INF-Datei haben, können Sie auf verschiedene Weise Informationen daraus abrufen. Funktionen wie setupgetinfinformation, setupqueryinffileinformation und setupqueryinfversioninformation rufen Informationen zur INF-Datei selbst ab.
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: Abrufen von Informationen aus einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347609"
---
# <a name="retrieving-information-from-an-inf-file"></a>Abrufen von Informationen aus einer INF-Datei

Nachdem Sie ein Handle für eine INF-Datei haben, können Sie auf verschiedene Weise Informationen daraus abrufen. Funktionen wie [**setupgetinfinformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**setupqueryinffileinformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)und [**setupqueryinfversioninformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) rufen Informationen zur INF-Datei selbst ab.

Andere Funktionen, wie z. b. [**setupgetsourceinfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) und [**setupgettargetpath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) , rufen Informationen zu den Quelldateien und Zielverzeichnissen ab.

Auf Low-Level-Funktionen wie " [**setupgetlinetext**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) " und " [**setupgetstringfield**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) " können Sie direkt auf Informationen zugreifen, die in einer Zeile oder einem Feld einer INF-Datei gespeichert sind. Diese Funktionen werden intern von den Funktionen auf höherer Ebene verwendet, sind aber auch verfügbar, wenn Sie auf der Zeilen-oder Feldebene auf INF-Informationen zugreifen müssen.

 

 



