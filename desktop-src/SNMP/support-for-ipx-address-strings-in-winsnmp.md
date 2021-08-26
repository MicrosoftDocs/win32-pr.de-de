---
title: Unterstützung für IPX-Adresszeichenfolgen in WinSNMP
description: WinSNMP 2.0 formalisiert die Verwendung von IPX-Adresszeichenfolgen.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: debd25897c32515b880ff82f691aa0421af6358ae72c7e49de3408d55bcbd609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886080"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a>Unterstützung für IPX-Adresszeichenfolgen in WinSNMP

WinSNMP 2.0 formalisiert die Verwendung von IPX-Adresszeichenfolgen. Wenn Sie eine IPX-Adresszeichenfolge als Eingabeparameter für die [**SnmpStrToEntity-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) angeben, müssen Sie die Zeichenfolge mit den folgenden Standards formatieren:

-   Eine Netzwerknummer, die aus acht Hexadezimalziffern besteht (bei Bedarf mit Null gefüllt)
-   Ein Trennzeichen (entweder ":", "." oder " – ")
-   Eine Knotennummer, die aus 12 Hexadezimalziffern besteht (bei Bedarf mit Null gefüllt)

Beispiel: 00000001:00081A0D01C2 oder 00000001.00081a0d01c2. Hexadezimalziffern können Groß- oder Kleinbuchstaben sein.

Dies ist das Format, das die [**SnmpEntityToStr-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) verwendet, um eine IPX-Adresszeichenfolge zurückzugeben. Die Zeichenfolge wird zurückgegeben, wenn eine Anwendung, die in einem der SNMPAPI \_ UNTRANSLATED-Modi arbeitet, die **SnmpEntityToStr-Funktion aufruft.** Die Zeichenfolge kann auch zurückgegeben werden, wenn die Anwendung im SNMPAPI TRANSLATED-Modus ausgeführt wird \_ und kein benutzerfreundlicher Name für die Entität verfügbar ist.

 

 




