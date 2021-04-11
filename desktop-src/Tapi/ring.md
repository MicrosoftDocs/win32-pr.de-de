---
description: Ein einzelnes Telefon kann ggf. mit unterschiedlichen ringmodi Klingeln.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: Ring
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959711"
---
# <a name="ring"></a>Ring

Ein einzelnes Telefon kann ggf. mit unterschiedlichen ringmodi Klingeln. Aufgrund der Vielzahl von verfügbaren ringmodi werden die ringmodi anhand ihrer ringmodusnummer identifiziert. Eine ringmodusnummer liegt zwischen 0 und der Anzahl der verfügbaren ringmodi minus 1.

Die Funktionen, die eine Anwendung zum Steuern der ringmodi eines Telefon Geräts verwenden würde, sind [**phonesetring**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), wodurch ein geöffnetes Telefongerät entsprechend einem bestimmten Ring Modus und [**phonegetring**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), das den aktuellen Ring Modus eines geöffneten Telefon Geräts zurückgibt, geklingelt wird.

Wenn der Ring Modus eines Telefon Geräts geändert wird, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendung gesendet, um die Anwendung über die Statusänderung zu benachrichtigen. Die Parameter für diese Nachricht geben Aufschluss über die Änderung.

 

 



