---
description: Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, eine Grafik oder ein Textobjekt so nah wie möglich an der ursprünglichen Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei Bildverarbeitungstechnologien und Farbfunktionen zwischen Geräten.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled Gerätekontextfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33337aeea32f1ca84b74e3fc45e9bd67dbfe1ce1a5300a502a5303f55cab357
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944200"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled Gerätekontextfunktionen

Microsoft Image Color Management (ICM) stellt sicher, dass ein Farbbild, eine Grafik oder ein Textobjekt so nah wie möglich an der ursprünglichen Absicht auf jedem Gerät gerendert wird, trotz der Unterschiede bei Bildverarbeitungstechnologien und Farbfunktionen zwischen Geräten. (Weitere Informationen finden Sie unter [Windows Color System](/previous-versions//dd372446(v=vs.85)).)

Es gibt verschiedene Funktionen in der Grafikgeräteschnittstelle (GDI), die Farbdaten verwenden oder verarbeiten. Die folgenden Gerätekontextfunktionen sind für die Verwendung mit ICM:

-   [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**Auswählenobjekt**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
