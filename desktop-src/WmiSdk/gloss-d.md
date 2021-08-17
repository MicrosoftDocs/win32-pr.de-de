---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2310ce8b14baf2b57634cfa36ef83c3dab239503632972b67bdc4cc6a9b1f602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924156"
---
# <a name="d-wmi"></a>D (WMI)

[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F G](gloss-f.md) [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) T [U](gloss-t.md) V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**Datetime**
</dt> <dd>

Weitere Informationen [*finden Sie unter CIM datetime*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**Entkoppelter Anbieter**
</dt> <dd>

Ein Anbieter, der in einem anderen Prozess als WMI-Prozess ausgeführt wird. Entkoppelte Anbieter sind die empfohlene Methode zum Instrumentierten einer Anwendung, da der Anbieter seine eigene Lebensdauer steuern kann, anstatt jedes Mal gestartet zu werden, wenn ein Benutzer über WMI auf den Anbieter zutritt.

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**Direkter Zugriff**
</dt> <dd>

Eine Möglichkeit, auf Eigenschaften und Methoden zu zugreifen, die von WMI in einem Skript bereitgestellt werden, als ob es sich um Automatisierungseigenschaften und -methoden von [**SWbemObject wäre.**](swbemobject.md)

Nicht-direktionaler Zugriff: `VolumeName = MyDisk.Properties_("VolumeName")`

Direkter Zugriff: `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Distributed Management Task Force (DMTF)**
</dt> <dd>

Eine internationale Standardsorganisation, die mit wichtigen Technologieanbietern zusammenarbeiten kann, einschließlich Microsoft, um die Entwicklung, Einführung und Vereinheitlichung von Verwaltungsstandards und Initiativen für Desktop-, Unternehmens- und Internetumgebungen zu leiten.

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**
</dt> <dd>

Weitere Informationen *finden Sie unter Distributed Management Task Force (DMTF).*

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**dynamische Klasse**
</dt> <dd>

Eine CIM-Klasse, deren Definition bei Bedarf [*von einem*](gloss-p.md) Anbieter zur Laufzeit bereitgestellt wird. Dynamische Klassen stellen anbieterspezifische verwaltete [*Objekte dar*](gloss-m.md) und werden nicht im [*CIM-Repository gespeichert.*](gloss-c.md) Dynamische Klassen unterstützen nur *dynamische Instanzen.*

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**Dynamische Instanz**
</dt> <dd>

Eine Instanz einer CIM-Klasse, die bei Bedarf von einem [*Anbieter*](gloss-p.md) bereitgestellt wird. Sie wird nicht im [*CIM-Repository gespeichert.*](gloss-c.md) Dynamische Instanzen können für statische oder dynamische Klassen bereitgestellt werden. Die dynamische Unterstützung von Instanzen einer Klasse ermöglicht einem Anbieter die Bereitstellung von Eigenschaftswerten bis zu [*einer Minute.*](gloss-p.md)

</dd> </dl>

 

 



