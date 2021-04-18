---
description: Uniscriverwendet mehrere Strukturierungs Module, die das layoutwissen für bestimmte Skripts enthalten.
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: Verwenden von Strukturierungs Modulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a106e993aba515af38edd2b809ef60454a186cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354849"
---
# <a name="using-shaping-engines"></a>Verwenden von Strukturierungs Modulen

Uniscriverwendet mehrere Strukturierungs Module, die das layoutwissen für bestimmte Skripts enthalten. Außerdem nutzt Sie die OpenType-layoutstrukturierungs-Engine für die Behandlung Schriftart spezifischer Skript Features, wie z. b. die Generierung von Symbolen, die Bereichs Messung und die Unterstützung für Wörter Trennung. Unischreiber verwaltet die Neuanordnen von bidirektionalen Zeichen mithilfe des bidirektionalen Unicode-Algorithmus und versteht nicht-OpenType-Layout-Schriftarten Formate für arabische, hebräische und thailändische Formen.

Da die genauen Code Punkt Bereiche, die den einzelnen Strukturierungs Modulen zugewiesen sind, variieren können, werden Skript Nummern nicht veröffentlicht, mit der Ausnahme, dass Skripts nicht \_ definiert sind. Die Anwendung kann jedoch die Attribute von Skripts testen, indem Sie die [**scriptgetproperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) -Funktion aufruft, die auf die Tabelle der globalen Skript Eigenschaften zugreift. Die Anwendung kann die globalen Skript Eigenschaften verwenden, um Ihre eigenen Layoutregeln mit den erforderlichen Strukturierungs-Engine-Abteilungen zu kombinieren.

Die Anwendung greift auf eine Strukturierungs-Engine zu, indem Sie die [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) -Funktion aufruft. Alle komplexen Skript Strukturierungs Module, die Ziffern Strukturierungs Module und die ASCII-Strukturierungs Module überprüfen die Schriftart, die im Gerätekontext handle vor der Strukturierung angezeigt wird. Komplexe Skripts müssen mithilfe des Skripts geformt werden, das von der [**scriptitemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) -Funktion zurückgegeben wird, um lesbar zu sein. Andere Ausführungen bleiben lesbar, wenn Sie mit einem Skript formatiert \_ sind, das im **Escript** -Member der [**Skript \_ Analyse**](/windows/win32/api/usp10/ns-usp10-script_analysis) Struktur angegeben ist, obwohl Sie möglicherweise die typografische Qualität verlieren.

[**Scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) gibt 0 (null) zurück, wenn erfolgreich, oder USP \_ E \_ Script \_ Not \_ in \_ Font, wenn die von der Anwendung bereitgestellte Schriftart nicht genügend Symbole oder Tabellen enthält. Wenn die Anwendung Skript \_ definiert angibt und einige Zeichen von der Schriftart nicht unterstützt werden, ist die Funktion dennoch erfolgreich. In diesem Fall sollte die Anwendung den Ausgabepuffer des Symbols auf fehlende Symbole durchsuchen. Strategien für den Umgang mit fehlenden Symbolen finden Sie unter [Verwenden von Schriftart fallback](using-font-fallback.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 



