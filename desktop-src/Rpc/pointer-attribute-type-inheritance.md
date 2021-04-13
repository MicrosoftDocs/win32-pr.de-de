---
title: Vererbung von Pointer-Attribute Typen
description: Gemäß der DCE-Spezifikation muss jede IDL-Dateiattribute für Ihre Zeiger definieren.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390833"
---
# <a name="pointer-attribute-type-inheritance"></a>Vererbung von Pointer-Attribute Typen

Gemäß der DCE-Spezifikation muss jede IDL-Dateiattribute für Ihre Zeiger definieren. Wenn ein explizites Attribut keinem Zeiger zugewiesen ist, verwendet der Zeiger den Wert, der vom \[ [Zeiger \_ default](/windows/desktop/Midl/pointer-default) - \] Schlüsselwort angegeben wird. Einige DCE-Implementierungen lassen keine nicht attributierten Zeiger zu. Wenn ein Zeiger kein explizites Attribut hat, muss die IDL-Datei eine **\[ Zeiger \_ Standard \]** Spezifikation aufweisen, damit das Zeiger Attribut festgelegt werden kann.

Im Standardmodus (Microsoft-Extensions) können Sie das-Attribut eines Zeigers in der IDL-Datei angeben, die die definierende IDL-Datei importiert. In einer IDL-Datei definierte Zeiger können Attribute erben, die in anderen IDL-Dateien angegeben sind. Außerdem können IDL-Dateien im Standardmodus nicht attributierte Zeiger enthalten. Wenn weder die Basis-noch die importierten IDL-Dateien ein Zeiger Attribut oder einen Zeiger auf den **\[ \_ Standard \]** Wert angeben, werden nicht attributierte Zeiger als eindeutige Zeiger interpretiert.

Der mittlerer l-Compiler weist Zeiger Attribute mithilfe der folgenden Prioritätsregeln (1 ist am höchsten) Zeiger Attributen zu.



| Priorität | Beschreibung                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | Explizite Zeiger Attribute werden auf den Zeiger an der Definition oder der Verwendungs Website angewendet.                                      |
| 2        | Der Standardwert ist das **\[ Zeiger- \_ Standard \]** Attribut in der IDL-Datei, die den Typ definiert.                               |
| 3        | Der Standardwert ist das **\[ Zeiger- \_ Standard \]** Attribut in der IDL-Datei, die den Typ importiert.                               |
| 4        | Der Standardwert ist \[ [ptr](/windows/desktop/Midl/ptr) \] im DCE-Kompatibilitätsmodus oder \[ [](/windows/desktop/Midl/unique) \] im Microsoft-Erweiterungs Modus eindeutig. |



 

 

 