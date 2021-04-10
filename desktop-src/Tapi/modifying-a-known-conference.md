---
description: Das folgende Code Fragment veranschaulicht die Änderung einer Zeitspanne für Konferenzen. Der Standard Zeitraum beträgt 30 Minuten. In diesem Fragment ist die Zeitspanne auf ein Jahr festgelegt.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Ändern einer bekannten Konferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bd58003b276bd3cdd54da2e7ed0df4f154311e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214367"
---
# <a name="modifying-a-known-conference"></a>Ändern einer bekannten Konferenz

\[Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Das folgende Code Fragment veranschaulicht die Änderung der Zeitspanne einer Konferenz. Der Standard Zeitraum beträgt 30 Minuten. In diesem Fragment ist die Zeitspanne auf ein Jahr festgelegt.

Dieses Fragment geht davon aus, dass bereits eine [Verbindung mit einem ILS-Server](connecting-to-an-ils-server.md) hergestellt wurde und dass eine [Konferenz Verzeichnis Enumeration](enumerating-conference-directories.md) ausgeführt wurde, um den Verzeichniseintrag abzurufen, der geändert wird.

Dieses Fragment geht auch davon aus, dass es sich nicht um eine Multicast Konferenz handelt. Zum Ändern der Zeiten einer Multicast Konferenz ist eine Benachrichtigung über den Multicast Adress Zuordnungs Server erforderlich. Ein Beispiel für das Arbeiten mit der Multicast Adressierung finden Sie unter Abrufen [einer Multicast Adresse](acquiring-a-multicast-address.md) .


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Itdirectoryobjectconference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



