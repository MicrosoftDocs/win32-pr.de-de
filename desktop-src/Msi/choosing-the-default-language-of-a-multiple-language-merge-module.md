---
description: Die Standardsprache für ein Mergemodul ist die Sprache, die in der Tabelle ModuleSignature des Moduls aufgeführt ist, bevor Sprachtransformationen angewendet werden. Dies ist auch die erste Sprache, die in der Vorlagenzusammenfassungseigenschaft aufgeführt ist.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Auswählen der Standardsprache eines Mergemoduls mit mehreren Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c174a3917538b1562626819f8ba2bf07864c9169c27e717a078cca8d64992ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145656"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Auswählen der Standardsprache eines Mergemoduls mit mehreren Sprachen

Die Standardsprache für ein Mergemodul ist die Sprache, die in der [Tabelle ModuleSignature](modulesignature-table.md) des Moduls aufgeführt ist, bevor Sprachtransformationen angewendet werden. Dies ist auch die erste Sprache, die in der [**Vorlagenzusammenfassungseigenschaft**](template-summary.md) aufgeführt ist.

Die Standardsprache für das Modul sollte eine der spezifischsten Sprachen sein, die Sie unterstützen, da die Standardsprache immer zuerst überprüft wird. Wenn sie die angeforderte Sprache erfüllt, wird sie auch dann verwendet, wenn eine andere Sprache besser übereinstimmt. Wenn ein Modul beispielsweise 1033 und 0 unterstützt, sollte 1033 die Standardsprache sein. Wenn 0 die Standardsprache wäre, würde sie immer jede Anforderung erfüllen, und die 1033-Transformation würde nie verwendet werden, auch wenn 1033 die genaue angeforderte Sprache ist.

 

 



