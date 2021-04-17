---
description: Wiedergabe Steuerelemente in topoedit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Wiedergabe Steuerelemente in topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553708"
---
# <a name="playback-controls-in-topoedit"></a><span data-ttu-id="2c327-103">Wiedergabe Steuerelemente in topoedit</span><span class="sxs-lookup"><span data-stu-id="2c327-103">Playback Controls in TopoEdit</span></span>

<span data-ttu-id="2c327-104">Nachdem eine Topologie aufgelöst wurde, wird Sie in der Medien Sitzung zur Wiedergabe in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="2c327-104">After a topology is resolved, it is queued on the Media Session for playback.</span></span> <span data-ttu-id="2c327-105">Topoedit bietet eine Transportsteuerung zum Ändern des Status der Topologie in der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2c327-105">TopoEdit provides transport control for changing the state of topology on the Media Session.</span></span>

<span data-ttu-id="2c327-106">In der folgenden Tabelle sind der Menübefehl bzw. der Symbolleisten Befehl sowie die entsprechende Media Foundation-Methode für jeden Vorgang aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c327-106">The following table shows the menu/toolbar command and the equivalent Media Foundation method for each operation.</span></span>



| <span data-ttu-id="2c327-107">Menü/Symbolleisten Befehl</span><span class="sxs-lookup"><span data-stu-id="2c327-107">Menu/Toolbar Command</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="2c327-108">Media Foundation-Methode</span><span class="sxs-lookup"><span data-stu-id="2c327-108">Media Foundation Method</span></span>                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2c327-109">Klicken Sie  im Menü Steuerelemente **auf wieder** geben. \[ Zeilen \] vorschaltfläche-oder- \[ neue Linie \] Klicken Sie auf die **Wiedergabe** Schaltfläche auf der Symbolleiste (in der folgenden Abbildung dargestellt). \[ neueinzeilige \] ![ Bildschirm Abbildung der Wiedergabe Schaltfläche](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span><span class="sxs-lookup"><span data-stu-id="2c327-109">On the **Controls** menu, click **Play**.\[newline\] -or-\[newline\] click the **play** button on the toolbar (shown in the following image).\[newline\]![screen shot of the play button](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span></span>    | [<span data-ttu-id="2c327-110">**Imfmediasession:: Start**</span><span class="sxs-lookup"><span data-stu-id="2c327-110">**IMFMediaSession::Start**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| <span data-ttu-id="2c327-111">Klicken Sie im Menü Steuer **Elemente** auf " **Abbrechen**". \[ Zeilen \] vorschaltfläche-oder- \[ neue Zeile \] Klicken Sie auf der Symbolleiste auf die Schaltfläche zum **Abbrechen** (in der folgenden Abbildung dargestellt). \[ neueinzeilige \] ![ Bildschirm Abbildung der Schaltfläche "Abbrechen"](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span><span class="sxs-lookup"><span data-stu-id="2c327-111">On the **Controls** menu, click **Stop**.\[newline\] -or-\[newline\] click the **stop** button on the toolbar (shown in the following image).\[newline\]![screen shot of the stop button](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span></span>    | [<span data-ttu-id="2c327-112">**Imfmediasession:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="2c327-112">**IMFMediaSession::Stop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| <span data-ttu-id="2c327-113">Klicken Sie  im Menü Steuerelemente **auf Anhalten**. \[ Zeilen \] vorschaltfläche-oder- \[ neue Zeile \] Klicken Sie auf **der** Symbolleiste auf die Schaltfläche Anhalten (in der folgenden Abbildung dargestellt). \[ neueinzeilige \] ![ Bildschirm Abbildung der Pause-Schaltfläche](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span><span class="sxs-lookup"><span data-stu-id="2c327-113">On the **Controls** menu, click **Pause**.\[newline\] -or-\[newline\] click the **pause** button on the toolbar (shown in the following image).\[newline\]![screen shot of the pause button](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span></span> | [<span data-ttu-id="2c327-114">**Imfmediasession::P ause**</span><span class="sxs-lookup"><span data-stu-id="2c327-114">**IMFMediaSession::Pause**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

<span data-ttu-id="2c327-115">Informationen zum programmgesteuerten Steuern der Wiedergabe mithilfe Media Foundation APIs finden Sie unter [How to Control Presentation States](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="2c327-115">For information about controlling the playback programmatically by using Media Foundation APIs, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="seeking"></a><span data-ttu-id="2c327-116">Diejenigen</span><span class="sxs-lookup"><span data-stu-id="2c327-116">Seeking</span></span>

<span data-ttu-id="2c327-117">Wenn die Topologie suchbar ist, können Sie mithilfe der Suchleiste (in der folgenden Abbildung gezeigt) einen Speicherort in der Zeitachse der Topologie angeben, um die Wiedergabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="2c327-117">If the topology is seekable, you can seek by using the seek bar (shown in the following image) to specify a place in the topology's timeline to begin playback.</span></span>

![Screenshot der Suchleiste](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> <span data-ttu-id="2c327-119">Wenn die Medienquelle suchbar ist, sucht der Befehl zum Abbrechen auch nach der Topologie zurück zum Anfang des Streams.</span><span class="sxs-lookup"><span data-stu-id="2c327-119">If the media source is seekable, the Stop command also seeks the topology back to the start of the stream.</span></span>

 

## <a name="changing-the-playback-rate"></a><span data-ttu-id="2c327-120">Ändern der Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="2c327-120">Changing the Playback Rate</span></span>

<span data-ttu-id="2c327-121">Wenn die zugrunde liegende Medienquelle für die Topologie mehrere Wiedergabe Raten unterstützt, können Sie mit der Raten Leiste die Wiedergabe Rate ändern.</span><span class="sxs-lookup"><span data-stu-id="2c327-121">If the underlying media source for the topology supports multiple playback rates, you can use the rate bar to change the playback rate.</span></span> <span data-ttu-id="2c327-122">Erhöhen Sie den Schieberegler nach rechts, wie in der folgenden Abbildung gezeigt, um eine Topologie in der Medien Sitzung schnell weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="2c327-122">To fast-forward a topology on the Media Session, increase the rate by dragging the slider to the right, as shown in the following image.</span></span>

![Screenshot der Raten Leiste](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> <span data-ttu-id="2c327-124">In dieser Version unterstützt topoedit nur positive Raten.</span><span class="sxs-lookup"><span data-stu-id="2c327-124">In this version, TopoEdit only supports positive rates.</span></span> <span data-ttu-id="2c327-125">Die umgekehrte Wiedergabe wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2c327-125">Reverse playback is not supported.</span></span>

 

<span data-ttu-id="2c327-126">Informationen zum programmgesteuerten Ändern der Wiedergabe Rate mithilfe Media Foundation APIs finden Sie unter [Informationen zur Raten Kontrolle](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="2c327-126">For information about changing the playback rate programmatically by using Media Foundation APIs, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c327-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c327-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c327-128">Topoedit-Menüs</span><span class="sxs-lookup"><span data-stu-id="2c327-128">TopoEdit Menus</span></span>](topoedit-menus.md)
</dt> <dt>

[<span data-ttu-id="2c327-129">Topoedit-Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="2c327-129">TopoEdit Toolbar</span></span>](topoedit-toolbar.md)
</dt> <dt>

[<span data-ttu-id="2c327-130">Topoedit</span><span class="sxs-lookup"><span data-stu-id="2c327-130">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



