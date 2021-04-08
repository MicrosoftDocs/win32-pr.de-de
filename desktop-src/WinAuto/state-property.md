---
title: State-Eigenschaft
description: Die State-Eigenschaft beschreibt den Status eines Objekts zu einem bestimmten Zeitpunkt. Alle-Objekte unterstützen die State-Eigenschaft.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856860"
---
# <a name="state-property"></a>State-Eigenschaft

Die **State** -Eigenschaft beschreibt den Status eines Objekts zu einem bestimmten Zeitpunkt. Alle-Objekte unterstützen die **State** -Eigenschaft.

Die **State** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)abgerufen.

Microsoft Active Accessibility bietet in Oleacc. h definierte [Objekt Zustands Konstanten](object-state-constants.md), die zum Identifizieren des Zustands eines Objekts kombiniert werden. Es wird empfohlen, dass Server Entwickler diese vordefinierten Zustands Werte verwenden. Wenn vordefinierte Zustands Werte zurückgegeben werden, wird [**getstatetext**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) von Clients verwendet, um eine lokalisierte Zeichenfolge abzurufen, die den Zustand beschreibt.

Für Grafiken, die gelegentlich animiert werden, sollte die Eigenschaft **State** auf [**State \_ System \_ animiert**](object-state-constants.md) und die [**Role**](role-property.md) -Eigenschaft auf [**Role System- \_ \_ Grafik**](object-roles.md)festgelegt sein.

 

 




