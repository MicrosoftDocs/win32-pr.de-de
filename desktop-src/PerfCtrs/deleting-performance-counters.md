---
description: Führen Sie die folgenden Schritte aus, um die Anwendungs Leistungsindikatoren aus dem System zu entfernen.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Löschen von Leistungsindikatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360543"
---
# <a name="deleting-performance-counters"></a>Löschen von Leistungsindikatoren

Führen Sie die folgenden Schritte aus, um die Leistungsindikatoren der Anwendung aus dem System zu entfernen.

1.  Verwenden Sie das **unlodctr** -Tool, das auf dem Computer enthalten ist, um die gegenseitig relevanten Daten aus der Registrierung zu entfernen. Beachten Sie, dass der **Leistungs** Schlüssel der Anwendung vorhanden sein muss, damit das **unlodctr** -Tool erfolgreich ausgeführt werden konnte. Weitere Informationen finden Sie unter [Entfernen von Counter-Namen und Beschreibungen aus der Registrierung](removing-counter-names-and-descriptions-from-the-registry.md).
2.  Löschen Sie die **Leistungs** -und **Verknüpfungs** Schlüssel unter dem **Dienst** Schlüssel der Anwendung. Um diese Schlüssel zu löschen, verwenden Sie entweder das Regedt32.exe-Hilfsprogramm oder den Befehl [**regdeletekey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).

 

 
