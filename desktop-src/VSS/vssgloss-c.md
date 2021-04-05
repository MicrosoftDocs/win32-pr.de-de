---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751553"
---
# <a name="c-volume-shadow-copy-service"></a>C (Volumeschattenkopie-Dienst)

[a](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**Zertifizierungsstelle**
</dt> <dd>

Eine Entität, die zur Ausstellung von Zertifikaten anvertraut ist, die behaupten, dass der Empfänger, der Computer oder die Organisation, der das Zertifikat anfordert, die Bedingungen einer festgelegten

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**vom Client zugänglichen Schatten Kopie**
</dt> <dd>

Eine Schatten Kopie, die vom Systemanbieter zur Unterstützung von Schattenkopien für freigegebene Ordner und anderen Roll Back Mechanismen erstellt wird, die es Clients ermöglichen, alte Versionen von Dateien anzuzeigen und Fehler rückgängig zu machen, ohne eine vollständige Wiederherstellung zu erfordern Eine vom Client zugängliche Schatten Kopie wird mithilfe des **VSS \_ ctx- \_ Clients \_** erstellt, auf den zugegriffen werden kann. der [**\_ VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) -momentaufnahmenaufzählungs Kontext Außerdem wird der barrierefreie VSS-Volsnap attr-Client, auf den zugegriffen werden kann, \_ \_ \_ \_ die Enumeration der [**\_ VSS-Volumesnapshot- \_ \_ \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) automatisch für die vom Client zugänglichen Schatten Kopien festlegen. Siehe auch [*Schattenkopien für freigegebene Ordner*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**Zulieferern**
</dt> <dd>

Eine Gruppe von Dateien, die von einem Writer definiert werden und bei Sicherungs-und Wiederherstellungs Vorgängen als Einheit behandelt werden müssen. Siehe auch [*Datenbankkomponente*](vssgloss-d.md), [*Dateigruppen Komponente*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**Komponenten Abhängigkeit**
</dt> <dd>

Eine Situation, in der eine von einem Writer verwaltete Komponente (und der von ihr festgelegte Komponenten Satz) unabhängig von den von anderen Writern verwalteten Komponenten nicht gesichert oder wieder hergestellt werden kann. Eine Abhängigkeit gibt keine bevorzugte Reihenfolge zwischen der Komponente und den dokumentierten Abhängigkeiten und den Komponenten an, von denen Sie abhängt: eine Abhängigkeit gibt lediglich an, dass die Komponente und die Komponenten, von denen Sie abhängt, immer gemeinsam gesichert oder wieder hergestellt werden müssen.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**Komponenten Modus**
</dt> <dd>

Ein Modus, in dem ein Sicherungs-oder Wiederherstellungs Vorgang die Komponenten Informationen eines Writers nutzt. Siehe auch [*auswählbare Komponente*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**Komponenten Satz**
</dt> <dd>

Eine Gruppe von Komponenten, bei der mindestens eine auswählbare Komponente (für die Sicherungs-oder Wiederherstellungs Komponente) und eine Reihe nicht auswählbarer Komponenten in einer Hierarchie durch ihre logischen Pfade organisiert sind. Die implizite Teilnahme an einem Sicherungs-oder Wiederherstellungs Vorgang hängt von der expliziten Einbindung der auswählbaren Komponente der obersten Ebene ab. Im Dokument mit den Sicherungs Komponenten sind nur die Komponenten Informationen dieser auswählbaren Komponente enthalten. Ein Komponenten Satz kann auswählbare und nicht auswählbare unter Komponenten enthalten. Siehe auch [*logischer Pfad*](vssgloss-l.md), [*auswählbare Komponente*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**Schatten Kopie beim Kopieren bei Schreibvorgang**
</dt> <dd>

Eine Schatten Kopie, die erstellt wird, indem nur die Unterschiede vom ursprünglichen Volume gespeichert werden.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**Status "Absturz konsistent"**
</dt> <dd>

Der Status der Datenträger, die mit dem nach einem schwerwiegenden Fehler zu finden sind, der das System plötzlich heruntergefahren hat. Eine Wiederherstellung von einem solchen Schattenkopiesatz wäre äquivalent zu einem Neustart nach einem abrupten Herunterfahren. Dies ist der Standardzustand von Daten, die ohne Unterstützung von Writern als Schatten kopiert wurden.

</dd> </dl>

 

 



