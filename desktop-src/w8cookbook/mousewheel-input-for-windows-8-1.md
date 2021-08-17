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

## <a name="description"></a>Beschreibung

In Windows 8.1 werden Mausradereignisse nicht mehr basierend auf dem Tastaturfokus bereitgestellt, wie in früheren Versionen von Windows. Wenn Windows 8.1 mit der Maus auf eine Store-App zeigen, wird das Mausrad an diese App übermittelt. Aus Kompatibilitätsgründen wird das Mausrad jedoch weiterhin basierend auf dem Tastaturfokus bereitgestellt, wenn die Maus auf eine Desktop-App zeigen soll.

## <a name="manifestations"></a>Manifestationen

Wenn die Maus auf Store Apps bewegt wird, scrollt der Mauszeiger durch alle anwendbaren Inhalte, ohne dass der Benutzer auf die Store App klicken muss. Dies gilt auch für den Startbildschirm. Dadurch wird das Scrollen per Mausrad zu einer einfacheren Interaktion in Windows 8.1 als in Windows 8.

## <a name="mitigation"></a>Minderung

In den meisten Teilen sollte diese Änderung keine Auswirkungen auf vorhandene Apps haben. Wenn eine Store App erst nach dem Registrieren eines Mausklickereignisses auf Mausradereignisse lauscht, reagiert diese App wahrscheinlich erst dann auf Mausrad, wenn der Benutzer aktiv darauf geklickt hat. Daher besteht der wahrscheinlichste Nachteil hier darin, dass eine App weiterhin wie in Windows 8 ausgeführt wird. Bei Desktop-Apps erhält die App durch den Tastaturfokus keine Mausradeingaben mehr, aber dies führt auch in keiner Weise dazu, dass diese Apps beeinträchtigt werden. Daher sind keine kurzfristigen Entschärfungen erforderlich.

## <a name="solution"></a>Lösung

Store App-Entwickler sollten mit dem Empfang von Mausradereignissen ohne Mausklickereignis rechnen. Sie sollten z. B. erst nach dem Registrieren eines Mausklicks auf Mausradereignisse lauschen. Auf ähnliche Weise sollten Desktopanwendungen nicht versuchen, Mausradereignisse (z. B. durch Festlegen eines Hooks auf niedriger Ebene) zu erfassen, wenn sie den Tastaturfokus haben.

## <a name="tests"></a>Tests

Store App-Entwickler sollten auf Windows 8.1 testen, um sicherzustellen, dass alle Scrollfunktionen funktionieren, wenn die Maus auf die App bewegt wird. Desktop-App-Entwickler sollten auf Windows 8.1 testen, um sicherzustellen, dass sie keine Mausradereignisse erfassen (siehe anleitung oben).

 

 




