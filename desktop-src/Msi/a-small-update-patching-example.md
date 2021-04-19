---
description: In diesem Beispiel wird veranschaulicht, wie ein Patchpaket erstellt wird, das ein kleines Update auf das Beispiel Installationspaket anwendet, das in einem Installations Beispiel erläutert wird.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Beispiel für ein kleines Update-Patching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349368"
---
# <a name="a-small-update-patching-example"></a>Beispiel für ein kleines Update-Patching

In diesem Beispiel wird veranschaulicht, wie ein [Patchpaket](patch-packages.md) erstellt wird, das ein [kleines Update](small-updates.md) auf das Beispiel Installationspaket anwendet, das in [einem Installations Beispiel](an-installation-example.md)erläutert wird. Ein kleines Update nimmt Änderungen an einer oder mehreren Anwendungs Dateien vor, die als zu gering eingestuft werden, um das Ändern des Produktcodes zu rechtfertigen. Weitere Informationen finden Sie unter [Patching und Upgrades](patching-and-upgrades.md).

In diesem Beispiel wird veranschaulicht, wie ein Windows Installer Patch-Paket erstellt wird, mit dem die Konzert Funktion des hypothetischen Product MNP2000 aktualisiert wird, um einen Fehler im ursprünglichen Produkt zu beheben. Das Patchpaket für das Beispiel wendet ein kleines Update auf das Produkt an, das keine Änderung des Produktcodes erfordert. Weitere Informationen zu wichtigen Upgrades finden Sie im Abschnitt zu den [wichtigsten Upgrades](major-upgrades.md) im Abschnitt " [Patching und Upgrades](patching-and-upgrades.md) ".

Das Beispiel Aktualisierungs Paket verfügt über die folgenden Spezifikationen:

-   Es korrigiert einen geringfügigen Fehler in dem Konzert Zeitplan, der durch das Konzert Feature angezeigt wird.
-   Der Paket Code wird aktualisiert, um widerzuspiegeln, dass sich das Installationspaket geändert hat.
-   Das kleine Update kann durch Patchen der lokalen Installation des Produkts angewendet werden.

[Fortsetzen](planning-a-small-update-patch.md)

 

 



