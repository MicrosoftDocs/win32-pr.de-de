---
description: Der Unimodem- oder Universal Modem Driver, TSP (Unimdm.tsp) bietet Zugriff auf fast alle Standardmodems.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem-TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4562ad7692c288a963db27b6859fa5c472d8ff80017e2726c277fbf9d24452be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011900"
---
# <a name="unimodem-tsp"></a>Unimodem-TSP

Der Unimodem- oder Universal Modem Driver, TSP (Unimdm.tsp) bietet Zugriff auf fast alle Standardmodems. Es unterstützt Sprachmodems, die Halbduplexstreaming ermöglichen. Sie werden vom Wave-MSP unterstützt, und die Streamsteuerung ist möglich. (Beachten Sie, dass Unimodem Windows NT 4.0 oder früher keine Sprachmodems unterstützt, sodass keine direkte Streamsteuerung möglich ist.)

Dieser TSP unterstützt den [**Adresstypwert**](./lineaddresstype--constants.md) LINEADDRESSTYPE \_ PHONENUMBER. Wenn der Programmierer die Wählregeln verwenden möchte, muss die TAPI 3 [**ITAddressTranslation-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) oder die TAPI 2 [**lineTranslateAddress-Funktion**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) verwendet werden, um eine Wählbare Zeichenfolge von einer Telefonnummer im kanonischen Format zu erhalten.

Der Unimodem-TSP wird mit den Betriebssystemen Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Edition Edition, Windows 98 und Windows 95 installiert.

 

 
