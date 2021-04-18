---
description: Sie können einem lokalen Volume einen Laufwerk Buchstaben (z. b. X:) zuweisen \) , indem Sie die setvolumemountpoint-Funktion verwenden, vorausgesetzt, dass diesem Laufwerk Buchstaben nicht bereits ein Volume zugeordnet ist.
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Zuweisen eines Laufwerk Buchstabens zu einem Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343416"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a>Zuweisen eines Laufwerk Buchstabens zu einem Volume

Sie können einem lokalen Volume einen Laufwerk Buchstaben (z. b. X:) zuweisen \) , indem Sie die [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) -Funktion verwenden, vorausgesetzt, dass diesem Laufwerk Buchstaben nicht bereits ein Volume zugeordnet ist. , Wenn das lokale Volume bereits über einen Laufwerk Buchstaben verfügt. [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) schlägt fehl. Um dies zu behandeln, löschen Sie zuerst den Laufwerk Buchstaben mithilfe der [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) -Funktion. Beispielcode finden Sie unter [Bearbeiten von Laufwerk Buchstaben Zuweisungen](editing-drive-letter-assignments.md).

Das System unterstützt höchstens einen Laufwerk Buchstaben pro Volume. Daher ist es nicht möglich, dass C: \\ und F: \\ dasselbe Volume darstellen.

> [!Caution]
>
> Wenn Sie einen vorhandenen Laufwerk Buchstaben löschen und einen neuen zuweisen, können vorhandene Pfade, z. b. die in Desktop Verknüpfungen Möglicherweise wird auch der Pfad des Programms unterbrechen, sodass der Laufwerksbuchstabe geändert wird. Mit der Verwaltung von virtuellen Windows-Arbeitsspeicher kann dies die Anwendung unterbrechen, sodass das System instabil und möglicherweise unbrauchbar ist. Der Programm-Designer ist dafür verantwortlich, derartige potenzielle Katastrophen zu vermeiden.

 

 

 



