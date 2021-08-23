---
title: Namespace
description: Ein Namespace ist ein Kontext, in dem die Namen aller Objekte eindeutig auflösbar sein müssen.
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce9119b49cde888cb51f65e6e6b677fb364d640e1b78fe48c739b7c1206936d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692200"
---
# <a name="namespace"></a>Namespace

Ein Namespace ist ein Kontext, in dem die Namen aller Objekte eindeutig auflösbar sein müssen. Beispielsweise ist das Internet ein einzelner DNS-Namensraum, in dem alle Netzwerkgeräte mit einem DNS-Namen in eine bestimmte Adresse aufgelöst werden können (z. B. wird in `www.microsoft.com` 207.46.131.13 aufgelöst).

## <a name="flat-namespace"></a>Flacher Namespace

Ein Namespace kann flach oder hierarchisch sein. Ein flacher Namespace lässt sich nicht gut skalieren, da er nur so groß werden kann, bevor alle verfügbaren Namen verwendet werden. Sobald ein Name in einem Namespace mehr als einmal verwendet wird, verstößt der Namespace gegen die eindeutig auflösbare Anforderung.

## <a name="hierarchical-namespace"></a>Hierarchischer Namespace

Ein hierarchischer Namespace ist in verschiedene Bereiche unterteilt, die als Unternamespaces bezeichnet werden können. Jeder Bereich ist ein eigener Unternamespace innerhalb des gesamten Namespace. Daher muss jedes Objekt nur innerhalb seines Unternamespace einen eindeutigen Namen haben, um einen eindeutig auflösbaren Namen innerhalb der Namespacehierarchie zu haben. Hierarchische Namespaces können dann auf extrem große Netzwerke skaliert werden, wenn Sie dem gesamten Namensraum weitere Objekte hinzufügen. Sie müssen eindeutige Namen für sie nur innerhalb des Unternamespace finden, zu dem sie &mdash; gehören.

Alle DNS-Namespaces sind hierarchisch. Die Unternamespaces im hierarchischen DNS-Namespace werden als Domänen *bezeichnet.* Der eindeutige Name eines Computers innerhalb einer Domäne wird als *relativer Distinguished Name bezeichnet.* Computer mit dem gleichen relativen Distinguished Name können in verschiedenen Unternamespaces (Domänen) der Namespacehierarchie vorhanden sein, da sie mithilfe eines vollqualifizierten Domänennamens (FQDN) vollständig in ein eindeutiges Objekt innerhalb der gesamten DNS-Hierarchie aufgelöst werden können. Beispielsweise könnten Sie einen Server mit dem Namen *server1* in der *widgets.microsoft.com-Domäne* (widgets.microsoft.com-Namespace) und *server1* im gadgets.widgets.microsoft.com *haben.*  Da sie sich in unterschiedlichen Unternamespaces im hierarchischen Namespace befinden, können sie in verschiedene FQDNs server1.widgets.microsoft.com &mdash;  und server1.gadgets.widgets.microsoft.com. 
