---
title: DVC-Server-APIs
description: Die SERVER-APIs des dynamischen virtuellen Kanals (DYNAMIC Virtual Channel, DVC) werden vom Remotedesktopverbindung (RDC)-Server der Verbindung implementiert.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f43ab4032e4500732e2f9ee6cfa9a2c17f8b1892e55973ba633758792f00bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353973"
---
# <a name="dvc-server-apis"></a>DVC-Server-APIs

Die SERVER-APIs des dynamischen virtuellen Kanals (DYNAMIC Virtual Channel, DVC) werden vom Remotedesktopverbindung (RDC)-Server der Verbindung implementiert.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**IWTSServerChannel**](iwtsserverchannel.md)
</dt> <dd>

Diese Schnittstelle wird nicht unterstützt.

</dd> <dt>

[**IWTSServerChannelManager**](iwtsserverchannelmanager.md)
</dt> <dd>

Diese Schnittstelle wird nicht unterstützt.

</dd> <dt>

[**TPriority**](tpriority.md)
</dt> <dd>

Diese Enumeration wird nicht verwendet.

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>Verhaltensänderungen für andere Server-APIs

-   Die Server-API wurde um einen zusätzlichen Aufruf erweitert, der einen dynamischen virtuellen Kanal (Dynamic Virtual Channel, DVC) öffnet. Der zusätzliche Aufruf erfolgt mithilfe der [**WTSVirtualChannelOpenEx-Funktion.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
-   [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    Wenn Sie diese API mit DVC verwenden, werden die gelesenen Daten immer mit [**CHANNEL \_ PDU \_ HEADER vorgefertigt.**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header) Dies bedeutet, dass jeder Lese-/Leselauf mindestens mit dem **CHANNEL \_ PDU \_ LENGTH-Datenblock** erfolgen muss, der als Eingabepuffer übergeben wird.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Wenn das Dateihandle für den DVC durch Aufrufen von [**WTSVirtualChannelQuery mit**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) dem *Parameter WTSVirtualFileHandle* abgerufen wird, gilt die gleiche Regel. Alle Leseläufe enthalten den [**CHANNEL \_ \_ PDU-HEADER,**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)und der Lesepuffer muss mindestens die **GRÖßE CHANNEL \_ PDU \_ LENGTH** haben.

 

 