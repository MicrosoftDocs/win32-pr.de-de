---
description: 'Sie können einem \) lokalen Volume mithilfe der SetVolumeMountPoint-Funktion einen Laufwerkbuchstaben (z. B. X: ) zuweisen, sofern diesem Laufwerkbuchstaben noch kein Volume zugewiesen ist.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Zuweisen eines Laufwerkbuchstabens zu einem Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cc2e894580a394e73896291f05a2f54c615949bfeb63ea3e574deef1353d91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766223"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Zuweisen eines Laufwerkbuchstabens zu einem Volume

Sie können einem \) lokalen Volume mithilfe der [**SetVolumeMountPoint-Funktion**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) einen Laufwerkbuchstaben (z. B. X: ) zuweisen, sofern diesem Laufwerkbuchstaben noch kein Volume zugewiesen ist. Wenn das lokale Volume bereits über einen Laufwerkbuchstaben verfügt. dann schlägt [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) fehl. Löschen Sie hierzu zunächst den Laufwerkbuchstaben mithilfe der [**DeleteVolumeMountPoint-Funktion.**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) Beispielcode finden Sie unter [Bearbeiten von Laufwerkbuchstabenzuweisungen.](editing-drive-letter-assignments.md)

Das System unterstützt höchstens einen Laufwerkbuchstaben pro Volume. Daher können C: \\ und F: \\ nicht das gleiche Volume darstellen.

> [!Caution]
>
> Das Löschen eines vorhandenen Laufwerkbuchstabens und das Zuweisen eines neuen Laufwerkbuchstabens kann dazu führen, dass vorhandene Pfade, z. B. in Desktopverknüpfungen, nicht mehr vorhanden sind. Es kann auch den Pfad zum Programm unterbrechen, das die Laufwerkbuchstaben ändert. Bei Windows verwaltung des virtuellen Arbeitsspeichers kann dies die Anwendung unterbrechen, sodass das System in einem instabilen und möglicherweise unbrauchbaren Zustand verbleibt. Es liegt in der Verantwortung des Programmdesigners, solche potenziellen Katastrophen zu vermeiden.

 

 

 



