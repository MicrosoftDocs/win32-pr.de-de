---
description: Die Tabelle FeatureComponents definiert die Beziehung zwischen Features und Komponenten. Für jedes Feature werden in dieser Tabelle alle Komponenten aufgeführt, aus denen dieses Feature zusammenhing.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: FeatureComponents-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7635a43784ee7e8fbb71c7161bb07d39ffe5238177ea2a7cdaabdeb18dc41e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430870"
---
# <a name="featurecomponents-table"></a>FeatureComponents-Tabelle

Die Tabelle FeatureComponents definiert die Beziehung zwischen Features und Komponenten. Für jedes Feature werden in dieser Tabelle alle Komponenten aufgeführt, aus denen dieses Feature zusammenhing.

Die Tabelle FeatureComponents enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Komponente\_   | [Identifier](identifier.md) | J   | N        |
| Komponente\_ | [Identifier](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_
</dt> <dd>

Ein externer Schlüssel in der ersten Spalte der [Featuretabelle](feature-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Ein externer Schlüssel in der ersten Spalte der [Component-Tabelle.](component-table.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Pro Feature gilt ein Maximalwert von 1.600 Komponenten.

Komponenten können von zwei oder mehr Features gemeinsam genutzt werden, d. &a. auf dieselbe Komponente kann von mehr als einem Feature verwiesen werden.

Auf diese Tabelle wird verwiesen, wenn die [PublishFeatures-Aktion](publishfeatures-action.md) oder die [UnpublishFeatures-Aktion](unpublishfeatures-action.md) ausgeführt wird.

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

 

 



