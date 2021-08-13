---
title: State-Eigenschaft
description: Die State-Eigenschaft beschreibt den Status eines Objekts zu einem zeitpunkt. Alle -Objekte unterstützen die State-Eigenschaft.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e174e938dd6252852ded6de957a54f6f94264aa811bd5bb76094af7bbba61f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564418"
---
# <a name="state-property"></a>State-Eigenschaft

Die **State-Eigenschaft** beschreibt den Status eines Objekts zu einem zeitpunkt. Alle -Objekte unterstützen die **State-Eigenschaft.**

Die **State-Eigenschaft** wird durch Aufrufen von [**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)abgerufen.

Microsoft Active Accessibility stellt in oleacc.h definierte [Objektzustandskonstanten](object-state-constants.md)bereit, die kombiniert werden, um den Zustand eines Objekts zu identifizieren. Es wird empfohlen, dass Serverentwickler diese vordefinierten Zustandswerte verwenden. Wenn vordefinierte Zustandswerte zurückgegeben werden, verwenden Clients [**GetStateText,**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) um eine lokalisierte Zeichenfolge abzurufen, die den Zustand beschreibt.

Bei Grafiken, die gelegentlich animiert werden, sollte die **State-Eigenschaft** auf [**STATE SYSTEM \_ \_ ANIMATED**](object-state-constants.md) und die [**Role-Eigenschaft**](role-property.md) auf [**ROLE SYSTEM \_ \_ GRAPHIC**](object-roles.md)festgelegt sein.

 

 




