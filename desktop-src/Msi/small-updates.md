---
description: Bei einem kleinen Update werden Änderungen an mindestens einer Anwendungsdateien vorgenommen, die zu klein sind, um eine Änderung des Produktcodes zu rechtfertigen.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Kleine Updates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 392e19507ca37cf865fab44485b93346dd1ad6cf6d81ada212acb2ec11ddb1c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628170"
---
# <a name="small-updates"></a>Kleine Updates

Bei einem kleinen Update werden Änderungen an mindestens einer Anwendungsdateien vorgenommen, die zu klein sind, um eine Änderung des Produktcodes zu rechtfertigen. Ein kleines Update wird häufig auch als Quick Fix Engineering -Update (QFE) bezeichnet. Ein kleines Update lässt keine Neustrukturierung der Funktionskomponentenstruktur zu.

Ein typisches kleines Update ändert nur eine oder zwei Dateien oder einen Registrierungsschlüssel. Da ein kleines Update die Informationen in der .msi ändert, muss der Installationspaketcode geändert werden. Der Paketcode wird in der [**Eigenschaft Zusammenfassung der Revisionsnummer**](revision-number-summary.md) des [Zusammenfassungsinformationsstreams gespeichert.](summary-information-stream.md)

Der Produktcode wird nie mit einem kleinen Update geändert, sodass alle änderungen, die durch ein kleines Update eingeführt werden, mit den unter Ändern des Produktcodes [beschriebenen Richtlinien übereinstimmen müssen.](changing-the-product-code.md) Für ein Update ist ein [größeres Upgrade erforderlich,](major-upgrades.md) um den [**ProductCode zu ändern.**](productcode.md) Wenn es erforderlich ist, zwischen Produkten zu unterscheiden, ohne den Produktcode zu ändern, verwenden Sie ein [kleineres Upgrade.](minor-upgrades.md)

Informationen zum Anwenden eines kleinen Updatepatchpakets auf ein Windows Installer-Paket finden Sie unter Creating [a Small Update Patch](creating-a-small-update-patch.md), Applying Small Updates by Patching the Local Installation of the [Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md), Applying Small Updates [by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md), and Applying Small Updates by [Patching an Administrative Image](applying-small-updates-by-patching-an-administrative-image.md).

 

 



