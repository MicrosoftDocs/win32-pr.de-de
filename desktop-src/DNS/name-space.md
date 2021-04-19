---
title: Namespace
description: Ein Namespace ist ein Kontext, in dem die Namen aller Objekte eindeutig aufgelöst werden müssen.
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb79ba44bfaab1ea50dd89961503176dc8fbd1a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106355153"
---
# <a name="namespace"></a>Namespace

Ein Namespace ist ein Kontext, in dem die Namen aller Objekte eindeutig aufgelöst werden müssen. Das Internet ist beispielsweise ein einzelner DNS-Namespace, in dem alle Netzwerkgeräte mit einem DNS-Namen in eine bestimmte Adresse aufgelöst werden können (z `www.microsoft.com` . b. wird in 207.46.131.13 aufgelöst).

## <a name="flat-namespace"></a>Flacher Namespace

Ein Namespace kann flach oder hierarchisch sein. Ein flacher Namespace skaliert nicht gut, da er nur so groß werden kann, bis alle verfügbaren Namen aufgebraucht sind. Sobald ein Name mehrmals in einem Namespace verwendet wird, verstößt der Namespace gegen die eindeutig auflösbare Anforderung.

## <a name="hierarchical-namespace"></a>Hierarchischer Namespace

Ein hierarchischer Namespace ist in verschiedene Bereiche unterteilt, die als untergeordnete Namespaces betrachtet werden können. Jeder Bereich ist ein eigener untergeordneter Namespace innerhalb des gesamten Namespace. Daher muss jedes Objekt einen eindeutigen Namen nur innerhalb seines untergeordneten Namespace aufweisen, um einen eindeutig auflösbaren Namen innerhalb der Namespace Hierarchie zu erhalten. Hierarchische Namespaces können dann auf extrem große Netzwerke &mdash; skaliert werden, wenn Sie dem gesamten Namespace weitere Objekte hinzufügen. Sie müssen nur innerhalb des untergeordneten Namespace, zu dem Sie gehören, eindeutige Namen finden.

Alle DNS-Namespaces sind hierarchisch. Die Subnamespaces im hierarchischen DNS-Namespace werden als *Domänen* bezeichnet. Der eindeutige Name eines Computers in einer Domäne wird als *relativer Distinguished Name* bezeichnet. Computer mit demselben relativen Distinguished Name können in unterschiedlichen Subnamespaces (Domänen) der Namespace Hierarchie vorhanden sein, da Sie mithilfe eines voll qualifizierten Domänen Namens (FQDN) vollständig in ein eindeutiges Objekt innerhalb der gesamten DNS-Hierarchie aufgelöst werden können. Beispielsweise können Sie einen Server mit dem Namen *Server1* in der *widgets.Microsoft.com* -Domäne (den *widgets.Microsoft.com* -Namespace) haben, und Sie können *Server1* im *Gadgets.widgets.Microsoft.com* -Namespace haben. Da Sie sich in verschiedenen Subnamespaces im hierarchischen Namespace befinden, können Sie in verschiedene FQDNs &mdash; -*Server1.widgets.Microsoft.com* und *Server1.Gadgets.widgets.Microsoft.com* aufgelöst werden.
