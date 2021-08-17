---
description: Führen Sie die folgenden Schritte aus, um Ihre Anwendungsleistungsindikatoren aus dem System zu entfernen.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Löschen von Leistungsindikatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c34dfc64be4ded0ce07b466393851b235ca4b2f49c89e05f067041f236565fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144013"
---
# <a name="deleting-performance-counters"></a>Löschen von Leistungsindikatoren

Führen Sie die folgenden Schritte aus, um die Leistungsindikatoren Ihrer Anwendung aus dem System zu entfernen.

1.  Verwenden Sie das auf dem Computer enthaltene Tool **unlodctr,** um die indikatorbezogenen Daten aus der Registrierung zu entfernen. Beachten Sie, dass der Leistungsschlüssel **der Anwendung vorhanden** sein muss, damit das **unlodctr-Tool** erfolgreich ist. Weitere Informationen finden Sie unter [Entfernen von Indikatornamen und Beschreibungen aus der Registrierung.](removing-counter-names-and-descriptions-from-the-registry.md)
2.  Löschen Sie **die Schlüssel** Leistung **und Verknüpfung** unter dem Schlüssel Dienste **der** Anwendung. Um diese Schlüssel zu löschen, verwenden Sie entweder das Regedt32.exe Hilfsprogramm, oder rufen [**Sie RegDeleteKey auf.**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)

 

 
