---
description: Die Erweiterungs Tabelle enthält Informationen zu Dateinamen Erweiterungs Servern, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungs Schlüsseln und-Werten.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Erweiterungs Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350545"
---
# <a name="extension-table"></a>Erweiterungs Tabelle

Die Erweiterungs Tabelle enthält Informationen zu Dateinamen Erweiterungs Servern, die als Teil der Produktankündigung generiert werden müssen. Jede Zeile generiert einen Satz von Registrierungs Schlüsseln und-Werten.

Die Erweiterungs Tabelle enthält die Spalten, die in der folgenden Tabelle aufgeführt sind.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Durchwahl   | [Text](text.md)             | J   | N        |
| Komponente\_ | [Bezeichner](identifier.md) | J   | N        |
| ProgID\_    | [Text](text.md)             | N   | J        |
| Medi\_      | [Text](text.md)             | N   | J        |
| Funktion\_   | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Weiterung
</dt> <dd>

Die der Tabellenzeile zugeordnete Erweiterung. Die Erweiterung kann bis zu 255 Zeichen lang sein. Geben Sie die Erweiterung in diesem Feld ohne den vorangehenden Zeitraum ein.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Ein externer Schlüssel für die erste Spalte der [Komponenten](component-table.md) Tabelle. Diese Spalte verweist auf die Komponente, mit der die Installation der Erweiterung gesteuert wird.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgID\_
</dt> <dd>

Die Programm-ID, die dieser Erweiterung zugeordnet ist. Dabei handelt es sich um einen Fremdschlüssel in der [ProgID](progid-table.md) -Tabelle.

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>Medi\_
</dt> <dd>

Der Inhaltstyp, der für die Erweiterungs Spalte geschrieben werden soll.

Ein externer Schlüssel für die erste Spalte der [MIME](mime-table.md) -Tabelle.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Befinden\_
</dt> <dd>

Ein externer Schlüssel in der ersten [Spalte der Featuretabelle,](feature-table.md) der das Feature angibt, das den Erweiterungs Server bereitstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Auf die Erweiterungs Tabelle wird verwiesen, wenn die [RegisterExtensionInfo](registerextensioninfo-action.md) -Aktion oder die [unregisterextensioninfo](unregisterextensioninfo-action.md) -Aktion ausgeführt wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE69](ice69.md)  
</dl>

 

 



