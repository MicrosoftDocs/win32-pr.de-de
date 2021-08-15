---
description: Die PublishComponent-Tabelle ordnet komponenten, die in der Tabelle Komponente aufgeführt sind, einer Qualifizierertextzeichenfolge und einer Kategorie-ID-GUID zu.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: PublishComponent-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0abd7567e8327aa36a120fd5a13115cb191e1660566e9d480446295dca53cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376383"
---
# <a name="publishcomponent-table"></a>PublishComponent-Tabelle

Die PublishComponent-Tabelle ordnet komponenten, die in der [Tabelle Komponente](component-table.md) aufgeführt sind, einer Qualifizierertextzeichenfolge und einer Kategorie-ID-GUID zu. Komponenten mit paralleler Funktionalität, die auf diese Weise gruppiert wurden, werden als qualifizierte Komponenten bezeichnet. Weitere Informationen finden Sie unter [Qualifizierte Komponenten.](qualified-components.md) Dadurch wird dem Installationsprogramm beim Verweisen auf Komponenten eine Methode für die Dekonstruktion auf einer einzelnen Ebene zur Verfügung stellen. Weitere Informationen finden Sie [unter Verwenden von qualifizierten Komponenten.](using-qualified-components.md)

Die PublishComponent-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Componentid | [GUID](guid.md)             | J   | N        |
| Qualifizierer   | [Text](text.md)             | J   | N        |
| Komponente\_ | [Identifier](identifier.md) | J   | N        |
| AppData     | [Text](text.md)             | N   | J        |
| Komponente\_   | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

Eine [Zeichenfolgen-GUID,](guid.md) die die Kategorie der zu gruppierenden Komponenten darstellt. Beachten Sie, dass der Titel dieser Spalte irreführend ist. Dies ist die GUID für die Kategorie der qualifizierten Komponenten und nicht die gleiche GUID, die in der ComponentId-Spalte der [Component-Tabelle](component-table.md)angezeigt wird. Hier bezieht er sich auf einen Server, der die Funktionalität einer Komponente für externe Clients und nicht für die Komponente selbst bereitstellt.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualifizierer
</dt> <dd>

Eine Textzeichenfolge, die den Wert in der ComponentId-Spalte qualifiziert. Ein Qualifizierer wird verwendet, um mehrere Formen derselben Komponente zu unterscheiden, z. B. eine Komponente, die in mehreren Sprachen implementiert ist. Dies sind die Qualifizierertextzeichenfolgen, die von [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)zurückgegeben werden.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in Spalte 1 der [Component-Tabelle.](component-table.md) Dieser Bezeichner bezieht sich auf den Datensatz der qualifizierten Komponente in der Tabelle Komponente.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>Appdata
</dt> <dd>

Ein optionaler lokalisierbarer Text, der die qualifizierte Komponente dieses Datensatzes beschreibt. Die Zeichenfolge wird häufig von der Anwendung analysiert und kann dem Benutzer angezeigt werden. Sie sollte die qualifizierte Komponente beschreiben. Dies kann mit [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)abgerufen werden.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_
</dt> <dd>

Externer Schlüssel in Spalte 1 der [Featuretabelle](feature-table.md). Dies ist das Feature, das diese qualifizierte Komponente verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf diese Tabelle wird verwiesen, wenn die [PublishComponents-Aktion](publishcomponents-action.md) oder die [UnpublishComponents-Aktion](unpublishcomponents-action.md) ausgeführt wird.

Beachten Sie, dass der Name dieser Tabelle irreführend ist. Diese Tabelle ist zum Erstellen von Ankündigungen nicht erforderlich. Informationen zum Festlegen des Installationszustands von Komponenten, die ankündigen sollen, finden Sie in der Spalte Attribute der [Tabelle Komponenten](component-table.md) und in der [Featuretabelle.](feature-table.md)

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



