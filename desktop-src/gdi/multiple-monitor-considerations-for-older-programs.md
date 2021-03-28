---
description: Im Allgemeinen benötigen ältere Anwendungen keine Änderungen, die auf mehreren Überwachungssystemen funktionieren.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Überlegungen zu mehreren überwachen für ältere Programme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978521"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a>Überlegungen zu mehreren überwachen für ältere Programme

Im Allgemeinen benötigen ältere Anwendungen keine Änderungen, die auf mehreren Überwachungssystemen funktionieren. In den meisten Fällen scheint das System nur eine Anzeige zu haben. Systemmetriken spiegeln die primäre Anzeige und Vollbild-Anwendungen auf dem primären Replikat wider. Das System verarbeitet Minimierung, Maximierung, Menüs und Dialogfelder.

Bei einigen Programmen treten jedoch Probleme auf. Bei einigen, die Probleme haben können, handelt es sich um Remote Steuerungsanwendungen, die über direkten Hardware Zugriff verfügen, und um solche, die den GDI oder Anzeigetreiber gepatcht haben. In diesen Fällen muss der Benutzer möglicherweise einen Monitor über den primären Monitor hinaus deaktivieren.

 

 



