---
description: Die FeatureComponents-Tabelle definiert die Beziehung zwischen Features und Komponenten. Für jede Funktion werden in dieser Tabelle alle Komponenten aufgelistet, aus denen diese Funktion besteht.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: FeatureComponents-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754225"
---
# <a name="featurecomponents-table"></a>FeatureComponents-Tabelle

Die FeatureComponents-Tabelle definiert die Beziehung zwischen Features und Komponenten. Für jede Funktion werden in dieser Tabelle alle Komponenten aufgelistet, aus denen diese Funktion besteht.

Die FeatureComponents-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Funktion\_   | [Bezeichner](identifier.md) | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_
</dt> <dd>

Ein externer Schlüssel in die erste Spalte der Funktions [Tabelle](feature-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Ein externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es gibt eine Obergrenze von 1600 Komponenten pro Feature.

Komponenten können von zwei oder mehr Features gemeinsam genutzt werden, d. h., auf dieselbe Komponente kann von mehreren Features verwiesen werden.

Auf diese Tabelle wird verwiesen, wenn die [publishfeatures-Aktion](publishfeatures-action.md) oder die [unpublishfeatures-Aktion](unpublishfeatures-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE21](ice21.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE47](ice47.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE69](ice69.md)  
</dl>

 

 



