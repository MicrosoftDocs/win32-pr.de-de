---
title: Schreiben eines Client-DVC-Moduls
description: Zum Schreiben eines DVC-Clientmoduls (Dynamic Virtual Channel) müssen Sie zunächst ein Remotedesktopverbindung-Client-Plug-In (RDC) implementieren und registrieren.
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa9f365034ff7771baf8eaeca102d7156f592e71d0cedffc97cef6d75b81fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008264"
---
# <a name="writing-a-client-dvc-module"></a>Schreiben eines Client-DVC-Moduls

Zum Schreiben eines DVC-Clientmoduls (Dynamic Virtual Channel) müssen Sie zunächst ein Remotedesktopverbindung-Client-Plug-In (RDC) implementieren und registrieren. Das DVC-Plug-In ist eine Implementierung von [**IWTSPlugin,**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)die als Component Object Model -Objekt (COM) registriert ist.

> [!Note]  
> Das Plug-In muss in einem Freethreadingmodell implementiert werden. Die Implementierung des Apartmentmodells wird nicht unterstützt.

 

Im Folgenden finden Sie eine Liste der Schnittstellen, die von -Objekten implementiert werden, die vom Plug-In instanziiert werden.



| Schnittstelle                                                        | BESCHREIBUNG                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Ermöglicht das Remotedesktopverbindung Client-Plug-In (RDC), das vom Remotedesktopverbindung(RDC)-Client geladen werden kann.<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Benachrichtigt das Remotedesktopverbindung Client-Plug-In (RDC) über eingehende Anforderungen an einem bestimmten Listener.<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Empfängt Benachrichtigungen zu Kanalzustandsänderungen oder empfangenen Daten. Jede Instanz dieser Schnittstelle ist einer Instanz von [**IWTSVirtualChannel zugeordnet.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)<br/> |



 

Im Folgenden finden Sie eine Liste der Schnittstellen, die von Objekten implementiert werden, die vom Remotedesktopverbindung-Client (RDC) instanziiert werden und Teil des Frameworks sind.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Verwaltet alle Remotedesktopverbindung(RDC)-Client-Plug-Ins, DVC-Listener oder statischen virtuellen Kanäle.<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Verwaltet die Konfigurationseinstellungen für jeden Listener für die DVC-Verbindung.<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Steuert den Kanalzustand sowie Schreibvorgänge auf dem Kanal.<br/>                                           |



 

Die folgende Abbildung zeigt die Beziehung zwischen dem Remotedesktopverbindung-Client (RDC) und dem Remotedesktopverbindung-Client-Plug-In (RDC).

![Beziehung zwischen Client und Plug-In](images/tsclient.png)

 

 





