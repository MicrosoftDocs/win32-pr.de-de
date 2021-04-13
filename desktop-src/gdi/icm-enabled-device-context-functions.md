---
description: Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, eine Grafik oder ein Textobjekt so nah wie möglich an seine ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: Gerätekontext Funktionen ICM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978584"
---
# <a name="icm-enabled-device-context-functions"></a>Gerätekontext Funktionen ICM-Enabled

Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, eine Grafik oder ein Textobjekt so nah wie möglich an seine ursprüngliche Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei den Abbild Erstellungs Technologien und Farbfunktionen zwischen Geräten. (Weitere Informationen finden Sie unter [Windows Color System](/previous-versions//dd372446(v=vs.85)).)

Es gibt verschiedene Funktionen in der Graphics Device Interface (GDI), die Farbdaten verwenden oder verwenden. Die folgenden Gerätekontext Funktionen sind für die Verwendung mit ICM aktiviert:

-   [**"Kreatecompatibledc"**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**-**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**Getdcbrushcolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**Getdcpcolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**Setdcbrushcolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**Setdcpcolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
