---
title: DVC-Client-APIs
description: Die CLIENT-APIs des dynamischen virtuellen Kanals (DYNAMIC Virtual Channel, DVC) werden speziell für den Remotedesktopverbindung -Client (RDC) der Verbindung implementiert.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557f51adbf10562465f93a101e502632a791d5c272b278c5a8b7ea6124637913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130816"
---
# <a name="dvc-client-apis"></a>DVC-Client-APIs

Die CLIENT-APIs des dynamischen virtuellen Kanals (DYNAMIC Virtual Channel, DVC) werden speziell für den Remotedesktopverbindung -Client (RDC) der Verbindung implementiert. Einige der APIs werden vom DVC-Framework und einige vom Plug-In-Entwickler implementiert. Einige der APIs werden zur Unterstützung des Remotedesktopverbindung-Client-Plug-Ins (RDC) verwendet und stehen nicht direkt im Zusammenhang mit dem Datentransport.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Ermöglicht das Remotedesktopverbindung Client-Plug-In (RDC), das vom Remotedesktopverbindung(RDC)-Client geladen werden kann.

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Verwaltet die Konfigurationseinstellungen für jeden Listener für die Verbindung mit dem dynamischen virtuellen Kanal (Dynamic Virtual Channel, DVC).

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Wird verwendet, um das Remotedesktopverbindung Client-Plug-In (RDC) über eingehende Anforderungen an einem bestimmten Listener zu benachrichtigen.

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Verwaltet alle Remotedesktopverbindung Client-Plug-Ins (RDC) und DVC-Listener (Dynamischer virtueller Kanal).

</dd> <dt>

[**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Wird verwendet, um den Kanalzustand zu steuern, und schreibt auf den Kanal.

</dd> <dt>

[**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Empfängt Benachrichtigungen zu Kanalzustandsänderungen oder empfangenen Daten.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Diese Schnittstelle wird nicht unterstützt.

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

Wird aufgerufen, damit das Plug-In eine Instanz der [**IWTSPlugin-Schnittstelle**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) für alle Plug-Ins erstellt, die von der DLL implementiert werden.

</dd> </dl>

 

 




