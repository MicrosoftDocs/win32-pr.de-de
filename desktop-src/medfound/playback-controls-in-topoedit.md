---
description: Wiedergabesteuerelemente in TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Wiedergabesteuerelemente in TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c59dfceb30f839ba58d37385a3178d42429eb858c98f3f5196dd95141ac2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239692"
---
# <a name="playback-controls-in-topoedit"></a>Wiedergabesteuerelemente in TopoEdit

Nachdem eine Topologie aufgelöst wurde, wird sie in der Mediensitzung zur Wiedergabe in die Warteschlange gestellt. TopoEdit bietet Transportsteuerung zum Ändern des Topologiezustands in der Mediensitzung.

Die folgende Tabelle zeigt den Menü-/Symbolleistenbefehl und die entsprechende Media Foundation für jeden Vorgang.



| Menü-/Symbolleistenbefehl                                                                                                                                                                                                                          | Media Foundation-Methode                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Klicken Sie **im Menü** Steuerelemente auf **Wieder geben.** \[ "newline" oder "newline" klicken auf der Symbolleiste auf die \] Wiedergabeschaltfläche \[ \] (in der folgenden Abbildung dargestellt).  \[ Screenshot der \] ![ Wiedergabeschaltfläche](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**DURCHSTARTMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| Klicken Sie **im Menü** Steuerelemente auf **Beenden.** \[ "newline" oder "newline" klicken Sie auf der Symbolleiste auf die Schaltfläche \] \[ "Beenden" \] (in der folgenden Abbildung dargestellt).  \[ Screenshot der \] ![ Stoppschaltfläche](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**VERERBUNGMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| Klicken Sie **im Menü** Steuerelemente auf **Anhalten.** \[ "newline" oder "newline" klicken Sie auf der Symbolleiste auf die Schaltfläche "Anhalten" \] \[ \] (in der folgenden Abbildung dargestellt).  \[ Screenshot der \] ![ Pausenschaltfläche](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**VERERBUngssitzung::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Informationen zum programmgesteuerten Steuern der Wiedergabe mithilfe von Media Foundation-APIs finden Sie unter [Steuern von Präsentationszuständen.](how-to-control-presentation-states.md)

## <a name="seeking"></a>Suchen

Wenn die Topologie durchsetzbar ist, können Sie mithilfe der Suchleiste (wie in der folgenden Abbildung dargestellt) einen Ort in der Topologiezeitachse angeben, um mit der Wiedergabe zu beginnen.

![Screenshot der Suchleiste](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Wenn die Medienquelle durchsetzbar ist, sucht der Befehl Stop auch die Topologie zurück zum Anfang des Streams.

 

## <a name="changing-the-playback-rate"></a>Ändern der Wiedergaberate

Wenn die zugrunde liegende Medienquelle für die Topologie mehrere Wiedergaberaten unterstützt, können Sie die Ratenleiste verwenden, um die Wiedergaberate zu ändern. Um eine Topologie in der Mediensitzung schnell vorwärts zu bringen, erhöhen Sie die Rate, indem Sie den Schieberegler nach rechts ziehen, wie in der folgenden Abbildung dargestellt.

![Screenshot der Preisleiste](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> In dieser Version unterstützt TopoEdit nur positive Raten. Die umgekehrte Wiedergabe wird nicht unterstützt.

 

Informationen zum programmgesteuerten Ändern der Wiedergaberate mithilfe von Media Foundation-APIs finden Sie unter Informationen zur [Rate Control](about-rate-control.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TopoEdit-Menüs](topoedit-menus.md)
</dt> <dt>

[TopoEdit-Symbolleiste](topoedit-toolbar.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



