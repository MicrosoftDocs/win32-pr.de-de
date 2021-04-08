---
description: Die Standardsprache für ein Mergemodul ist die Sprache, die in der Tabelle ModuleSignature des Moduls aufgeführt ist, bevor sprach Transformationen angewendet werden. Dies ist auch die erste Sprache, die in der Template-Übersichts Eigenschaft aufgeführt ist.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Auswählen der Standardsprache eines Mergemoduls mit mehreren Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864416"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Auswählen der Standardsprache eines Mergemoduls mit mehreren Sprachen

Die Standardsprache für ein Mergemodul ist die Sprache, die in der [Tabelle ModuleSignature](modulesignature-table.md) des Moduls aufgeführt ist, bevor sprach Transformationen angewendet werden. Dies ist auch die erste Sprache, die in der [**Template-Übersichts**](template-summary.md) Eigenschaft aufgeführt ist.

Die Standardsprache für das Modul sollte eine der spezifischsten Sprachen sein, die Sie unterstützen, da die Standardsprache immer zuerst geprüft wird, und wenn Sie der angeforderten Sprache entspricht, wird Sie auch dann verwendet, wenn eine andere Sprache eine bessere Übereinstimmung ist. Wenn ein Modul z. b. 1033 und 0 unterstützt, sollte 1033 die Standardsprache sein. Wenn 0 die Standardsprache wäre, würde Sie immer jede Anforderung erfüllen, und die 1033-Transformation würde nie verwendet werden, auch wenn 1033 die exakt angeforderte Sprache ist.

 

 



