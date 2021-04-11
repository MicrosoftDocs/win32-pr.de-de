---
description: Ein kleines Update nimmt Änderungen an einer oder mehreren Anwendungs Dateien vor, die zu gering sind, um das Ändern des Produktcodes zu rechtfertigen.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Kleine Updates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128372"
---
# <a name="small-updates"></a>Kleine Updates

Ein kleines Update nimmt Änderungen an einer oder mehreren Anwendungs Dateien vor, die zu gering sind, um das Ändern des Produktcodes zu rechtfertigen. Ein kleines Update wird häufig auch als QFE-Update (Quick Fix Engineering) bezeichnet. Bei einem kleinen Update ist die Neuorganisation der Funktionskomponenten Struktur nicht zulässig.

Bei einem typischen kleinen Update werden nur eine oder zwei Dateien oder ein Registrierungsschlüssel geändert. Da ein kleines Update die Informationen in der MSI-Datei ändert, muss der Installationspaket Code geändert werden. Der Paketcode wird in der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " des [Zusammenfassungs Informationsdaten Stroms](summary-information-stream.md)gespeichert.

Der Produktcode wird nie mit einem kleinen Update geändert, sodass alle Änderungen, die durch ein kleines Update eingeführt wurden, mit den in [Ändern des Produktcodes](changing-the-product-code.md)beschriebenen Richtlinien übereinstimmen müssen. Ein Update erfordert ein [großes Upgrade](major-upgrades.md) , um [**ProductCode**](productcode.md)zu ändern. Wenn es erforderlich ist, zwischen Produkten zu unterscheiden, ohne den Produktcode zu ändern, verwenden Sie ein [kleineres Upgrade](minor-upgrades.md).

Informationen zum Anwenden eines kleinen Update-Patch-Pakets auf ein Windows Installer Paket finden Sie unter [Erstellen eines kleinen Update Patches](creating-a-small-update-patch.md), [anwenden kleiner Updates durch Patchen der lokalen Installation des Produkts](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [anwenden kleiner Updates durch erneutes Installieren des Produkts](applying-small-updates-by-reinstalling-the-product.md)und [anwenden kleiner Updates durch Patchen eines administrativen Abbilds](applying-small-updates-by-patching-an-administrative-image.md).

 

 



