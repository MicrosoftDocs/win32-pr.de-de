---
title: Registrieren des Protokoll-Managers
description: Sie müssen mindestens einen Registrierungswerteintrag für Ihren Protokoll-Manager erstellen, damit Remotedesktopdienste Dienst ihn instanziieren kann.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851fe74d7e22a068eccd0d901cab14d754b6b2364611bfdda2aecd68dcf224d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988790"
---
# <a name="registering-the-protocol-manager"></a>Registrieren des Protokoll-Managers

Sie müssen mindestens einen Registrierungswerteintrag für Ihren Protokoll-Manager erstellen, damit Remotedesktopdienste Dienst ihn instanziieren kann.

## <a name="registry-location"></a>Registrierungsstandort

Erstellen Sie einen Registrierungsschlüssel am folgenden Speicherort für jeden Listener [**(IWRdsProtocolListener),**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)den Ihr Protokoll verwendet. In diesem Beispiel heißen die neuen Listenerschlüssel *MyListener1* und *MyListener2.*

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

Als Referenz können Sie die Werteinträge unter dem standardmäßigen **RDP-Tcp-Listenerschlüssel** an diesem Speicherort anzeigen.

## <a name="registry-value-entries"></a>Registrierungswerteinträge

Der Listenerschlüssel für das Protokoll muss über einen Werteintrag namens **LoadableProtocol \_ Object verfügen.**<dl> <dt>

Datentyp
</dt> <dd>REG_SZ</dd> </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager-Schnittstelle.)**</a> Der Remotedesktopdienste verwendet diese CLSID, um den Protokoll-Manager für diesen Listener zu instanziieren, nachdem er den Listener in der Registrierung gefunden hat.

Wenn Ihr Protokollanbieter mehr als einen Listener verwendet, erstellt der Remotedesktopdienste-Dienst nur eine Instanz des Protokoll-Managers und verwendet ihn zum einmaligen Aufrufen von [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) für jeden Listener.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Remotedesktopprotokoll Anbieters](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Methodenaufrufsequenz](method-call-sequence.md)
</dt> </dl>

 

 




