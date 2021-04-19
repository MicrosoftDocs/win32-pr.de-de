---
description: Das Unimodem oder der universelle Modem Treiber, TSP (Unimdm. TSP), bietet Zugriff auf fast alle Standard Modems.
ms.assetid: 1ea60477-f6c9-44ae-969c-515dfb0c607e
title: Unimodem-TSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115cc4fd159b2e62062171131f583bad19dc9b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363334"
---
# <a name="unimodem-tsp"></a>Unimodem-TSP

Das Unimodem oder der universelle Modem Treiber, TSP (Unimdm. TSP), bietet Zugriff auf fast alle Standard Modems. Es unterstützt Sprachmodems, die das Halbduplex Streaming ermöglichen. Sie werden von der Wave-MSP unterstützt, und die Datenstrom Steuerung ist möglich. (Beachten Sie, dass Unimodem unter Windows NT 4,0 oder früher keine Sprachmodems unterstützt, daher ist die direkte Datenstrom Steuerung nicht möglich.)

Dieser TSP unterstützt den [**Adresstyp**](./lineaddresstype--constants.md) Wert lineadresssstype \_ PhoneNumber. Wenn der Programmierer die Wähl Regeln verwenden möchte, muss die TAPI 3 [**itadresstranslations**](/windows/win32/api/tapi3if/nn-tapi3if-itaddresstranslation) -Schnittstelle oder die TAPI 2 [**linetranslateaddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) -Funktion verwendet werden, um eine als zulässig einsetzbare Zeichenfolge aus einer Telefonnummer im kanonischen Format abzurufen.

Der Unimodem-TSP wird mit den Betriebssystemen Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Millennium Edition, Windows 98 und Windows 95 installiert.

 

 
