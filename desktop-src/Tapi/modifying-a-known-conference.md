---
description: Das folgende Codefragment veranschaulicht die Änderung eines Konferenzzeitbereichs. Die Standardzeit beträgt 30 Minuten. In diesem Fragment ist die Zeitspanne auf ein Jahr festgelegt.
ms.assetid: 7f05d62e-2bcc-4d98-8a71-97ed20a12af2
title: Ändern einer bekannten Konferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b139b05f70f801a28b91ecb6c2773fd740f10df7c0fd2b8e86b904b210cc50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575600"
---
# <a name="modifying-a-known-conference"></a>Ändern einer bekannten Konferenz

\[Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Das folgende Codefragment veranschaulicht die Änderung des Zeitraums einer Konferenz. Die Standardzeit beträgt 30 Minuten. In diesem Fragment ist die Zeitspanne auf ein Jahr festgelegt.

Dieses Fragment setzt voraus, dass bereits [eine Verbindung mit einem ILS-Server](connecting-to-an-ils-server.md) hergestellt wurde und dass eine [Konferenzverzeichnisenumeration](enumerating-conference-directories.md) durchgeführt wurde, um den Verzeichniseintrag abzurufen, der geändert wird.

Dieses Fragment geht auch davon aus, dass es sich nicht um eine Multicastkonferenz handelt. Zum Ändern der Zeiten auf einer Multicastkonferenz ist eine Benachrichtigung des Multicastadresszuordnungsservers erforderlich. Ein Beispiel für die Arbeit mit Multicastadressierung finden Sie unter [Abrufen einer Multicastadresse.](acquiring-a-multicast-address.md)


```C++
// If ( hr != S_OK ) process the error here. 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> </dl>

 

 



