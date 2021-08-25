---
description: Wenn ein Fehler auftritt, geben die meisten Systemfunktionen einen Fehlercode zurück, in der Regel 0, NULL oder &\# 8211;1.
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Last-Error Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd3f7a202f4ed67105620a7d2688cfa278fbdc127ed942861de0d69517e96620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912550"
---
# <a name="last-error-code"></a>Last-Error Code

Wenn ein Fehler auftritt, geben die meisten Systemfunktionen einen Fehlercode zurück, in der Regel 0, **NULL** oder –1. Viele Systemfunktionen legen auch einen zusätzlichen Fehlercode fest, der als *letzter Fehlercode bezeichnet wird.* Dieser Fehlercode wird für jeden ausgeführten Thread separat verwaltet. Ein Fehler in einem Thread überschreibt den Code des letzten Fehlers in einem anderen Thread nicht. Jede Funktion kann die [**Funktion SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) oder [**SetLastErrorEx**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) aufrufen, um den Code für den letzten Fehler für den aktuellen Thread zu festlegen. Diese Funktionen sind in erster Linie für Dynamic Link Libraries (DLL) vorgesehen, damit sie Informationen für die aufrufende Anwendung bereitstellen können. Beachten Sie, dass einige Funktionen **SetLastError** oder **SetLastErrorEx** mit 0 aufrufen, wenn sie erfolgreich sind, wobei der von der zuletzt fehlerhaften Funktion festgelegte Fehlercode zurückgewährt wird, während andere nicht.

Eine Anwendung kann den Code des letzten Fehlers mithilfe der [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) abrufen. Der Fehlercode kann mehr darüber erfahren, was tatsächlich aufgetreten ist, damit die Funktion fehlschlägt. In der Dokumentation für Systemfunktionen werden die Bedingungen angegeben, unter denen die Funktion den Code des letzten Fehlers legt.

Das System definiert einen Satz von Fehlercodes, die als Last-Error-Codes festgelegt oder von diesen Funktionen zurückgegeben werden können. Fehlercodes sind 32-Bit-Werte (Bit 31 ist das wichtigste Bit). Bit 29 ist für anwendungsdefinierte Fehlercodes reserviert. Für keinen Systemfehlercode ist dieses Bit festgelegt. Wenn Sie Fehlercodes für Ihre Anwendung definieren, legen Sie dieses Bit fest, um anzugeben, dass der Fehlercode von einer Anwendung definiert wurde, und um sicherzustellen, dass die Fehlercodes nicht mit systemdefinierten Fehlercodes in Konflikt stehen. Weitere Informationen finden Sie unter WinError.h und [Systemfehlercodes](system-error-codes.md).

 

 
