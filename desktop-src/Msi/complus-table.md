---
description: Die complus-Tabelle enthält Informationen, die zum Installieren von com+-Anwendungen erforderlich sind.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: ComPlus-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369045"
---
# <a name="complus-table"></a>ComPlus-Tabelle

Die complus-Tabelle enthält Informationen, die zum Installieren von com+-Anwendungen erforderlich sind.

Die complus-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Komponente\_ | [Bezeichner](identifier.md) | J   | N        |
| EXPTYPE     | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Ein externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md). Dies ist die Komponente, die die COM+-Anwendung enthält.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>EXPTYPE
</dt> <dd>

Exportiererungsflags, die während der Generierung der MSI-Datei verwendet werden. Weitere Informationen finden Sie in der com+-Dokumentation im Microsoft Windows Software Development Kit (SDK).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie in der [registercomplus-Aktion](registercomplus-action.md) und der [unregistercomplus-Aktion](unregistercomplus-action.md).

Weitere Informationen finden Sie unter [Installieren einer COM+-Anwendung mit dem Windows Installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



