---
title: Unterstützung für USB 3,0
description: Unterstützung für USB 3,0
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730760"
---
# <a name="support-for-usb-30"></a>Unterstützung für USB 3,0

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

In Windows 8 und Windows Server 2012 haben wir Unterstützung für USB 3,0 hinzugefügt. Hierzu haben wir einen neuen Software Stapel hinzugefügt, um den USB 3,0-Host Controller (erweiterbarer Host Controller, XHC) zu schalten. Wir haben Schnittstellen Parität, iriql-Ebene, Aufruferkontext, Fehlerstatus, Wiederholungs Häufigkeit usw. beibehalten. Bei der Interaktion mit einem Gerät, das über USB 2,0 und USB 3,0 verbunden ist, sollten Sie keinen Unterschied haben.

Wenn Sie jedoch einen Treiber für ein neues USB 3,0-Gerät schreiben, entscheiden Sie sich definitiv für neue USB 3,0-Funktionen.

## <a name="manifestation"></a>Ausstrahlung

Geräte Übertragungen werden schneller und weniger Energieverbrauch von PCs durch USB-Geräte beansprucht. Wenn eine Verbindung mit einem USB 3,0-Port besteht, besteht das Risiko, dass vorhandene USB-Geräte nicht ordnungsgemäß funktionieren. Dies sollte nicht der Fall sein, und es ist nicht zu erwarten, aber da die Software, die USB 3,0 unterstützt, neu ist, ist dies ein Risiko.

 

 




