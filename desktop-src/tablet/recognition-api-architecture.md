---
description: Eine frei Hand fähige Anwendung kommuniziert mit dem Erkennungssystem über die Tablet PC Platform-APIs.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Erkennungs-API-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560861"
---
# <a name="recognition-api-architecture"></a>Erkennungs-API-Architektur

Eine frei Hand fähige Anwendung kommuniziert mit dem Erkennungssystem über die Tablet PC Platform-APIs. Anwendungen verwenden das [**iinkrecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) -Objekt, um dies zu erreichen. Die Tablet PC-Plattform interagiert mit Ihrem Erkennungs Modul, indem Sie die Schnittstellen im C-Stil verwenden, die in diesem Abschnitt dokumentiert sind. In der folgenden Abbildung zeigt der Bereich in der gestrichelten Linie, was in diesem Abschnitt dokumentiert ist.

![Abbildung der Erkennungs Architektur mit hervorgehobenem Erkennungs Modul](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

Eine benutzerdefinierte Erkennung muss "recapis. h" enthalten (standardmäßig installiert in C: \\ Programme \\ Microsoft Tablet PC Platform SDK \\ include). Sofern nicht erwähnt, muss ihre Dynamic Link Library (dll) alle API-Funktionen exportieren, auch wenn Sie festlegen, dass einige von Ihnen E \_ notimpl zurückgeben.

Unter keinen Umständen wird Ihre Erkennung direkt von einer frei Hand fähigen Anwendung aufgerufen. Stattdessen werden von Anwendungen entweder die Automation-APIs oder die verwalteten APIs aufgerufen, um Ergebnisse von ihrer Erkennung zu erhalten.

 

 



