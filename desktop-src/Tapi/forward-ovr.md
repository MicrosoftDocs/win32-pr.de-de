---
description: Weiterleitung ist die Umleitung einer eingehenden Sitzung an eine andere Zieladresse.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Weiter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddddd21a945c3ca63a5c9040b8eabe0d1056b74b2f819f3fb62dbd8b760aaca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660850"
---
# <a name="forward"></a>Weiter

Weiterleitung ist die Umleitung einer eingehenden Sitzung an eine andere Zieladresse. TAPI ermöglicht einer Anwendung, eine Liste der Weiterleitungsbedingungen für eine Adresse anzugeben. Weiterleitungsbedingungen können so genau wie ein anderes Ziel und [**Weiterleitungsmodus**](./lineforwardmode--constants.md) für jede Aufruferadresse sein.

Der Weiterleitungsvorgang kann auch verwendet werden, um ein selektives Feature ohne Störung zu implementieren, indem einige Anrufer an Voicemail weitergeleitet werden und andere versuchen, den Abschluss zu versuchen.

Der Weiterleitungsvorgang kann auch alle derzeit wirksamen Weiterleitungen abbrechen.

Einige Dienstanbieter erfordern, dass eine Anwendung vor einem Weiterleitungsvorgang einen Beratungsaufruf erstellt. Der Weiterleitungsvorgang wird dann mit einem Zeiger auf den Anruf der Beratung übergeben.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2.x:** Um [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) zum Abrufen von [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)festzulegen, ändern Sie die [**LINE \_ ADDRESSSTATE-Benachrichtigungsmeldung**](./line-addressstate.md) mit LINEADDRESSSTATE \_ FORWARD.

**TAPI 3.x:** Siehe [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), Änderungsbenachrichtigung: [**ITAddressEvent::get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ FORWARD.

> [!Note]  
> Es kann für einen Dienstanbieter unmöglich sein, jederzeit zu wissen, welche Weiterleitung für eine Adresse wirksam ist. Die Weiterleitung kann auf eine Weise abgebrochen oder geändert werden, die nicht zu einer Benachrichtigung an den Dienstanbieter führt.

 

 

 
