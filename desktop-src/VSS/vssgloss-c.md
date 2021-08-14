---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e10734fa1676980473b53cb16f5cf1166d5b2ff2813f9bf59159c37116514c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751446"
---
# <a name="c-volume-shadow-copy-service"></a>C (Volumeschattenkopie-Dienst)

[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**Zertifizierungsstelle**
</dt> <dd>

Eine Entität, die mit der Ausstellung von Zertifikaten beauftragt wurde, die bestätigt, dass die Empfängerperson, der Computer oder die Organisation, die das Zertifikat anfordert, die Bedingungen einer festgelegten Richtlinie erfüllt.

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**Auf den Client zugängliche Schattenkopie**
</dt> <dd>

Eine schattenkopische Kopie, die vom Systemanbieter erstellt wurde, um Schattenkopien für freigegebene Ordner und andere Rollbackmechanismen zu unterstützen, mit denen Clients alte Versionen von Dateien anzeigen und Fehler rückgängig machen können, ohne dass eine vollständige Wiederherstellung erforderlich ist. Eine auf den Client zugängliche Schattenkopie wird mithilfe des **VSS \_ CTX \_ CLIENT \_ ACCESSIBLE-Werts** der [**\_ VSS \_ SNAPSHOT \_ CONTEXT-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) erstellt. Darüber hinaus wird der \_ VSS VOLSNAP \_ ATTR \_ CLIENT \_ ACCESSIBLE-Wert der [**\_ VSS VOLUME SNAPSHOT ATTRIBUTES-Enumeration automatisch für vom Client zugängliche \_ Schattenkopien \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) festgelegt. Siehe auch [*Schattenkopien für freigegebene Ordner*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**Komponente**
</dt> <dd>

Eine Gruppe von Dateien, die von einem Writer definiert wird und während Sicherungs- und Wiederherstellungsvorgängen als Einheit behandelt werden muss. Siehe auch [*Datenbankkomponente*](vssgloss-d.md), [*Dateigruppenkomponente*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**Komponentenabhängigkeit**
</dt> <dd>

Eine Situation, in der eine Von einem Writer verwaltete Komponente (und der von ihr festgelegte Komponentensatz) nicht unabhängig von komponenten, die von anderen Writern verwaltet werden, gesichert oder wiederhergestellt werden kann. Eine Abhängigkeit gibt keine Reihenfolge der Präferenz zwischen der Komponente mit den dokumentierten Abhängigkeiten und den Komponenten an, von denen sie abhängt: Eine Abhängigkeit gibt lediglich an, dass die Komponente und die Komponenten, von denen sie abhängt, immer zusammen gesichert oder wiederhergestellt werden müssen.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**Komponentenmodus**
</dt> <dd>

Ein Modus, in dem ein Sicherungs- oder Wiederherstellungsvorgang die Komponenteninformationen eines Writers verwendet. Siehe auch [*auswählbare Komponente*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**Komponentensatz**
</dt> <dd>

Eine Gruppe von Komponenten mit mindestens einer auswählbaren Komponente (für Sicherung oder Wiederherstellung) und einer Reihe von nicht auswählbaren Komponenten, die in einer Hierarchie nach ihren logischen Pfaden organisiert sind. Die implizite Teilnahme an einem Sicherungs- oder Wiederherstellungsvorgang hängt von der expliziten Einbeziehung der auswählbaren Komponente der obersten Ebene ab. Nur die Komponenteninformationen dieser auswählbaren Komponente sind im Dokument Sicherungskomponenten enthalten. Ein Komponentensatz kann auswählbare und nicht auswählbare Unterkomponenten enthalten. Siehe auch [*logischer Pfad*](vssgloss-l.md), [*auswählbare Komponente*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**Kopie bei Schreibschattenkopie**
</dt> <dd>

Eine Schattenkopie, die erstellt wird, indem nur die Unterschiede zum ursprünglichen Volume gespeichert werden.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**Absturzkons konsistenter Zustand**
</dt> <dd>

Der Status von Datenträgern, der dem entspricht, was nach einem schwerwiegenden Fehler gefunden wird, der das System plötzlich herunterfährt. Eine Wiederherstellung aus einem solchen Schattenkopiesatz wäre gleichbedeutend mit einem Neustart nach einem plötzlichen Herunterfahren. Dies ist der Standardzustand von Daten, die ohne Unterstützung von Writern kopiert wurden.

</dd> </dl>

 

 



