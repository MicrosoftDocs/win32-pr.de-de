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
# <a name="dvc-server-apis"></a><span data-ttu-id="9bcc4-103">DVC-Server-APIs</span><span class="sxs-lookup"><span data-stu-id="9bcc4-103">DVC Server APIs</span></span>

<span data-ttu-id="9bcc4-104">Die Server-APIs des dynamischen virtuellen Kanals werden vom RDC-Server (Remotedesktopverbindung) der Verbindung implementiert.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-104">The dynamic virtual channel (DVC) server APIs are implemented by the Remote Desktop Connection (RDC) server of the connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9bcc4-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9bcc4-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="9bcc4-106">**Iwtsserverchannel**</span><span class="sxs-lookup"><span data-stu-id="9bcc4-106">**IWTSServerChannel**</span></span>](iwtsserverchannel.md)
</dt> <dd>

<span data-ttu-id="9bcc4-107">Diese Schnittstelle wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-107">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="9bcc4-108">**Iwtsserverchannelmanager**</span><span class="sxs-lookup"><span data-stu-id="9bcc4-108">**IWTSServerChannelManager**</span></span>](iwtsserverchannelmanager.md)
</dt> <dd>

<span data-ttu-id="9bcc4-109">Diese Schnittstelle wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-109">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="9bcc4-110">**Tpriority**</span><span class="sxs-lookup"><span data-stu-id="9bcc4-110">**TPriority**</span></span>](tpriority.md)
</dt> <dd>

<span data-ttu-id="9bcc4-111">Diese Enumeration wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-111">This enumeration is not used.</span></span>

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a><span data-ttu-id="9bcc4-112">Verhaltensänderungen für andere Server-APIs</span><span class="sxs-lookup"><span data-stu-id="9bcc4-112">Changes in Behavior for Other Server APIs</span></span>

-   <span data-ttu-id="9bcc4-113">Die Server-API wurde mit einem zusätzlichen-Rückruf erweitert, der einen dynamischen virtuellen Kanal (DVC) öffnet.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-113">The server API has been extended with an additional call which opens a dynamic virtual channel (DVC).</span></span> <span data-ttu-id="9bcc4-114">Der zusätzliche-Befehl wird mithilfe der [**WFS virtualchannelopenex**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) -Funktion durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-114">The additional call is made using the [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) function.</span></span>
-   [<span data-ttu-id="9bcc4-115">**Wout virtualchannelread**</span><span class="sxs-lookup"><span data-stu-id="9bcc4-115">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    <span data-ttu-id="9bcc4-116">Wenn diese API mit DVC verwendet wird, werden die mit der [**\_ channelpdu- \_ Kopfzeile**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)gelesenen Daten immer vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-116">When using this API with DVC, it will always prepend the data read with [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span></span> <span data-ttu-id="9bcc4-117">Dies bedeutet, dass jeder Lesevorgang durchgeführt werden muss, wenn mindestens der Datenblock " **Channel \_ PDU \_ length** " als Eingabepuffer übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-117">This means that any read must be done with at least the **CHANNEL\_PDU\_LENGTH** data block passed as the input buffer.</span></span>

-   [<span data-ttu-id="9bcc4-118">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="9bcc4-118">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    <span data-ttu-id="9bcc4-119">Wenn das Datei Handle für den DVC durch Aufrufen von [**wzvirtualchannelquery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) mit dem Parameter *wtionvirtualfilehandle* abgerufen wird, wird dieselbe Regel angewendet.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-119">If the file handle to the DVC is retrieved by calling [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) with parameter *WTSVirtualFileHandle*, the same rule will apply.</span></span> <span data-ttu-id="9bcc4-120">Alle Lesevorgänge enthalten den [**\_ PDU- \_ Header des Kanals**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), und der Lese Puffer muss mindestens die **\_ \_ Länge der channelpdu** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9bcc4-120">All reads will include the [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), and the read buffer has to be at least **CHANNEL\_PDU\_LENGTH** size.</span></span>

 

 