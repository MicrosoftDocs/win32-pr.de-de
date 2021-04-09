---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042366"
---
# <a name="d-wmi"></a>D (WMI)

[a](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**DateTime**
</dt> <dd>

Weitere Informationen finden Sie unter [*CIM DateTime*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**entkoppelter Anbieter**
</dt> <dd>

Ein Anbieter, der in einem anderen Prozess als WMI-Prozess ausgeführt wird. Entkoppelte Anbieter sind die empfohlene Methode zum Instrumentieren einer Anwendung, da der Anbieter seine eigene Lebensdauer steuern kann, anstatt jedes Mal gestartet zu werden, wenn ein Benutzer über WMI auf den Anbieter zugreift.

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**direkter Zugriff**
</dt> <dd>

Eine Möglichkeit, auf Eigenschaften und Methoden zuzugreifen, die von WMI in einem Skript bereitgestellt werden, als ob es sich um Automatisierungs Eigenschaften und-Methoden von " [**errbemubject**](swbemobject.md)" handelt

Nicht direkter Zugriff: `VolumeName = MyDisk.Properties_("VolumeName")`

Direkter Zugriff: `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**Task Force für verteilte Verwaltung (DMTF)**
</dt> <dd>

Eine internationale Standard Organisation, die mit wichtigen Technologieanbietern wie Microsoft zusammenarbeitet, um die Entwicklung, Übernahme und Vereinheitlichung von Verwaltungsstandards und-Initiativen für Desktop-, Unternehmens-und Internet Umgebungen zu unterstützt.

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**
</dt> <dd>

Siehe *verteilte Verwaltung Task Force (DMTF)*.

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**dynamische Klasse**
</dt> <dd>

Eine CIM-Klasse, deren Definition bei Bedarf von einem [*Anbieter*](gloss-p.md) zur Laufzeit bereitgestellt wird. Dynamische Klassen stellen anbieterspezifische [*verwaltete Objekte*](gloss-m.md) dar und werden nicht im CIM- [*Repository*](gloss-c.md)gespeichert. Dynamische Klassen unterstützen nur *dynamische Instanzen*.

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**dynamische Instanz**
</dt> <dd>

Eine Instanz einer CIM-Klasse, die von einem [*Anbieter*](gloss-p.md) bei Bedarf bereitgestellt wird. Sie wird nicht im CIM- [*Repository*](gloss-c.md)gespeichert. Dynamische Instanzen können für statische oder dynamische Klassen bereitgestellt werden. Durch die dynamische Unterstützung von Instanzen einer Klasse kann ein Anbieter bis zu Minuten [*Eigenschafts*](gloss-p.md) Werte bereitstellen.

</dd> </dl>

 

 



