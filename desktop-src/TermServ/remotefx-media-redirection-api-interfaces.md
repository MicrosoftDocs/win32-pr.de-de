---
title: RemoteFX Schnittstellen der Medienumleitungs-API
description: Die RemoteFX-API für die Medienumleitung unterstützt die folgenden Schnittstellen.
ms.assetid: 9fb19c56-67a8-40f1-b6f1-8448eb83b38c
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f148e88fea7fc7fc540323c199b8feae3c63fd57c62f232518c21ec6433cdea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127630"
---
# <a name="remotefx-media-redirection-api-interfaces"></a>RemoteFX Schnittstellen der Medienumleitungs-API

Die RemoteFX-API für die Medienumleitung unterstützt die folgenden Schnittstellen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**IWTSBitmapRenderer**](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderer)
</dt> <dd>

Wird von einem dynamischen Plug-In für virtuelle Kanäle zum Rendern von Bitmaps verwendet.

</dd> <dt>

[**IWTSBitmapRendererCallback**](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderercallback)
</dt> <dd>

Ein dynamisches Plug-In für virtuelle Kanäle implementiert diese Schnittstelle, um benachrichtigt zu werden, wenn sich die Größe des Renderingbereichs ändert.

</dd> <dt>

[**IWTSBitmapRenderService**](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsbitmaprenderservice)
</dt> <dd>

Dieser Dienst wird verwendet, um eine visuelle Zuordnung auf dem Client zu erstellen, die einem zugeordneten Fenster auf dem Server entspricht.

</dd> <dt>

[**IWTSPluginServiceProvider**](/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtspluginserviceprovider)
</dt> <dd>

Bietet eine Möglichkeit für Dynamic Virtual Channel-Plug-Ins, verschiedene Clientdienste Remotedesktop abfragen.

</dd> </dl>

 

 




