---
description: Einige von TSPI definierte Typen sind nicht transparente Handles.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Nicht transparente Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de2daf3e5d486215ced5f16eac64930bd177b2072e54f6e7b8ecc0ccec49765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404520"
---
# <a name="opaque-handles"></a>Nicht transparente Handles

Einige von TSPI definierte Typen sind nicht transparente Handles. Diese werden in TSPI als öffentliche Verweise auf private Datenstrukturen verwendet. Dies ermöglicht die Typüberprüfung von Parametern, die für die Schnittstellenprozessen bereitgestellt werden, während dennoch ein Maß für Typschutz gegeben wird. Nur der Besitzer der privaten Datenstruktur weiß, wie der nicht transparente Typ als Verweis auf seine Datenstrukturdarstellung interpretiert werden kann. Als Beispiel für die Verwendung von nicht transparenten Ziehpunkten sollten Sie ein Telefongerät in Betracht ziehen. Sowohl TAPI als auch der Dienstanbieter verwalten in der Regel Datenstrukturen, die ihre jeweiligen Ansichten des Geräts darstellen.

In typischen Telefondatenstrukturen, die von TAPI und einem Dienstanbieter verwaltet werden, enthält jede ein nicht transparentes Handle für die andere Datenstruktur. Diese wurden in einem frühen Initialisierungsschritt ausgetauscht. Wenn TAPI eine TSPI-Funktion aufruft, übergibt sie das nicht transparente Handle, um auf das Gerät zu verweisen. Der Dienstanbieter weiß, wie dieser als Verweis (Pfeil) in seine Datenstruktur aufgelöst werden kann. Ein ähnlicher Prozess tritt auf, wenn der Dienstanbieter eine Rückruffunktion in TAPI aufruft.

 

 



