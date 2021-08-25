---
description: Die Tabelle Complus enthält Informationen, die zum Installieren von COM+-Anwendungen erforderlich sind.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Complus-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77885688226689e5d81e074b1a9a28ef3801aaeba5febf51165377ac9ad9e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144971"
---
# <a name="complus-table"></a>Complus-Tabelle

Die Tabelle Complus enthält Informationen, die zum Installieren von COM+-Anwendungen erforderlich sind.

Die Complus-Tabelle enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Komponente\_ | [Identifier](identifier.md) | J   | N        |
| ExpType     | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Ein externer Schlüssel in der ersten Spalte der [Component-Tabelle.](component-table.md) Dies ist die Komponente, die die COM+-Anwendung enthält.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Exportflags, die während der Generierung der .msi werden. Weitere Informationen finden Sie in der COM+-Dokumentation im Microsoft Windows Software Development Kit (SDK).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen finden [Sie unter der Aktion RegisterComPlus](registercomplus-action.md) und der Aktion [UnregisterComPlus.](unregistercomplus-action.md)

Weitere [Informationen finden Sie unter Installieren einer COM+-Anwendung mit dem Windows Installer.](installing-a-com--application-with-the-windows-installer.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



