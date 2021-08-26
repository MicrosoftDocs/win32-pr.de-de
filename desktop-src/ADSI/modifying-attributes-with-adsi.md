---
title: Ändern von Attributen mit ADSI
description: Um Attributwerte zu ändern, stellt ADSI die Methoden IADs.Put und IADs.PutEx bereit. Diese Methoden ändern die Daten im clientseitigen Cache. Die IADs.SetInfo-Methode muss aufgerufen werden, um die Änderungen an das Verzeichnis zu committen.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Ändern von Attributen mit ADSI
- Attribute ADSI , Ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef82d6a3d4c486fcd1fca1f5cba7ae62f57e66e713ed84551a5a9372cdc86683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079960"
---
# <a name="modifying-attributes-with-adsi"></a>Ändern von Attributen mit ADSI

Um Attributwerte zu ändern, stellt ADSI die [**Methoden IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) bereit. Diese Methoden ändern die Daten im clientseitigen Cache. Die [**IADs.SetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) muss aufgerufen werden, um die Änderungen an das Verzeichnis zu committen.

> [!Note]  
> Wenn bei einem einzelnen Aufruf von [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)ein Commit für mehrere Attributänderungen ausgeführt wird, wird keines der Attribute geändert, wenn ein einzelnes Attribut nicht geändert werden kann. Wenn Sie z. B. die Attribute [**sn**](/windows/desktop/ADSchema/a-sn) und [**givenName**](/windows/desktop/ADSchema/a-givenname) ändern und das [**attribut telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) eines Benutzerobjekts ohne nachfolgende Aufrufe der **SetInfo-Methode** löschen, werden die Änderungen beim Aufrufen von **SetInfo** eingegeben. Wenn eine oder mehrere der Änderungen nicht zulässig sind und daher nicht ausgeführt werden können, werden während des Aufrufs von **SetInfo** keine der an den Attributen vorgenommenen gemeinsamen Änderungen eingegeben.

 

Die [**IADs.Put-Methode**](/windows/desktop/api/Iads/nf-iads-iads-put) verwendet einen Attributnamen und einen Variant-Parameter. Verwenden Sie diese Methode, um Attribute festzulegen, die sowohl einzelne als auch mehrere Werte enthalten.

Die [**IADs.PutEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-putex) ermöglicht die Steuerung von Vorgängen für mehrwertige Attribute. Sie können vorhandene Werte anfügen, löschen, aktualisieren und löschen. Die **IADs.PutEx-Methode** erwartet immer ein variants Array von Attributwerten. Sie können diese Methode jedoch auch verwenden, um ein Attribut mit einem einzelnen Wert festzulegen.

Die [**IADs.PutEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-putex) verwendet die von der [**ADS PROPERTY OPERATION \_ \_ \_ ENUM-Enumeration angegebenen**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) Vorgänge.

 

 