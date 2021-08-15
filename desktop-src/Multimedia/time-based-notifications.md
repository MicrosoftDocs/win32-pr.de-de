---
title: Time-Based Benachrichtigungen
description: Time-Based Benachrichtigungen
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- -Benachrichtigungen
- -Nachrichten
- -Benachrichtigungen, zeitbasierte Benachrichtigungen
- zeitbasierte Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80052d5e728a7a5b00e6177a36c30f470fe80daeafbe39a12aa4c9a883766534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688250"
---
# <a name="time-based-notifications"></a>Time-Based Benachrichtigungen

Sie können das Betriebssystem benachrichtigen, in regelmäßigen Abständen Nachrichten an eine Anwendung zu senden, indem Sie den *fChanged-Parameter* von [**"sollenSetCapture"**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) auf **FALSE** festlegen und die Länge des Intervalls zwischen aufeinander folgenden Nachrichten angeben. Weisen Sie dazu dem *uPeriod-Parameter* einen Wert zwischen den minimalen und maximalen Abrufhäufigkeiten für das 30-000-000-30-000-000-000-Verhältnis zu. Sie können diesen Bereich ermitteln, indem Sie die [**funktion "attributGetDevCaps"**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) verwenden, die die **Member wPeriodMin** und **wPeriodMax** in der [**WRCAPS-Struktur ausfüllt.**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) Wenn der *uPeriod-Wert* außerhalb des Bereichs der gültigen Abrufhäufigkeiten für das 30-0-System liegt, verwendet der Treiber die minimale oder maximale Abrufhäufigkeit, je nachdem, welcher Wert näher am *uPeriod-Wert* liegt.

> [!Note]  
> Windows richtet ein Timerereignis mit jedem Aufruf von **"ungSetCapture" ein.**

 

 

 