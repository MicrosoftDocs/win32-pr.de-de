---
title: Time-Based Benachrichtigungen
description: Time-Based Benachrichtigungen
ms.assetid: cf7bc0d4-f3bd-4416-b85f-0ff51a0efbbc
keywords:
- Benachrichtigungen, Benachrichtigungen
- meldungen, nachrichten
- Benachrichtigungen, zeitbasierte Benachrichtigungen
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

Sie können das Betriebssystem benachrichtigen, in regelmäßigen Abständen Nachrichten an eine Anwendung zu senden, indem Sie den *fChanged-Parameter* von [**"ouSetCapture"**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) auf **FALSE** festlegen und die Intervalllänge zwischen aufeinanderfolgenden Nachrichten angeben. Weisen Sie hierzu dem *uPeriod-Parameter* einen Wert zwischen der minimalen und der maximalen Abrufhäufigkeit für die Teilung zu. Sie können diesen Bereich mithilfe der [**funktiongetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) bestimmen, die die **Member wPeriodMin** und **wPeriodMax** in der [**STRUKTUR VON CABCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) ausfüllt. Wenn der *uPeriod-Wert* außerhalb des Bereichs gültiger Abrufhäufigkeiten für das Intervall liegt, verwendet der Fahrer die minimale oder maximale Abrufhäufigkeit, je nachdem, welcher Wert näher am *uPeriod-Wert* liegt.

> [!Note]  
> Windows richtet bei jedem Aufruf von **"ousetCapture"** ein Timerereignis ein.

 

 

 