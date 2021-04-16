---
description: Einige Typen, die von TSPI definiert werden, sind nicht transparente Handles.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Nicht transparente Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527098"
---
# <a name="opaque-handles"></a>Nicht transparente Handles

Einige Typen, die von TSPI definiert werden, sind nicht transparente Handles. Diese werden in TSPI als öffentliche Verweise auf private Datenstrukturen verwendet. Dies ermöglicht die Typüberprüfung von Parametern, die für die Schnittstellen Prozeduren bereitgestellt werden, während trotzdem ein Measure vom Typ "Protection" Nur der Besitzer der privaten Datenstruktur weiß, wie der nicht transparente Typ als Verweis auf seine Datenstruktur Darstellung interpretiert werden kann. Als Beispiel für die Verwendung von nicht transparenten Handles sollten Sie ein Telefongerät in Erwägung gezogen. TAPI und der Dienstanbieter verwalten in der Regel Datenstrukturen, die die jeweiligen Ansichten des Geräts darstellen.

In typischen Telefondaten Strukturen, die von TAPI und einem Dienstanbieter verwaltet werden, enthält jedes ein undurchsichtiges Handle für die andere Datenstruktur. Diese wurden in einem frühen Initialisierungs Schritt ausgetauscht. Wenn TAPI eine TSPI-Funktion aufruft, übergibt er das nicht transparente handle, um auf das Gerät zu verweisen. Der Dienstanbieter weiß, wie dieser als Verweis (Pfeil) zur Datenstruktur aufgelöst werden kann. Ein ähnlicher Prozess tritt auf, wenn der Dienstanbieter eine Rückruffunktion in TAPI aufruft.

 

 



