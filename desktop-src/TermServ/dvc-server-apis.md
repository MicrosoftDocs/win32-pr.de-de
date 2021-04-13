---
title: DVC-Server-APIs
description: Die Server-APIs des dynamischen virtuellen Kanals werden vom RDC-Server (Remotedesktopverbindung) der Verbindung implementiert.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390889"
---
# <a name="dvc-server-apis"></a>DVC-Server-APIs

Die Server-APIs des dynamischen virtuellen Kanals werden vom RDC-Server (Remotedesktopverbindung) der Verbindung implementiert.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Iwtsserverchannel**](iwtsserverchannel.md)
</dt> <dd>

Diese Schnittstelle wird nicht unterstützt.

</dd> <dt>

[**Iwtsserverchannelmanager**](iwtsserverchannelmanager.md)
</dt> <dd>

Diese Schnittstelle wird nicht unterstützt.

</dd> <dt>

[**Tpriority**](tpriority.md)
</dt> <dd>

Diese Enumeration wird nicht verwendet.

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>Verhaltensänderungen für andere Server-APIs

-   Die Server-API wurde mit einem zusätzlichen-Rückruf erweitert, der einen dynamischen virtuellen Kanal (DVC) öffnet. Der zusätzliche-Befehl wird mithilfe der [**WFS virtualchannelopenex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) -Funktion durchgeführt.
-   [**Wout virtualchannelread**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    Wenn diese API mit DVC verwendet wird, werden die mit der [**\_ channelpdu- \_ Kopfzeile**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)gelesenen Daten immer vorangestellt. Dies bedeutet, dass jeder Lesevorgang durchgeführt werden muss, wenn mindestens der Datenblock " **Channel \_ PDU \_ length** " als Eingabepuffer übergeben wird.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Wenn das Datei Handle für den DVC durch Aufrufen von [**wzvirtualchannelquery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) mit dem Parameter *wtionvirtualfilehandle* abgerufen wird, wird dieselbe Regel angewendet. Alle Lesevorgänge enthalten den [**\_ PDU- \_ Header des Kanals**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), und der Lese Puffer muss mindestens die **\_ \_ Länge der channelpdu** aufweisen.

 

 