---
description: In der Tabelle PublishComponent werden die in der Component-Tabelle aufgeführten Komponenten mit einer qualifizierertextzeichenfolge und einer Kategorie-ID-GUID verknüpft.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: PublishComponent-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349198"
---
# <a name="publishcomponent-table"></a>PublishComponent-Tabelle

In der Tabelle PublishComponent werden die in der [Component-Tabelle](component-table.md) aufgeführten Komponenten mit einer qualifizierertextzeichenfolge und einer Kategorie-ID-GUID verknüpft. Komponenten mit paralleler Funktionalität, die auf diese Weise gruppiert wurden, werden als qualifizierte Komponenten bezeichnet. Siehe [qualifizierte Komponenten](qualified-components.md). Dadurch erhält das Installationsprogramm eine Methode für eine Dereferenzierung auf einer einzelnen Ebene, wenn auf Komponenten verwiesen wird. Siehe [verwenden qualifizierter Komponenten](using-qualified-components.md).

Die PublishComponent-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| ComponentID | [GUID](guid.md)             | J   | N        |
| Qualifizierer   | [Text](text.md)             | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md) | J   | N        |
| AppData     | [Text](text.md)             | N   | J        |
| Funktion\_   | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentID
</dt> <dd>

Eine Zeichen folgen- [GUID](guid.md) , die die Kategorie der Komponenten darstellt, die gruppiert werden. Beachten Sie, dass der Titel dieser Spalte irreführend ist. Dies ist die GUID für die Kategorie qualifizierter Komponenten und ist nicht dieselbe GUID, die in der ComponentID-Spalte der [Component-Tabelle](component-table.md)angezeigt wird. Hier bezieht es sich auf einen Server, der die Funktionalität einer Komponente für externe Clients anstelle der Komponente selbst bereitstellt.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Turnier
</dt> <dd>

Eine Text Zeichenfolge, die den Wert in der ComponentID-Spalte qualifiziert. Ein Qualifizierer wird verwendet, um mehrere Formen derselben Komponente, z. b. eine Komponente, die in mehreren Sprachen implementiert ist, zu unterscheiden. Dabei handelt es sich um die von [**msienbicomponentqualifier**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)zurückgegebenen qualifizierertextzeichenfolgen.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in Spalte 1 der [Komponenten Tabelle](component-table.md). Dieser Bezeichner verweist auf den Daten Satz der qualifizierten Komponente in der Component-Tabelle.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>APPDATA
</dt> <dd>

Ein optionaler Lokalisier barer Text, der die qualifizierte Komponente dieses Datensatzes beschreibt. Die Zeichenfolge wird häufig von der Anwendung analysiert und kann dem Benutzer angezeigt werden. Die qualifizierte Komponente sollte beschrieben werden. Dies kann mit [**msienumschlag componentqualifizierern**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)abgerufen werden.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_
</dt> <dd>

Externer Schlüssel in Spalte 1 der [Featuretabelle](feature-table.md). Dies ist das Feature, das diese qualifizierte Komponente verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Auf diese Tabelle wird verwiesen, wenn die [PublishComponents-Aktion](publishcomponents-action.md) oder die [unpublishcomponents-Aktion](unpublishcomponents-action.md) ausgeführt wird.

Beachten Sie, dass der Name dieser Tabelle irreführend ist. Diese Tabelle ist nicht erforderlich, um Ankündigungen zu erstellen. Informationen dazu, wie Sie den Installationsstatus von Komponenten für die Ankündigung festlegen, finden Sie in der Spalte Attribute der [Komponenten Tabelle](component-table.md) und [Funktions Tabelle](feature-table.md) .

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



