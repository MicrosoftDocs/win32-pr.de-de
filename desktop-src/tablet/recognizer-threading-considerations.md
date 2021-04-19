---
description: Obwohl der&\# 160; Erkennungs Kontext&\# 160; von zwei Threads gleichzeitig von der Tablet PC-Plattform aus nicht aufgerufen werden kann, kann die Funktion adviseinkchange jederzeit in jedem Thread aufgerufen werden.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Überlegungen zum Erkennungs Thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363264"
---
# <a name="recognizer-threading-considerations"></a>Überlegungen zum Erkennungs Thread

Obwohl auf einen [Erkennungs Kontext](hrecocontext-handle.md) nicht gleichzeitig von der Tablet PC-Plattform aus von zwei Threads aus zugegriffen werden kann, kann die Funktion [**adviseinkchange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) jederzeit in jedem beliebigen Thread aufgerufen werden. Da die Tablet PC-Plattform nicht sicherstellt, dass immer nur ein Erkennungs Kontext vorhanden ist, können zwei separate Erkennungs Kontexte in separaten Threads gleichzeitig versuchen, auf Ihre [Erkennung](hrecognizer-handle.md)zuzugreifen. Daher müssen globale Variablen in der Erkennungs-Engine Thread sicher sein.

Word-Listen sind eine optionale Implementierung, die zum Erhöhen der Genauigkeit verwendet wird. Wenn Ihre Erkennung Wortlisten implementiert, muss Sie Thread sicher sein. Weitere Informationen zum Verwenden von Word-Listen finden Sie unter [Verwenden von Anwendungs Wörterbüchern](using-application-dictionaries.md).

Weitere Informationen zu anderen Threading Überlegungen finden Sie unter [Überlegungen zum Tablet PC-Threading](tablet-pc-threading-considerations.md).

 

 



