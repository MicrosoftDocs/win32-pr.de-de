---
description: Verwenden Sie zum Veröffentlichen eines Produkts, einer Komponente oder eines Features eine der Veröffentlichungs Aktionen.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Veröffentlichen von Produkten, Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdd8c8445491646399c7d118a69ae497d27faff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215905"
---
# <a name="publishing-products-features-and-components"></a>Veröffentlichen von Produkten, Features und Komponenten

Verwenden Sie zum [veröffentlichen](components-and-features.md) eines Produkts, einer Komponente oder eines Features eine der Veröffentlichungs Aktionen. Die [publishproduct-Aktion](publishproduct-action.md) registriert die Produktinformationen beim System. Nachdem Sie die publishproduct-Aktion ausgeführt haben, veröffentlichen Sie die Komponenten mit der [PublishComponents-Aktion](publishcomponents-action.md), die wiederum die [PublishComponent-Tabelle](publishcomponent-table.md) verwendet, um die Komponenten zu ermitteln, die als angekündigt festgelegt sind. Zum Veröffentlichen auf featurebasis rufen Sie die [publishfeatures-Aktion](publishfeatures-action.md)auf. Bei dieser Aktion wird die [FeatureComponents-Tabelle](featurecomponents-table.md) als Daten verwendet, um aufzulösen, welche Features angekündigt werden.

Es gibt auch zwei Aktionen, die die Veröffentlichung eines Features oder einer Komponente aufheben: die [unpublishcomponents-Aktion](unpublishcomponents-action.md) und die [unpublishfeatures-Aktion](unpublishfeatures-action.md).

 

 



