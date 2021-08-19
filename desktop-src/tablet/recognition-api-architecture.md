---
description: Eine Ink-fähige Anwendung kommuniziert über die ApIs der Tablet PC-Plattform mit dem Erkennungssystem.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Architektur der Erkennungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59775658bcda2ecafd142476e6ff48ccdda2e82b31af62d5f49b218513f9b326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966893"
---
# <a name="recognition-api-architecture"></a>Architektur der Erkennungs-API

Eine Ink-fähige Anwendung kommuniziert über die ApIs der Tablet PC-Plattform mit dem Erkennungssystem. Anwendungen verwenden dazu [**das IInkRecognizer-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) Die Tablet PC-Plattform interagiert mit Ihrer Erkannten, indem sie die in diesem Abschnitt dokumentierten Schnittstellen im C-Stil verwendet. In der folgenden Abbildung zeigt der Bereich innerhalb der gestrichelten Linie, was in diesem Abschnitt dokumentiert ist.

![Abbildung der Erkennungsarchitektur mit hervorgehobener Erkennung](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

Eine benutzerdefinierte Recognizer muss Recapis.h enthalten (standardmäßig installiert in C: \\ Programme Microsoft Tablet PC Platform SDK \\ \\ Include). Sofern nicht anders angegeben, muss Ihre Dynamic Link Library (DLL) alle API-Funktionen exportieren, auch wenn Sie einige von ihnen E \_ NOTIMPL zurückgeben möchten.

Unter keinen Umständen wird Ihre Erkennen direkt von einer Ink-fähigen Anwendung aufgerufen. Stattdessen rufen Anwendungen entweder die Automation-APIs oder die verwalteten APIs auf, um Ergebnisse von Ihrer Erkannten zu erhalten.

 

 



