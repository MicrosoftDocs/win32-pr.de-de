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
# <a name="playback-controls-in-topoedit"></a>Wiedergabe Steuerelemente in topoedit

Nachdem eine Topologie aufgelöst wurde, wird Sie in der Medien Sitzung zur Wiedergabe in die Warteschlange eingereiht. Topoedit bietet eine Transportsteuerung zum Ändern des Status der Topologie in der Medien Sitzung.

In der folgenden Tabelle sind der Menübefehl bzw. der Symbolleisten Befehl sowie die entsprechende Media Foundation-Methode für jeden Vorgang aufgeführt.



| Menü/Symbolleisten Befehl                                                                                                                                                                                                                          | Media Foundation-Methode                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Klicken Sie  im Menü Steuerelemente **auf wieder** geben. \[ Zeilen \] vorschaltfläche-oder- \[ neue Linie \] Klicken Sie auf die **Wiedergabe** Schaltfläche auf der Symbolleiste (in der folgenden Abbildung dargestellt). \[ neueinzeilige \] ![ Bildschirm Abbildung der Wiedergabe Schaltfläche](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)    | [**Imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| Klicken Sie im Menü Steuer **Elemente** auf " **Abbrechen**". \[ Zeilen \] vorschaltfläche-oder- \[ neue Zeile \] Klicken Sie auf der Symbolleiste auf die Schaltfläche zum **Abbrechen** (in der folgenden Abbildung dargestellt). \[ neueinzeilige \] ![ Bildschirm Abbildung der Schaltfläche "Abbrechen"](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)    | [**Imfmediasession:: Beendigung**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| Klicken Sie  im Menü Steuerelemente **auf Anhalten**. \[ Zeilen \] vorschaltfläche-oder- \[ neue Zeile \] Klicken Sie auf **der** Symbolleiste auf die Schaltfläche Anhalten (in der folgenden Abbildung dargestellt). \[ neueinzeilige \] ![ Bildschirm Abbildung der Pause-Schaltfläche](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg) | [**Imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

Informationen zum programmgesteuerten Steuern der Wiedergabe mithilfe Media Foundation APIs finden Sie unter [How to Control Presentation States](how-to-control-presentation-states.md).

## <a name="seeking"></a>Diejenigen

Wenn die Topologie suchbar ist, können Sie mithilfe der Suchleiste (in der folgenden Abbildung gezeigt) einen Speicherort in der Zeitachse der Topologie angeben, um die Wiedergabe zu starten.

![Screenshot der Suchleiste](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> Wenn die Medienquelle suchbar ist, sucht der Befehl zum Abbrechen auch nach der Topologie zurück zum Anfang des Streams.

 

## <a name="changing-the-playback-rate"></a>Ändern der Wiedergabe Rate

Wenn die zugrunde liegende Medienquelle für die Topologie mehrere Wiedergabe Raten unterstützt, können Sie mit der Raten Leiste die Wiedergabe Rate ändern. Erhöhen Sie den Schieberegler nach rechts, wie in der folgenden Abbildung gezeigt, um eine Topologie in der Medien Sitzung schnell weiterzuleiten.

![Screenshot der Raten Leiste](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> In dieser Version unterstützt topoedit nur positive Raten. Die umgekehrte Wiedergabe wird nicht unterstützt.

 

Informationen zum programmgesteuerten Ändern der Wiedergabe Rate mithilfe Media Foundation APIs finden Sie unter [Informationen zur Raten Kontrolle](about-rate-control.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topoedit-Menüs](topoedit-menus.md)
</dt> <dt>

[Topoedit-Symbolleiste](topoedit-toolbar.md)
</dt> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 



