---
title: DVC-Client-APIs
description: Die DVC-Client-APIs (Dynamic Virtual Channel) werden speziell für den Remotedesktopverbindung-Client (RDC) der Verbindung implementiert.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309783"
---
# <a name="dvc-client-apis"></a>DVC-Client-APIs

Die DVC-Client-APIs (Dynamic Virtual Channel) werden speziell für den Remotedesktopverbindung-Client (RDC) der Verbindung implementiert. Einige der APIs werden vom DVC-Framework implementiert, und einige werden vom Plug-in-Entwickler implementiert. Einige der APIs werden zur Unterstützung des-Client-Plug-Ins für Remotedesktopverbindung (RDC) verwendet und sind nicht direkt mit dem Datentransport verknüpft.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Ermöglicht das Laden des-Remotedesktopverbindung (RDC)-Client-Plug-ins durch den Remotedesktopverbindung-Client (RDC).

</dd> <dt>

[**Iwunglistener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Verwaltet die Konfigurationseinstellungen für jeden Listener für die Verbindung des dynamischen virtuellen Kanals (DVC).

</dd> <dt>

[**Iwtilistenercallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Wird verwendet, um das Client-Plug-in für Remotedesktopverbindung (RDC) über eingehende Anforderungen für einen bestimmten Listener zu benachrichtigen.

</dd> <dt>

[**Iwout virtualchannelmanager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Verwaltet alle Remotedesktopverbindung (RDC)-Client-Plug-ins und-DVC-Listener (Dynamic Virtual Channel).

</dd> <dt>

[**Iwungvirtualchannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Wird verwendet, um den Kanal Zustand zu steuern und auf dem Kanal zu schreiben.

</dd> <dt>

[**Iwout virtualchannelcallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Empfängt Benachrichtigungen über Kanalstatus Änderungen oder empfangene Daten.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Diese Schnittstelle wird nicht unterstützt.

</dd> <dt>

[**Virtualchannelgetinstance**](virtualchannelgetinstance.md)
</dt> <dd>

Wird aufgerufen, damit das Plug-in eine Instanz der [**iwtsplugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) -Schnittstelle für alle Plug-Ins erstellt, die von der dll implementiert werden.

</dd> </dl>

 

 




