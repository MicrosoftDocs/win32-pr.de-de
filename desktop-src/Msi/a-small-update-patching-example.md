---
description: In diesem Beispiel wird veranschaulicht, wie Sie ein Patchpaket erstellen, das ein kleines Update auf das beispielinstallationspaket anwendet, das in Einem Installationsbeispiel erläutert wird.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Beispiel für kleine Updatepatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0670693e9f5c6bf1c6b48c72e4b05b0f06703d69c08f46f6a2209b3d5046ea7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082970"
---
# <a name="a-small-update-patching-example"></a>Beispiel für kleine Updatepatches

In diesem Beispiel wird veranschaulicht, wie sie ein [Patchpaket](patch-packages.md) erstellen, das ein [kleines Update](small-updates.md) auf das Beispielinstallationspaket anwendet, das in [Einem Installationsbeispiel](an-installation-example.md)erläutert wird. Ein kleines Update nimmt Änderungen an einer oder mehreren Anwendungsdateien vor, die zu klein sind, um eine Änderung des Produktcodes zu rechtfertigen. Weitere Informationen finden Sie unter [Patchen und Upgrades.](patching-and-upgrades.md)

In diesem Beispiel wird veranschaulicht, wie Sie ein Windows Installer-Patchpaket erstellen, das das Concert-Feature des hypothetischen Produkts MNP2000 aktualisiert, um einen Fehler im ursprünglichen Produkt zu beheben. Das Beispielpatchpaket wendet ein kleines Update auf das Produkt an, für das keine Änderung des Produktcodes erforderlich ist. Weitere Informationen zu [größeren Upgrades](major-upgrades.md) finden Sie im Thema Zu größeren Upgrades im Abschnitt [Patchen und Upgrades.](patching-and-upgrades.md)

Das Beispielupgradepaket weist die folgenden Spezifikationen auf:

-   Es wird ein kleiner Fehler im Vom Concert-Feature angezeigten Concert-Zeitplan korrigiert.
-   Der Paketcode wird aktualisiert, um zu berücksichtigen, dass sich das Installationspaket geändert hat.
-   Das kleine Update kann durch Patchen der lokalen Installation des Produkts angewendet werden.

[Fortsetzen](planning-a-small-update-patch.md)

 

 



