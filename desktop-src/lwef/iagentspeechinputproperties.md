---
title: Iagentspeechinputproperties
description: Iagentspeechinputproperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387931"
---
# <a name="iagentspeechinputproperties"></a>Iagentspeechinputproperties

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Iagentspeechinputproperties ermöglicht den Zugriff auf die Spracheingabe Eigenschaften, die vom Server verwaltet werden. Die meisten Eigenschaften sind für Client Anwendungen schreibgeschützt, aber der Benutzer kann Sie auf der Eigenschaften Seite des Microsoft-Agents ändern. Der Microsoft-Agent-Server gibt Werte nur dann zurück, wenn eine kompatible Sprach-Engine installiert und aktiviert ist. Wenn Sie diese Eigenschaften Abfragen, wird versucht, die Sprach-Engine zu starten.

**Methoden in Vtable-Reihenfolge**



| Iagentspeechinputproperties-Methoden                                     | BESCHREIBUNG                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**GetEnabled**](iagentspeechinputproperties--getenabled.md)           | Gibt zurück, ob die Spracherkennungs-Engine aktiviert ist. |
| [**GetHotKey**](iagentspeechinputproperties--gethotkey.md)             | Gibt die aktuelle Schlüsselzuweisung des Abhör Schlüssels zurück.  |
| [**Getlisteningtip**](iagentspeechinputproperties--getlisteningtip.md) | Gibt zurück, ob der Abhör Tipp aktiviert ist.             |



 

Die Methoden [**getinstallierte**](https://www.bing.com/search?q=**GetInstalled**), [**GetLcid**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)und [**ltengine**](https://www.bing.com/search?q=**SetEngine**) (in früheren Versionen des Microsoft-Agents unterstützt) werden weiterhin aus Gründen der Abwärtskompatibilität unterstützt. Allerdings werden die Methoden nicht als Stub und keine nützlichen Werte zurückgegeben. Verwenden Sie [**getsrmodeid**](https://www.bing.com/search?q=**GetSRModeID**) und [**setsrmodeid**](https://www.bing.com/search?q=**SetSRModeID**) , um die Spracherkennungs-Engine abzufragen und festzulegen, die mit dem Zeichen verwendet werden soll. Beachten Sie, dass die Engine die aktuelle Spracheinstellung des Zeichens entsprechen muss.

 

 




