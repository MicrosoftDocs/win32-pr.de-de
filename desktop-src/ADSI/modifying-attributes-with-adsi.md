---
title: Ändern von Attributen mit ADSI
description: Um Attributwerte zu ändern, stellt ADSI die Methoden IADs. Put und IADs. PutEx bereit. Mit diesen Methoden werden die Daten im Client seitigen Cache geändert. Die IADs. * tinfo-Methode muss aufgerufen werden, um die Änderungen im Verzeichnis zu übertragen.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Ändern von Attributen mit ADSI
- Attribute ADSI, ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391013"
---
# <a name="modifying-attributes-with-adsi"></a>Ändern von Attributen mit ADSI

Um Attributwerte zu ändern, stellt ADSI die Methoden [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) bereit. Mit diesen Methoden werden die Daten im Client seitigen Cache geändert. Die [**IADs. * tinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode muss aufgerufen werden, um die Änderungen im Verzeichnis zu übertragen.

> [!Note]  
> Wenn für mehrere Attribut Änderungen ein Commit in einem einzelnen [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)*-Befehl ausgeführt wird, wenn ein einzelnes Attribut nicht geändert werden kann, wird keines der Attribute geändert. Wenn Sie z. b. die Attribute " [**SN**](/windows/desktop/ADSchema/a-sn) " und " [**givenName**](/windows/desktop/ADSchema/a-givenname) " ändern und das " [**telefonienumber**](/windows/desktop/ADSchema/a-telephonenumber) "-Attribut eines Benutzer Objekts ohne nachfolgende Aufrufe der **SetInfo** -Methode löschen, werden die Änderungen beim Aufrufen von **SetInfo** eingegeben. Wenn eine oder mehrere der Änderungen nicht zulässig sind und daher nicht ausgeführt werden können, werden keine der an den Attributen vorgenommenen Änderungen beim **Abrufen von "***" eingegeben.

 

Die [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) -Methode nimmt einen Attributnamen und einen Variant-Parameter an. Verwenden Sie diese Methode, um Attribute festzulegen, die sowohl einzelne als auch mehrere Werte enthalten.

Die [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode bietet Kontrolle über Vorgänge für mehrwertige Attribute. Sie können vorhandene Werte anfügen, löschen, aktualisieren und löschen. Die **IADs. PutEx** -Methode erwartet immer ein Variant-Array von Attributwerten. Sie können diese Methode jedoch auch verwenden, um ein Attribut mit einem einzelnen Wert festzulegen.

Die [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) -Methode verwendet die Vorgänge, die durch die Enumeration der [**ADS- \_ Eigenschafts \_ Operation \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) festgelegt werden.

 

 