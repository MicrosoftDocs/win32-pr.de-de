---
description: Bestimmte Werte, die mit konfigurierbaren Mergemodulen verwendet werden, erfordern eine besondere Textbehandlung.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: CMSM-Sonderformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8521c422d62980da0d222f8a8fc8395afa40b68bfd65c5600298372b1035f97d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252140"
---
# <a name="cmsm-special-format"></a>CMSM-Sonderformat

Bestimmte Werte, die mit konfigurierbaren Mergemodulen verwendet werden, erfordern eine besondere Textbehandlung. Eine Textzeichenfolge, die als "CMSM Special Format" (CMSM-Sonderformat) beschrieben wird, behandelt das Semikolon (;) und entspricht (=) Zeichen als reservierte Zeichen, die vom Clientzusammenführungstool oder -Mergemod.dll.

Das CMSM-Sonderformat wird derzeit an den folgenden Stellen verwendet:

-   Die Row-Spalte der [ModuleSubstitution-Tabelle.](modulesubstitution-table.md)
-   Die Value -Spalte der [ModuleSubs standardwerten -Tabelle.](modulesubstitution-table.md)
-   Die ContextData-Spalte der [ModuleConfiguration-Tabelle,](moduleconfiguration-table.md) wenn Bitfield der Wert in der Spalte Format ist.
-   Die ContextData-Spalte der [ModuleConfiguration-Tabelle,](moduleconfiguration-table.md) wenn Text der Wert in der Spalte Format und Enum der Wert in der Spalte Type ist.
-   Die DefaultValue-Spalte der [ModuleConfiguration-Tabelle,](moduleconfiguration-table.md) wenn Key der Wert in der Spalte Format ist.
-   Konfigurierbare Elemente im Schlüsselformat, das von der [**ProvideTextData-Methode verwendet wird.**](configuremodule-providetextdata.md)

Um literale Semikolons oder gleichheitsgleiche Zeichen in einen Wert im CMSM-Sonderformat ein zu geben, stellen Sie dem Zeichen einen zurückgestellten Schrägstrich (' \\ ') voran. Ein literaler schräger Schrägstrich kann durch zwei schräge Schrägstriche dargestellt werden. Ein einzelnes Zeichen, dem ein einzelner schräger Schrägstrich vorangestellt ist, wird in das einzelne Zeichen übersetzt, auch wenn kein Vorzeichen erforderlich ist.

Wenn ein Semikolon oder gleichheitsgleiches Zeichen nicht durch einen zurückgestellten Schrägstrich vorangestellt ist, aber kein definiertes Verhalten im Kontext des Werts auft, ist die resultierende Zeichenfolge nicht definiert. Die DefaultValue-Spalte der ModuleConfiguration-Tabelle hat z. B. das CMSM-Sonderformat für alle Schlüsselelemente, da das Semikolon als Spaltentrennzeichen verwendet wird. Obwohl das Gleichheitszeichen in dieser Zeichenfolge keine besondere Bedeutung hat, müssen literale Gleichheitszeichen in dieser Zeichenfolge weiterhin mit Escapezeichen verkettet werden.

 

 



