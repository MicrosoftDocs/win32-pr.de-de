---
description: Die Tabelle Erweiterung enthält Informationen zu Dateinamenerweiterungsservern, die als Teil der Produktanzeige generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungsschlüsseln und -werten.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Erweiterungstabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d664df812b723d7ab6c9b966b09fac8c57a35b655e123f720fdb87bdf431146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821740"
---
# <a name="extension-table"></a>Erweiterungstabelle

Die Tabelle Erweiterung enthält Informationen zu Dateinamenerweiterungsservern, die als Teil der Produktanzeige generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungsschlüsseln und -werten.

Die Tabelle Erweiterung enthält die in der folgenden Tabelle gezeigten Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Durchwahl   | [Text](text.md)             | J   | N        |
| Komponente\_ | [Identifier](identifier.md) | J   | N        |
| Progid\_    | [Text](text.md)             | N   | J        |
| Mime\_      | [Text](text.md)             | N   | J        |
| Komponente\_   | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Erweiterung
</dt> <dd>

Die erweiterung, die der Tabellenzeile zugeordnet ist. Die Erweiterung kann bis zu 255 Zeichen lang sein. Geben Sie die Erweiterung in dieses Feld ohne vorherigen Zeitraum ein.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Component-Tabelle.](component-table.md) Diese Spalte verweist auf die Komponente, die die Installation der Erweiterung steuert.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>Progid\_
</dt> <dd>

Die dieser Erweiterung zugeordnete Programm-ID. Dies ist ein Fremdschlüssel in der [Tabelle ProgId.](progid-table.md)

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>Mime\_
</dt> <dd>

Der Inhaltstyp, der für die Spalte Erweiterung geschrieben werden soll.

Ein externer Schlüssel für die erste Spalte der [MIME-Tabelle.](mime-table.md)

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_
</dt> <dd>

Ein externer Schlüssel in der ersten Spalte der [Featuretabelle,](feature-table.md) der das Feature an gibt, das den Erweiterungsserver bietet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf die Extension-Tabelle wird verwiesen, wenn die [RegisterExtensionInfo-Aktion](registerextensioninfo-action.md) oder die [UnRegisterExtensionInfo-Aktion](unregisterextensioninfo-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE69](ice69.md)  
</dl>

 

 



