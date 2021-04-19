---
title: Schreiben eines Client-DVC-Moduls
description: Zum Schreiben eines c#-Client Moduls (Dynamic Virtual Channel) müssen Sie zuerst ein Remotedesktopverbindung-Client-Plug-in (RDC) implementieren und registrieren.
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339421"
---
# <a name="writing-a-client-dvc-module"></a>Schreiben eines Client-DVC-Moduls

Zum Schreiben eines c#-Client Moduls (Dynamic Virtual Channel) müssen Sie zuerst ein Remotedesktopverbindung-Client-Plug-in (RDC) implementieren und registrieren. Das DVC-Plug-in ist eine Implementierung von [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), die als Component Object Model (com)-Objekt registriert ist.

> [!Note]  
> Das Plug-in muss in einem kostenlosen Threading Modell implementiert werden. Die Implementierung von Apartment Modellen wird nicht unterstützt.

 

Im folgenden finden Sie eine Liste der Schnittstellen, die von Objekten implementiert werden, die durch das-Plug-in instanziiert werden.



| Schnittstelle                                                        | BESCHREIBUNG                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Ermöglicht das Laden des-Remotedesktopverbindung (RDC)-Client-Plug-ins durch den Remotedesktopverbindung-Client (RDC).<br/>                                                                 |
| [**Iwtilistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Benachrichtigt das Remotedesktopverbindung (RDC)-Client-Plug-in über eingehende Anforderungen für einen bestimmten Listener.<br/>                                                                             |
| [**Iwout virtualchannelcallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Empfängt Benachrichtigungen über Kanalstatus Änderungen oder empfangene Daten. Jede Instanz dieser Schnittstelle ist einer Instanz von [**iwtionvirtualchannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)zugeordnet.<br/> |



 

Im folgenden finden Sie eine Liste der Schnittstellen, die von Objekten implementiert werden, die vom-Remotedesktopverbindung (RDC)-Client instanziiert werden und Teil des-Frameworks sind.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Iwout virtualchannelmanager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Verwaltet alle Remotedesktopverbindung (RDC)-Client-Plug-ins, DVC-Listener oder statische virtuelle Kanäle.<br/> |
| [**Iwunglistener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Verwaltet die Konfigurationseinstellungen für jeden Listener für die DVC-Verbindung.<br/>                                |
| [**Iwungvirtualchannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Steuert den Kanalstatus und Schreibvorgänge auf dem Kanal.<br/>                                           |



 

In der folgenden Abbildung wird die Beziehung zwischen dem Remotedesktopverbindung-Client (RDC) und dem-Remotedesktopverbindung (RDC)-Client-Plug-in dargestellt.

![Beziehung zwischen Client und Plug-in](images/tsclient.png)

 

 





