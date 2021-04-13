---
title: Registrieren des Protokoll-Managers
description: Sie müssen mindestens einen Registrierungs Wert Eintrag für den Protokoll-Manager erstellen, damit der Remotedesktopdienste Dienst ihn instanziieren kann.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388129"
---
# <a name="registering-the-protocol-manager"></a>Registrieren des Protokoll-Managers

Sie müssen mindestens einen Registrierungs Wert Eintrag für den Protokoll-Manager erstellen, damit der Remotedesktopdienste Dienst ihn instanziieren kann.

## <a name="registry-location"></a>Registrierungsstandort

Erstellen Sie einen Registrierungsschlüssel an folgendem Speicherort für jeden Listener ([**iwrdsprotocollistener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)), den das Protokoll verwendet. In diesem Beispiel werden die neuen listenerschlüssel als *MyListener1* und *MyListener2* bezeichnet.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

Als Referenz können Sie die Werte Einträge unter dem Standard **-RDP-TCP-** listenerschlüssel an diesem Speicherort anzeigen.

## <a name="registry-value-entries"></a>Registrierungs Wert Einträge

Der listenerschlüssel für das Protokoll muss einen Wert Eintrag mit dem Namen **loadableprotocol \_** aufweisen.<dl> <dt>

Datentyp
</dt> <dd>REG_SZ</dd> </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**Iwrdsproprocolmanager**</a> -Schnittstelle.) Der Remotedesktopdienste-Dienst verwendet diese CLSID, um den Protokoll-Manager für diesen Listener zu instanziieren, nachdem er den Listener in der Registrierung gefunden hat.

Wenn Ihr Protokoll Anbieter mehr als einen Listener verwendet, erstellt der Remotedesktopdienste-Dienst nur eine Instanz des Protokoll-Managers und verwendet ihn, um für jeden Listener [**einen einmal**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) aufzurufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Remotedesktopprotokoll Anbieters](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Methoden aufrufssequenz](method-call-sequence.md)
</dt> </dl>

 

 




