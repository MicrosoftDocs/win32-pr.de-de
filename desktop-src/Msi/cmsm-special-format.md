---
description: Bestimmte Werte, die mit konfigurierbaren Mergemodulen verwendet werden, erfordern spezielle Textverarbeitung.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Spezielles cmsm-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215364"
---
# <a name="cmsm-special-format"></a>Spezielles cmsm-Format

Bestimmte Werte, die mit konfigurierbaren Mergemodulen verwendet werden, erfordern spezielle Textverarbeitung. Eine Text Zeichenfolge, die als "cmsm Special Format" bezeichnet wird, behandelt das Semikolon (;) und sind (=) Zeichen als reservierte Zeichen, die vom clientmerge-Tool oder Mergemod.dll verwendet werden.

Das spezielle cmsm-Format wird derzeit an den folgenden Speicherorten verwendet:

-   Die Zeilen Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md).
-   Die Wert Spalte der [ModuleSubstitution-Tabelle](modulesubstitution-table.md).
-   Die ContextData-Spalte der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) , wenn Bitfield der Wert in der Format-Spalte ist.
-   Die ContextData-Spalte der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) , wenn Text der Wert in der Format-Spalte und Enum der Wert in der Type-Spalte ist.
-   Die DefaultValue-Spalte der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) , wenn key der Wert in der Format-Spalte ist.
-   Konfigurierbare Elemente im Schlüsselformat, das von der [**providetextdata-Methode**](configuremodule-providetextdata.md)verwendet wird.

Um Literale Semikolons oder Gleichheitszeichen in einen Wert im cmsm-Sonderformat einzugeben, stellen Sie dem Zeichen einen umgekehrten Schrägstrich (" \\ ") voran. Ein literaler umgekehrter Schrägstrich kann durch zwei umgekehrte Schrägstriche dargestellt werden. Ein einzelnes Zeichen, dem ein einzelner umgekehrter Schrägstrich vorangestellt ist, wird in das einzelne Zeichen übersetzt, auch wenn das Zeichen nicht als Escapezeichen erforderlich ist.

Wenn ein Semikolon oder ein Gleichheitszeichen nicht durch einen umgekehrten Schrägstrich vorangestellt ist, aber nicht über ein definiertes Verhalten im Kontext des Werts verfügt, ist die resultierende Zeichenfolge nicht definiert. Beispielsweise befindet sich die DefaultValue-Spalte der ModuleConfiguration-Tabelle im cmsm-Sonderformat für alle Schlüsselelemente, da das Semikolon das Spalten Trennzeichen ist. Obwohl das Gleichheitszeichen in dieser Zeichenfolge keine besondere Bedeutung hat, müssen Literale gleich Zeichen in dieser Zeichenfolge weiterhin mit Escapezeichen versehen werden.

 

 



