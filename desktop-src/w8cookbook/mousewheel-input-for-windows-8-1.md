---
title: Mausradeingabe für Windows 8.1
description: Mausradeingabe für Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2285d2a0456376b01289ac7a4c2607117441384ebd13b0aaf0a162eac50fdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211383"
---
# <a name="mousewheel-input-for-windows-81"></a>Mausradeingabe für Windows 8.1

## <a name="platform"></a>Plattform

<dl> Clients – Windows 8.1  
Server – Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

In Windows 8.1 werden Mausradereignisse nicht mehr basierend auf dem Tastaturfokus übermittelt, wie in früheren Versionen von Windows. Wenn Windows 8.1 mit der Maus auf eine Store-App bewegen, wird das Mausrad an diese App übermittelt. Aus Kompatibilitätsgründen wird das Mausrad jedoch weiterhin basierend auf dem Tastaturfokus übermittelt, wenn der Mauszeiger auf eine Desktop-Appzeigerzeiger ist.

## <a name="manifestations"></a>Manifestationen

Wenn der Mauszeiger mit dem Mauszeiger auf Store Apps klickt, führt das Mausrad einen Bildlauf für alle anwendbaren Inhalte durch, ohne dass der Benutzer auf die Store muss. Dies gilt auch für den Startbildschirm. Dadurch wird das Scrollen mit dem Mausrad zu einer einfacheren Interaktion in Windows 8.1 als in Windows 8.

## <a name="mitigation"></a>Minderung

In den meisten Jahren sollte diese Änderung keine Auswirkungen auf vorhandene Apps haben. Wenn eine Store-App erst nach der Registrierung eines Mausklickereignisses auf Mausradereignisse laused, reagiert diese App wahrscheinlich erst, wenn der Benutzer aktiv darauf geklickt hat. Daher ist der wahrscheinlichste Nachteil hier einfach, dass eine App weiterhin wie in der Windows 8. Bei Desktop-Apps bietet der Tastaturfokus der App keine Mausradeingabe mehr, aber dies führt auch nicht zu einer Unterbrechung dieser Apps. Daher sind keine kurzfristigen Entschärfungen erforderlich.

## <a name="solution"></a>Lösung

Store App-Entwickler sollten davon ausgehen, Mausradereignisse ohne ein vorzappungsbereites Mausklickereignis zu empfangen. Sie sollten beispielsweise nicht erst nach dem Registrieren eines Mausklicks auf Mausradereignisse lauschen. Ebenso sollten Desktopanwendungen nicht versuchen, Mausradereignisse zu erfassen (z. B. durch Festlegen eines Hooks auf niedriger Ebene), wenn sie den Tastaturfokus haben.

## <a name="tests"></a>Tests

Store app developers should test on Windows 8.1 to verify that all scrolling functionality works whenever the mouse is hingovering over the app. Desktop-App-Entwickler sollten Windows 8.1 testen, um sicherzustellen, dass sie keine Mausradereignisse erfassen (wie oben beschrieben).

 

 




