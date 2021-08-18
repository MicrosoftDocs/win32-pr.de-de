---
title: Pointer-Attribute Typvererbung
description: Gemäß der DCE-Spezifikation muss jede IDL-Datei Attribute für ihre Zeiger definieren.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf0b365cecf2880fa2746536c3f1d80505f5d7534b95017f8abb18ceecd9d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019260"
---
# <a name="pointer-attribute-type-inheritance"></a>Pointer-Attribute Typvererbung

Gemäß der DCE-Spezifikation muss jede IDL-Datei Attribute für ihre Zeiger definieren. Wenn einem Zeiger kein explizites Attribut zugewiesen ist, verwendet der Zeiger den Wert, der durch das \[ [Zeiger-Standardschlüsselwort \_ angegeben](/windows/desktop/Midl/pointer-default) \] wird. Einige DCE-Implementierungen lassen keine nicht attributierten Zeiger zu. Wenn ein Zeiger nicht über ein explizites Attribut verfügt, muss die IDL-Datei **\[ \_ \]** über eine Zeiger-Standardspezifikation verfügen, damit das Zeigerattribut festgelegt werden kann.

Im Standardmodus (Microsoft-extensions) können Sie das Attribut eines Zeigers in der IDL-Datei angeben, die die definierende IDL-Datei importiert. Zeiger, die in einer IDL-Datei definiert sind, können Attribute erben, die in anderen IDL-Dateien angegeben sind. Außerdem können IDL-Dateien im Standardmodus nicht attributierte Zeiger enthalten. Wenn weder die Basis- noch die importierten IDL-Dateien ein Zeigerattribut **\[ \_ \]** oder einen Zeiger standard angeben, werden nicht attributierte Zeiger als eindeutige Zeiger interpretiert.

Der MIDL-Compiler weist Zeigerattributen zeigern mithilfe der folgenden Prioritätsregeln zu (1 ist die höchste).



| Priorität | Beschreibung                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | Explizite Zeigerattribute werden auf den Zeiger an der Definition oder der Verwendungswebsite angewendet.                                      |
| 2        | Der Standardwert ist das **\[ \_ \] Zeiger-Standardattribut** in der IDL-Datei, das den Typ definiert.                               |
| 3        | Der Standardwert ist das **\[ \_ \] Zeiger-Standardattribut** in der IDL-Datei, das den Typ importiert.                               |
| 4        | Der Standardwert ist \[ [ptr im](/windows/desktop/Midl/ptr) \] DCE-Kompatibilitätsmodus oder \[ [eindeutig im](/windows/desktop/Midl/unique) \] Microsoft-Erweiterungsmodus. |



 

 

 