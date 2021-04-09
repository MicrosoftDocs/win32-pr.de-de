---
description: Wenn ein Fehler auftritt, geben die meisten Systemfunktionen einen Fehlercode zurück, normalerweise 0, NULL oder &\# 8211; 1.
ms.assetid: fd5b0d6e-78cf-4f51-b61d-d32576cd485a
title: Last-Error-Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bf0fe2f544fc3d87690be81b0d09767745ef95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958221"
---
# <a name="last-error-code"></a>Last-Error-Code

Wenn ein Fehler auftritt, geben die meisten Systemfunktionen einen Fehlercode zurück, normalerweise 0, **null** oder – 1. Viele Systemfunktionen legen außerdem einen zusätzlichen Fehlercode fest, der als *Letzter Fehlercode* bezeichnet wird. Dieser Fehlercode wird für jeden laufenden Thread separat verwaltet. ein Fehler in einem Thread überschreibt nicht den letzten Fehlercode in einem anderen Thread. Jede Funktion kann die Funktion " [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) " oder " [**setlasterrorex**](/windows/desktop/api/Winuser/nf-winuser-setlasterrorex) " aufrufen, um den letzten Fehlercode für den aktuellen Thread festzulegen. Diese Funktionen sind hauptsächlich für Dynamic Link Libraries (dll) vorgesehen, sodass Sie Informationen für die aufrufenden Anwendung bereitstellen können. Beachten Sie, dass einige Funktionen **SetLastError** oder **setlasterrorex** mit 0 aufrufen, wenn Sie erfolgreich sind, und den von der zuletzt fehlgeschlagenen Funktion festgelegten Fehlercode zurücksetzen, während andere dies nicht tun.

Eine Anwendung kann den letzten Fehlercode mithilfe der [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion abrufen. der Fehlercode kann darüber informieren, was tatsächlich aufgetreten ist, damit die Funktion fehlschlägt. In der Dokumentation für Systemfunktionen werden die Bedingungen angegeben, unter denen die Funktion den letzten Fehlercode festlegt.

Das System definiert eine Reihe von Fehlercodes, die als letzte Fehlercodes festgelegt oder von diesen Funktionen zurückgegeben werden können. Fehlercodes sind 32-Bit-Werte (Bit 31 ist das signifikanteste Bit). Bit 29 ist für Anwendungs definierte Fehlercodes reserviert. Dieses Bit ist für keinen Systemfehler Code festgelegt. Wenn Sie Fehlercodes für Ihre Anwendung definieren, legen Sie dieses Bit fest, um anzugeben, dass der Fehlercode von einer Anwendung definiert wurde, und um sicherzustellen, dass die Fehlercodes nicht mit System definierten Fehlercodes in Konflikt stehen. Weitere Informationen finden Sie unter Winerror. h und [System Fehler Codes](system-error-codes.md).

 

 
